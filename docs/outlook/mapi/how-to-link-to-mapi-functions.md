---
title: Ссылки на функции MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346887"
---
# <a name="link-to-mapi-functions"></a>Ссылки на функции MAPI

**Относится к**: Outlook 2013 | Outlook 2016 
  
Существует три метода связывания: неявное связывание, явное связывание и Новая Гибридная модель, использующая библиотеку-заглушку MAPI.
  
## <a name="implicit-linking"></a>Неявное связывание

Исторически вызов функций MAPI в приложении обмена сообщениями всегда включал ссылку на библиотеку mapi32. lib. Это включало вызовы маршрутизации MAPI в библиотеку заглушек Windows MAPI, MAPI32. dll, которая затем перенаправляет вызовы на реализацию клиента MAPI по умолчанию во время выполнения. Этот процесс вызова называется неявным связыванием. В левой части следующего рисунка показан пример неявной ссылки, используемой в процессе вызова функции MAPI. Процесс инициируется приложением MAPI и включает библиотеку MAPI (MAPI32. lib) и заглушку Windows MAPI (MAPI32. dll) и завершается реализацией клиента MAPI Outlook для заглушки MAPI (Msmapi32. dll).
  
**Сравнение неявного и неявного связывания.**

![Сравнение неявного и явного сравнения ссылок]для неявного и(media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "неявного связывания")
  
## <a name="explicit-linking"></a>Явное связывание

Так как клиент MAPI по умолчанию поддерживает установку по запросу с помощью установщика Windows (MSI), вы можете разрабатывать приложения для обмена сообщениями непосредственно на заглушке Outlook MAPI, а не с помощью библиотеки MAPI и заглушки Windows MAPI. В правой части предыдущего рисунка показан пример процесса вызова функции MAPI, начиная с приложения MAPI, в котором выполняется поиск пути и имени DLL для заглушки Outlook MAPI (шаг 2 в следующем разделе), и вызовы функций в заглушке Outlook MAPI (шаг 3 в следующем разделе). В следующей процедуре показано, как вызывать функции MAPI с помощью явной ссылки. 
  
> [!NOTE]
> Эта информация о явном связывании может быть избыточной для ваших потребностей с введением Мапистублибрари. lib, обсуждаемой в следующем разделе. Как и в случае неявной модели, Новая библиотека управляет всеми и реализует явную логику связывания, которая загружает MAPI Outlook напрямую. 
  
Более подробную информацию о явном связывании можно найти в разделе Links.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Вызов элементов API MAPI без библиотеки MAPI и заглушки Windows MAPI

1. В файле программы создайте глобальный список указателей функций для каждого используемого элемента API MAPI. 
    
   В приведенном ниже примере показан этот шаг.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Создайте функцию, которая инициализирует функции MAPI для связи с БИБЛИОТЕКой MAPI клиента MAPI по умолчанию (например, Msmapi32. dll для Microsoft Outlook). В этой функции выполните следующие действия: 
    
    1. Загрузите MAPI32. dll из соответствующего системного каталога. 
        
       |||
       |:-----|:-----|
       |x64 или x86 с оригинальной версии  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 в режиме WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Вызовите функцию [фжеткомпонентпас](fgetcomponentpath.md) , чтобы получить путь и имя DLL, которые реализуют подсистему MAPI. Дополнительные сведения см. [в статье Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Загрузите DLL, вызвав функцию LoadLibrary. 
        
    4. Инициализируйте массив указателей функций MAPI, вызвав функцию GetProcAddress. 
        
    В следующем примере показаны предыдущие действия:
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. Наконец, вызовите функцию, созданную в действии 2 в своем приложении для обмена сообщениями, прежде чем совершать вызовы в элементы API MAPI. 
    
   > [!CAUTION]
   > Перед закрытием приложения необходимо деинициализировать подсистему MAPI. 
  
   В следующем примере показан этот шаг: 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a>Мапистублибрари. lib

Появление Microsoft Outlook 2010 и 64-разрядной версии MAPI, теперь расширено до Microsoft Outlook 2013, требует больше, чем традиционный 32-разрядный API для полной реализации. Новый проект, Библиотека заглушек MAPI, опубликованная на веб-сайте CodePlex, предоставляет возможность замены для MAPI32. lib, которая поддерживает создание приложений для 32-и 64-разрядной версии MAPI. Мапистублибрари. lib исключает необходимость явной ссылки на MAPI и ее построения, вы можете удалить MAPI32. lib из параметров компоновщика, заменив его на Мапистублибрари. lib; дальнейшие изменения кода не требуются. Кроме того, она исключает необходимость написания кода **LoadLibrary**, **GetProcAddress**и **FreeLibrary** для обработки более новых экспортируемых компонентов, включенных в файл библиотеки, но не в MAPI32. lib, что было бы необходимым при использовании явного связывания. 
  
Некоторые новые функции, связанные с этой библиотекой и недоступные в MAPI32. lib, включают следующие:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Альтернативным способом включения библиотеки-заглушки MAPI является копирование исходных файлов, Мапистублибрари. cpp и Стубутилс. cpp, непосредственно в проект и удаление любой ссылки на MAPI32. lib и любой код, явно ссылающийся на MAPI.
  
Чтобы получить доступ к файлам библиотеки-заглушки MAPI, а также сведения о том, как создать и интегрировать ее в проект, а также на вопросы об этой библиотеке, например, когда и зачем ее использовать, обратитесь к [библиотеке заглушек MAPI](https://mapistublibrary.codeplex.com/documentation) на сайте CodePlex. 
  
## <a name="see-also"></a>См. также

- [Общие сведения о программировании MAPI](mapi-programming-overview.md)
- [Установка подсистемы MAPI](installing-the-mapi-subsystem.md)
- [Установка файлов заголовков MAPI](how-to-install-mapi-header-files.md)
- [Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Определение используемого метода связывания](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Связывание исполняемого файла с библиотекой DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Настройка ключей MSI для библиотеки MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

