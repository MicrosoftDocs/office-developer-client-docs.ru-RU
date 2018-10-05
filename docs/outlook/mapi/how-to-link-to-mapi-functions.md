---
title: Ссылка на функции MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400147"
---
# <a name="link-to-mapi-functions"></a>Ссылка на функции MAPI

**Относится к**: Outlook 2013 | Outlook 2016 
  
Существует три метода компоновки: неявное связывание, явного связывания и новая модель гибридного использования библиотеки заглушка MAPI.
  
## <a name="implicit-linking"></a>Неявное связывание

С исторической точки зрения вызов функции MAPI в приложение для обмена сообщениями всегда задействованных ссылки на библиотеку Mapi32.lib. Это включенные маршрутизации вызовов MAPI в библиотеку заглушка Windows MAPI Mapi32.dll, который затем передается вызовы реализации клиента MAPI по умолчанию во время выполнения. Этот процесс вызова называется неявное связывание. В левой части на следующем рисунке показан пример неявного связывания в процесс вызова функции MAPI. Процесс инициируется приложения MAPI и состоит из библиотеки MAPI (Mapi32.lib) и заглушка Windows MAPI (Mapi32.dll) и завершения реализации клиент Outlook MAPI заглушка MAPI (Msmapi32.dll).
  
**Сравнение неявного и явного связывания.**

![Сравнение неявного и явного связывания] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Сравнение неявного и явного связывания")
  
## <a name="explicit-linking"></a>Связывание Explicit

Так как клиент MAPI по умолчанию поддерживает установку по запросу с помощью установщика Windows (MSI), вы можете создавать приложений для обмена сообщениями непосредственно на заглушка Outlook MAPI вместо использования библиотеки MAPI и заглушка Windows MAPI. В правой части на предыдущем рисунке показан пример MAPI процесс вызова функции, начиная с приложения MAPI ищете путь и имя DLL-Библиотеку Outlook MAPI заглушка (шаг 2 в следующем разделе) и вызовов функций в (заглушку Outlook MAPI Шаг 3 в следующем разделе). Следующей процедуре показано, как вызывать функции MAPI с помощью явного связывания. 
  
> [!NOTE]
> Эти сведения о явного связывания может быть избыточным в соответствии с потребностями с введением MAPIStubLibrary.lib, обсуждаемые в следующем разделе. Как неявные модели новую библиотеку управляет всех компонентов и реализует явного связывания логику, которая загружает Outlook MAPI напрямую. 
  
Дополнительные сведения о явного связывания можно явно ссылки.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Чтобы вызвать элементы API-интерфейса MAPI без библиотеки MAPI и заглушка Windows MAPI

1. В файле программы создания глобального списка указатели на функции для каждого элемента MAPI API, которое используется. 
    
   В следующем примере показано это действие.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Создание функции, инициализирует функции MAPI для ссылки на библиотеку DLL MAPI клиент MAPI по умолчанию (например, Msmapi32.dll из Microsoft Outlook). В этой функции выполните следующие действия. 
    
    1. Загрузите mapi32.dll из каталога, соответствующую систему. 
        
       |||
       |:-----|:-----|
       |x64 или x86 изначально  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 в режиме WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Вызовите функцию [FGetComponentPath](fgetcomponentpath.md) для получения путь и имя библиотеки DLL, который реализует подсистемы MAPI. Дополнительные сведения можно [выбрать определенные версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Загрузите DLL путем вызова функции LoadLibrary. 
        
    4. Инициализация массива указатель функции MAPI путем вызова функции GetProcAddress. 
        
    В следующем примере показано предыдущие действия:
        
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

3. И, наконец вызовите функцию, созданный на шаге 2 в приложение для обмена сообщениями прежде чем выполнять вызовы к элементам API-интерфейса MAPI. 
    
   > [!CAUTION]
   > Необходимо выполнении отмены инициализации подсистемы MAPI перед закрытием приложения. 
  
   В следующем примере показано это действие: 
    
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

После выпуска Microsoft Outlook 2010 и 64-разрядная версия MAPI, теперь расширение для Microsoft Outlook 2013 требуется больше, чем традиционные API 32-разрядная версия для полная реализация. Новый проект в библиотеку заглушка MAPI, размещенные на веб-сайте CodePlex предоставляет замены сборка для Mapi32.lib, поддерживающего построение приложений MAPI в 32- и 64-разрядная версия. MAPIStubLibrary.lib устраняет необходимость явного связывания MAPI и построения, можно удалить Mapi32.lib из параметры настройки компоновщика, заменив MAPIStubLibrary.lib; следует необходимые дополнительные изменения в коде. Он также позволяет отказаться от писать код **LoadLibrary** **GetProcAddress**и **FreeLibrary** обрабатывать новые экспорта, включенные в этот файл библиотеки, но не в Mapi32.lib, который может потребоваться при использовании явного связывания. 
  
Ниже перечислены некоторые из новых функций, связанные с этой библиотеки, которые не доступны в Mapi32.lib:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Другой способ включения библиотеки заглушка MAPI — это скопировать исходные файлы MapiStubLibrary.cpp и StubUtils.cpp, непосредственно в проект и удаление любое взаимодействие Mapi32.lib и любой код, который явно связано MAPI.
  
Доступ к файлам библиотеки заглушка MAPI и сведения о создании и интегрировать в проект, а также вопросы об этой библиотеки например, когда и почему его использование, см в [Библиотеке заглушка MAPI](https://mapistublibrary.codeplex.com/documentation) на сайте CodePlex. 
  
## <a name="see-also"></a>См. также

- [����� �������� � ���������������� MAPI](mapi-programming-overview.md)
- [Установка подсистемы MAPI](installing-the-mapi-subsystem.md)
- [Установка файлов заголовков MAPI](how-to-install-mapi-header-files.md)
- [Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Определение подходящего метода связывания для использования](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Связывание исполняемого файла для библиотеки DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Настройка разделов MSI для библиотеки DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

