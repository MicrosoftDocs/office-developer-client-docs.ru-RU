---
title: Инициализация поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Последнее изменение: 05 октября 2012 г.'
ms.openlocfilehash: 31114e4082fbc5e4c57da95eb6b32339822b1645
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427824"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Инициализация поставщика упакованного PST-хранилища

**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы реализовать завернутый поставщик файлов личных папок (PST), необходимо инициализировать поставщика магазина PST с помощью **[функции MSProviderInit](msproviderinit.md)** в качестве точки входа. После инициализации DLL поставщика функция **[MSGSERVICEENTRY](msgserviceentry.md)** настраивает поставщика магазина PST. 
  
В этом разделе функция **MSProviderInit** и **функция MSGSERVICEENTRY** демонстрируются с помощью примеров кода из поставщика магазинов ПСД sample Wrapped. В примере реализован завернутый поставщик PST, который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке поставщика магазинов PST sample wrapped см. в примере Установки поставщика упаковки [PST Store.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)
  
После инициализации поставщика магазинов PST необходимо реализовать функции, чтобы MAPI и spooler MAPI могли войти в поставщик магазина сообщений. Дополнительные сведения см. в [журнале On to a Wrapped PST Store Provider.](logging-on-to-a-wrapped-pst-store-provider.md)
  
## <a name="initialization-routine"></a>Процедура инициализации

Все поставщики магазинов PST должны реализовать функцию **[MSProviderInit](msproviderinit.md)** в качестве точки входа для инициализации DLL поставщика. **MSProviderInit** проверяет, совместим ли номер версии интерфейса поставщика услуг  `ulMAPIVer` с текущим номером  `CURRENT_SPI_VERSION` версии. Функция сохраняет режимы управления памятью MAPI в  `g_lpAllocateBuffer` параметры и  `g_lpAllocateMore`  `g_lpFreeBuffer` параметры. Эти процедуры управления памятью следует использовать во всей реализации магазина PST для распределения памяти и решения. 
  
### <a name="msproviderinit-example"></a>Пример MSProviderInit()

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a>Завернутые пути PST и Unicode

Чтобы модифицировать исходный пример, подготовленный в Microsoft Visual Studio 2008 г. для использования путей Юникод в NST для использования в Microsoft Outlook 2010, русская версия и Outlook 2013 г., в **режиме CreateStoreEntryID,** который производит идентификатор входа, следует использовать один формат для путей ASCII, а другой для путей Unicode. Они представлены в качестве структур в следующем примере. 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> Различия в этих структурах имеют два NULL-bytes до пути Юникод. Если вам нужно интерпретировать идентификатор записи в "Режиме входа в службу", который следует, одним из способов определить, является ли это случаем или нет, было бы бросить в качестве EIDMS сначала, а затем проверить, является ли szPath[0] NULL. Если это так, вместо этого отдай его в качестве EIDMSW. 
  
## <a name="service-entry-routine"></a>Процедура входа в службу

Функция **[MSGSERVICEENTRY](msgserviceentry.md)** — это точка входа в службу сообщений, в которой настроен поставщик магазина PST. Функция вызывает  `GetMemAllocRoutines()` для получения процедур управления памятью MAPI. Функция использует параметр, чтобы найти раздел профилей для поставщика и задает  `lpProviderAdmin` свойства в профиле. 
  
### <a name="serviceentry-example"></a>Пример ServiceEntry()

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a>См. также

- [О поставщике пакетных пакетов PST Store](about-the-sample-wrapped-pst-store-provider.md)
- [Установка поставщика пакетных пакетов PST](installing-the-sample-wrapped-pst-store-provider.md)
- [Ведение журнала в поставщике упакованных магазинов PST](logging-on-to-a-wrapped-pst-store-provider.md)
- [Использование поставщика упакованных магазинов PST](using-a-wrapped-pst-store-provider.md)
- [Отключение поставщика упакованных магазинов PST](shutting-down-a-wrapped-pst-store-provider.md)

