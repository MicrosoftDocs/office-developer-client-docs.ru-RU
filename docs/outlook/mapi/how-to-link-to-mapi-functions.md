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
  
Существует три способа связывания: неявное связывание, явное связывание и новая гибридная модель с помощью библиотеки заголовок MAPI.
  
## <a name="implicit-linking"></a>Неявное связывание

Традиционно вызов функций MAPI в приложении для обмена сообщениями всегда связывался с библиотекой Mapi32.lib. Это включало вызовы MAPI маршрутов в библиотеку загонов Windows MAPI, Mapi32.dll, которая затем перенаададовыла вызовы в клиентскую реализацию MAPI по умолчанию во время выполнения. Этот процесс вызова называется неявной связью. В левой части рисунка ниже показан пример неявной связи, используемой в процессе вызова функции MAPI. Этот процесс инициализировался приложением MAPI и включает библиотеку MAPI (Mapi32.lib) и загую Windows MAPI (Mapi32.dll) и его можно завершить с помощью клиентской реализации MAPI Outlook в загладке MAPI (Msmapi32.dll).
  
**Сравнение неявных и явных ссылок.**

![Сравнение неявного и явного связывания](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Сравнения неявных и явных ссылок")
  
## <a name="explicit-linking"></a>Явное связывание

Так как клиент MAPI по умолчанию поддерживает установку по требованию с помощью установщика Windows (MSI), можно разрабатывать приложения для обмена сообщениями непосредственно на загоне MAPI Outlook, а не с помощью библиотеки MAPI и загона Windows MAPI. В правой части предыдущего рисунка показан пример процесса вызова функции MAPI, начиная с приложения MAPI, которое ищет путь и имя DLL для загладки MAPI Outlook (шаг 2 в следующем разделе) и делает вызов функции в загрезке Outlook MAPI (шаг 3 в следующем разделе). В следующей процедуре показано, как вызывать функции MAPI с использованием явных ссылок. 
  
> [!NOTE]
> Эти сведения об явных связываниях могут быть лишними в соответствии с вашими потребностями с появлением MAPIStubLibrary.lib, рассмотренного в следующем разделе. Как и неявная модель, новая библиотека управляет всем и реализует явную логику связывания, которая загружает MAPI Outlook напрямую. 
  
Дополнительные сведения об явных ссылках см. в явной ссылке.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Вызов элементов API MAPI без библиотеки MAPI и заголовки Windows MAPI

1. В файле программы создайте глобальный список указателей функций для каждого используемого элемента API MAPI. 
    
   В следующем примере показан этот шаг.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Создайте функцию, которая инициализирует функции MAPI для ссылки на DLL MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Microsoft Outlook). В этой функции сделайте следующее: 
    
    1. Загруз mapi32.dll из соответствующего системного каталога. 
        
       |||
       |:-----|:-----|
       |X64 или x86 в основном  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 в режиме WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Вызовите [функцию FGetComponentPath,](fgetcomponentpath.md) чтобы получить путь и имя DLL, реализуя подсистему MAPI. Дополнительные сведения см. в [поддоме "Выбор конкретной версии MAPI для загрузки".](how-to-choose-a-specific-version-of-mapi-to-load.md)
        
    3. Загрузив DLL, выполняв вызов функции LoadLibrary. 
        
    4. Инициализировать массив указателей функции MAPI с помощью вызова функции GetProcAddress. 
        
    В следующем примере показаны предыдущие шаги:
        
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

3. Наконец, вызовите функцию, созданную на шаге 2 в приложении для обмена сообщениями, прежде чем вызывать элементы API MAPI. 
    
   > [!CAUTION]
   > Перед закрытием приложения необходимо инициализировать подсистему MAPI. 
  
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

Для полной реализации Microsoft Outlook 2010, русская версия 64-битного MAPI, который теперь распространяется на Microsoft Outlook 2013, требуется больше, чем традиционный 32-битный API. Новый проект, библиотека ЗАГТ MAPI, опубликованная на веб-сайте CodePlex, представляет собой замену для Mapi32.lib, которая поддерживает создание как 32-, так и 64-битных приложений MAPI. MAPIStubLibrary.lib устраняет необходимость явного связывания с MAPI, и после его создания можно удалить Mapi32.lib из параметров linker, заменив его на MAPIStubLibrary.lib; Никаких дальнейших изменений в коде не требуется. Он также устраняет необходимость в написании **кода LoadLibrary,** **GetProcAddress** и **FreeLibrary** для обработки новых экспортов, включенных в этот файл библиотеки, но не в Файл Mapi32.lib, что потребуется при явном связывание. 
  
Некоторые из новых функций, связанных с этой библиотекой, недоступны в Mapi32.lib, включают следующие:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Альтернативным способом включения библиотеки затуха MAPI является копирование исходных файлов MapiStubLibrary.cpp и StubUtils.cpp непосредственно в проект и удаление ссылок на Mapi32.lib и любой код, явным образом ссылающийся на MAPI.
  
Сведения о том, как создать и интегрировать библиотеку в свой проект, а также вопросы об этой библиотеке, например о том, когда и зачем ее использовать, см. в библиотеке [ЗАТМ MAPI](https://mapistublibrary.codeplex.com/documentation) на сайте CodePlex. 
  
## <a name="see-also"></a>См. также

- [Общие сведения о программировании MAPI](mapi-programming-overview.md)
- [Установка подсистемы MAPI](installing-the-mapi-subsystem.md)
- [Установка файлов заголовок MAPI](how-to-install-mapi-header-files.md)
- [Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Определение используемого метода связывания](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Связывание исполняемого исполняемого с DLL-данными](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Настройка ключей MSI для DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

