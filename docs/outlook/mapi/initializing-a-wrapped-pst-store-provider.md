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
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="2ccf2-103">Инициализация оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="2ccf2-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="2ccf2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ccf2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ccf2-105">Чтобы реализовать оболочку поставщика хранилища личных папок (PST) файла, должны инициализировать оболочку поставщика хранилища PST-файлов, используя функцию **[MSProviderInit](msproviderinit.md)** в качестве точки входа.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="2ccf2-106">После инициализации DLL поставщика функции **[MSGSERVICEENTRY](msgserviceentry.md)** настраивает оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="2ccf2-107">В этом разделе функции **MSProviderInit** и **MSGSERVICEENTRY** демонстрируются с помощью примеров кода с переносом PST поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="2ccf2-108">В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="2ccf2-109">Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="2ccf2-110">Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="2ccf2-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="2ccf2-111">После инициализации оболочку поставщика хранилища PST-файлов необходимо реализовать функции, чтобы MAPI и диспетчер очереди MAPI могут войти на поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="2ccf2-112">Для получения дополнительных сведений см [Ведения журнала на оболочку поставщик хранилища PST -файлов](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2ccf2-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="2ccf2-113">Программа инициализации</span><span class="sxs-lookup"><span data-stu-id="2ccf2-113">Initialization routine</span></span>

<span data-ttu-id="2ccf2-114">Все поставщики оболочку хранилища PST-файлов необходимо реализовать функцию **[MSProviderInit](msproviderinit.md)** как точки входа для инициализации DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="2ccf2-115">**MSProviderInit** проверяет, если номер версии интерфейса поставщика службы `ulMAPIVer`, совместимый с текущий номер версии `CURRENT_SPI_VERSION`.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="2ccf2-116">Функция сохраняет памяти MAPI процедуры управления в `g_lpAllocateBuffer`, `g_lpAllocateMore`, и `g_lpFreeBuffer` параметры.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="2ccf2-117">Для выделения памяти и освобождение можно использовать эти процедуры управления памяти во всем оболочку реализация хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="2ccf2-118">Пример MSProviderInit()</span><span class="sxs-lookup"><span data-stu-id="2ccf2-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="2ccf2-119">Перенос PST-файлов и Юникод пути</span><span class="sxs-lookup"><span data-stu-id="2ccf2-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="2ccf2-120">Модифицировать исходный образец, подготовленном на Microsoft Visual Studio 2008 для использования Юникод пути к NST для использования в Microsoft Outlook 2010 с поддержкой Юникода и Outlook 2013, должны использовать процедуру **CreateStoreEntryID** , который позволяет получить идентификатор записи, один формат для пути ASCII, а другой Юникод пути.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="2ccf2-121">Далее представлены как структуры в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="2ccf2-122">Различия в эти структуры, два байта NULL перед путь в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="2ccf2-123">Если вам требуется самостоятельно интерпретировать идентификатор записи в «служба запись процедуры», исходя из, одним из способов определить, является ли, так и не будет привести как EIDMS во-первых, после чего проверьте ли szPath [0] имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="2ccf2-124">Если он установлен, приведены его как EIDMSW.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="2ccf2-125">Процедура записи службы</span><span class="sxs-lookup"><span data-stu-id="2ccf2-125">Service Entry routine</span></span>

<span data-ttu-id="2ccf2-126">Функция **[MSGSERVICEENTRY](msgserviceentry.md)** — точка входа службы сообщений, где настроены оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="2ccf2-127">Вызовы функций `GetMemAllocRoutines()` для получения памяти MAPI процедуры управления.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="2ccf2-128">Использует функцию `lpProviderAdmin` параметр найдите раздел профиля для поставщика и наборов свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="2ccf2-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="2ccf2-129">Пример ServiceEntry()</span><span class="sxs-lookup"><span data-stu-id="2ccf2-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2ccf2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2ccf2-130">See also</span></span>

- [<span data-ttu-id="2ccf2-131">Сведения о примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="2ccf2-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2ccf2-132">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="2ccf2-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2ccf2-133">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="2ccf2-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2ccf2-134">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="2ccf2-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2ccf2-135">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="2ccf2-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

