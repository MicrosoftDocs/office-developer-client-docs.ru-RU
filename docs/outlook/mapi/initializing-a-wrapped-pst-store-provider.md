---
title: Инициализация оболочку поставщика хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Последнее изменение: 05 октября 2012 г.'
ms.openlocfilehash: a332c63814163579d5fe8ab365145e9583fa6c97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809457"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Инициализация оболочку поставщика хранилища PST-файлов

**Применимо к**: Outlook 
  
Чтобы реализовать оболочку поставщика хранилища личных папок (PST) файла, должны инициализировать оболочку поставщика хранилища PST-файлов, используя функцию **[MSProviderInit](msproviderinit.md)** в качестве точки входа. После инициализации DLL поставщика функции **[MSGSERVICEENTRY](msgserviceentry.md)** настраивает оболочку поставщика хранилища PST-файлов. 
  
В этом разделе функции **MSProviderInit** и **MSGSERVICEENTRY** демонстрируются с помощью примеров кода с переносом PST поставщик хранилища. В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации. Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см. Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).
  
После инициализации оболочку поставщика хранилища PST-файлов необходимо реализовать функции, чтобы MAPI и диспетчер очереди MAPI могут войти на поставщика хранилища сообщений. Для получения дополнительных сведений см [Ведения журнала на оболочку поставщик хранилища PST -файлов](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Программа инициализации

Все поставщики оболочку хранилища PST-файлов необходимо реализовать функцию **[MSProviderInit](msproviderinit.md)** как точки входа для инициализации DLL поставщика. **MSProviderInit** проверяет, если номер версии интерфейса поставщика службы `ulMAPIVer`, совместимый с текущий номер версии `CURRENT_SPI_VERSION`. Функция сохраняет памяти MAPI процедуры управления в `g_lpAllocateBuffer`, `g_lpAllocateMore`, и `g_lpFreeBuffer` параметры. Для выделения памяти и освобождение можно использовать эти процедуры управления памяти во всем оболочку реализация хранилища PST-файлов. 
  
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

### <a name="wrapped-pst-and-unicode-paths"></a>Перенос PST-файлов и Юникод пути

Модифицировать исходный образец, подготовленном на Microsoft Visual Studio 2008 для использования Юникод пути к NST для использования в Microsoft Outlook 2010 с поддержкой Юникода и Outlook 2013, должны использовать процедуру **CreateStoreEntryID** , который позволяет получить идентификатор записи, один формат для пути ASCII, а другой Юникод пути. Далее представлены как структуры в следующем примере. 
  
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
> Различия в эти структуры, два байта NULL перед путь в формате Юникод. Если вам требуется самостоятельно интерпретировать идентификатор записи в «служба запись процедуры», исходя из, одним из способов определить, является ли, так и не будет привести как EIDMS во-первых, после чего проверьте ли szPath [0] имеет значение NULL. Если он установлен, приведены его как EIDMSW. 
  
## <a name="service-entry-routine"></a>Процедура записи службы

Функция **[MSGSERVICEENTRY](msgserviceentry.md)** — точка входа службы сообщений, где настроены оболочку поставщика хранилища PST-файлов. Вызовы функций `GetMemAllocRoutines()` для получения памяти MAPI процедуры управления. Использует функцию `lpProviderAdmin` параметр найдите раздел профиля для поставщика и наборов свойств в профиле. 
  
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

- [О примере оболочку поставщика хранилища PST-файлов](about-the-sample-wrapped-pst-store-provider.md)
- [Установка примера оболочку поставщика хранилища PST-файлов](installing-the-sample-wrapped-pst-store-provider.md)
- [Выполнив вход поставщик оболочку хранения PST-файлов](logging-on-to-a-wrapped-pst-store-provider.md)
- [С помощью поставщика оболочку хранилища PST-файлов](using-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика оболочку хранения PST-файлов](shutting-down-a-wrapped-pst-store-provider.md)

