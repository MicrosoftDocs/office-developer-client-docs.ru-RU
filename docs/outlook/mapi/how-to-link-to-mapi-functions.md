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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует три способа связывания: неявная привязка, явные ссылки и новая гибридная модель с помощью библиотеки STUB MAPI.
  
## <a name="implicit-linking"></a>Неявная привязка

Исторически функции MAPI в приложении обмена сообщениями всегда связаны со ссылкой на библиотеку Mapi32.lib. Это включало маршрутику вызовов MAPI в библиотеку Windows MAPI, Mapi32.dll, которая затем перенаадлила вызовы в клиентскую реализацию MAPI по умолчанию во время выполнения. Этот процесс вызова называется неявной привязкой. На левой стороне следующей фигуры показан пример неявной привязки, используемой в процессе вызова функции MAPI. Процесс инициировался приложением MAPI и включает библиотеку MAPI (Mapi32.lib) и загбаум Windows MAPI (Mapi32.dll) и завершится клиентской реализацией Outlook MAPI загмы MAPI (Msmapi32.dll).
  
**Сравнение неявных и явных ссылок.**

![Сравнение неявного и явного сопоставления](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "сопоставления неявной и явной связи")
  
## <a name="explicit-linking"></a>Явные ссылки

Поскольку клиент MAPI по умолчанию поддерживает установку по требованию с помощью установки Windows (MSI), приложения обмена сообщениями можно разрабатывать непосредственно на Outlook MAPI, а не с помощью библиотеки MAPI и Windows MAPI. На правой стороне предыдущего рисунка показан пример процесса вызова функции MAPI, начиная с приложения MAPI, которое ищет путь и имя DLL для загба Outlook MAPI (шаг 2 в следующем разделе) и делает вызовы функций в Outlook MAPI (шаг 3 в следующем разделе). В следующей процедуре показано, как вызывать функции MAPI с помощью явных ссылок. 
  
> [!NOTE]
> Эти сведения о явной связи могут быть лишними для ваших потребностей с введением MAPIStubLibrary.lib, рассмотренного в следующем разделе. Как и неявная модель, новая библиотека управляет всем и реализует явную логику связывания, которая загружает Outlook MAPI компании. 
  
Дополнительные сведения о явной ссылке см. в ссылке Explicitly.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Вызов элементов API MAPI без библиотеки MAPI и Windows MAPI

1. В файле программы создайте глобальный список указателей функции для каждого используемого элемента API MAPI. 
    
   В следующем примере показан этот шаг.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Создайте функцию, которая инициализирует функции MAPI для ссылки на DLL MAPI клиента MAPI по умолчанию (например, Msmapi32.dll Microsoft Outlook). В этой функции сделайте следующее: 
    
    1. Загрузка mapi32.dll из соответствующего каталога системы. 
        
       |||
       |:-----|:-----|
       |x64 или x86  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 в режиме WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Позвоните [в функцию FGetComponentPath,](fgetcomponentpath.md) чтобы получить путь и имя DLL, реализуемую подсистемой MAPI. Дополнительные сведения см. [в специальной версии MAPI для загрузки.](how-to-choose-a-specific-version-of-mapi-to-load.md)
        
    3. Загрузив DLL, вызов функции LoadLibrary. 
        
    4. Инициализация массива указателей функции MAPI с помощью вызова функции GetProcAddress. 
        
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

3. Наконец, перед вызовом элементов API MAPI вызывайте функцию, созданную на шаге 2 в приложении обмена сообщениями. 
    
   > [!CAUTION]
   > Перед закрытием приложения необходимо униниализовать подсистему MAPI. 
  
   В следующем примере показан следующий шаг: 
    
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

Появление Microsoft Outlook 2010, русская версия и 64-битных MAPI, теперь расширяющихся до Microsoft Outlook 2013, требует большего, чем традиционный 32-битный API для полной реализации. Новый проект , библиотека stub MAPI, размещенная на веб-сайте CodePlex, предоставляет замену для Mapi32.lib, которая поддерживает создание как 32-битных, так и 64-битных приложений MAPI. MAPIStubLibrary.lib устраняет необходимость прямой ссылки на MAPI, и, построив ее, можно удалить Mapi32.lib из параметров linker, заменив ее на MAPIStubLibrary.lib; никаких дальнейших изменений в коде не требуется. Он также устраняет необходимость записи **Кода LoadLibrary,** **GetProcAddress** и **FreeLibrary** для обработки новых экспортов, включенных в этот файл библиотеки, но не в Mapi32.lib, которые будут необходимы, если вы использовали явные ссылки. 
  
Некоторые из новых функций, связанных с этой библиотекой, недоступные в Mapi32.lib, включают следующие:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Альтернативным методом включения библиотеки stub MAPI является копирование исходных файлов MapiStubLibrary.cpp и StubUtils.cpp непосредственно в проект и удаление любых ссылок на Mapi32.lib и любого кода, явно ссылаясь на MAPI.
  
Сведения о создании и интеграции файлов библиотеки MAPI Stub, а также вопросы об этой библиотеке, например о том, когда и зачем ее использовать, см. в библиотеке [MAPI Stub на](https://mapistublibrary.codeplex.com/documentation) сайте CodePlex. 
  
## <a name="see-also"></a>См. также

- [Общие сведения о программировании MAPI](mapi-programming-overview.md)
- [Установка подсистемы MAPI](installing-the-mapi-subsystem.md)
- [Установка файлов заголовки MAPI](how-to-install-mapi-header-files.md)
- [Выберите определенную версию MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Определение способа привязки к использованию](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Привязка исполняемого к DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Настройка клавиш MSI для DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

