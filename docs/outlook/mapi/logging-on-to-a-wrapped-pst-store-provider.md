---
title: Вход в систему поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Последнее изменение: 02 июля 2012 г.'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408988"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="ffb94-103">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="ffb94-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="ffb94-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffb94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffb94-105">Прежде чем войти в MAPI к поставщику магазинов PST, необходимо инициализировать и настроить поставщика магазина файлов персональных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="ffb94-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="ffb94-106">Дополнительные сведения см. в [инициализации поставщика магазинов PST.](initializing-a-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ffb94-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="ffb94-107">После инициализации и настройки поставщика магазина PST необходимо реализовать две процедуры логона.</span><span class="sxs-lookup"><span data-stu-id="ffb94-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="ffb94-108">Журнал **[функции IMSProvider::Logon](imsprovider-logon.md)** в MAPI поставщику магазина PST.</span><span class="sxs-lookup"><span data-stu-id="ffb94-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="ffb94-109">Функции **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** войдите в spooler MAPI поставщику магазина PST.</span><span class="sxs-lookup"><span data-stu-id="ffb94-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="ffb94-110">В этом разделе функция **IMSProvider::Logon** и **функция IMSProvider::SpoolerLogon** демонстрируются с помощью примеров кода из поставщика магазина PST Sample Wrapped.</span><span class="sxs-lookup"><span data-stu-id="ffb94-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="ffb94-111">В примере реализован завернутый поставщик PST, который предназначен для использования в сочетании с API репликации.</span><span class="sxs-lookup"><span data-stu-id="ffb94-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="ffb94-112">Дополнительные сведения о загрузке и установке поставщика магазинов PST sample wrapped см. в примере Установки поставщика упаковки [PST Store.](installing-the-sample-wrapped-pst-store-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ffb94-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="ffb94-113">Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="ffb94-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="ffb94-114">После входа MAPI и пульпера MAPI в поставщик магазина PST, он готов к его использования.</span><span class="sxs-lookup"><span data-stu-id="ffb94-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="ffb94-115">Дополнительные сведения см. [в дополнительных сведениях Об](using-a-wrapped-pst-store-provider.md)использовании поставщика магазина PST.</span><span class="sxs-lookup"><span data-stu-id="ffb94-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="ffb94-116">MapI Logon routine</span><span class="sxs-lookup"><span data-stu-id="ffb94-116">MAPI Logon routine</span></span>

<span data-ttu-id="ffb94-117">После инициализации поставщика магазина PST необходимо реализовать функцию **[IMSProvider::Logon,](imsprovider-logon.md)** чтобы войти в MAPI в завернутый магазин PST.</span><span class="sxs-lookup"><span data-stu-id="ffb94-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="ffb94-118">Эта функция проверяет учетные данные пользователей и получает свойства конфигурации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffb94-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="ffb94-119">Необходимо также реализовать функцию, чтобы установить сведения о автономных `SetOLFIInOST` файлах **[(OLFI).](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="ffb94-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="ffb94-120">**OLFI** — это очередь долгосрочных структур ID, которая используется поставщиком магазина PST для назначения ID входа для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ffb94-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="ffb94-121">Наконец, функция **IMSProvider::Logon** возвращает объект магазина сообщений, в который могут войти пуллер MAPI и клиентские приложения в  `ppMDB` параметре.</span><span class="sxs-lookup"><span data-stu-id="ffb94-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="ffb94-122">Пример CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="ffb94-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="ffb94-123">MapI Spooler Logon routine</span><span class="sxs-lookup"><span data-stu-id="ffb94-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="ffb94-124">Как и **в IMSProvider::Logon,** необходимо реализовать функцию **[IMSProvider::SpoolerLogon,](imsprovider-spoolerlogon.md)** чтобы войти в пульпер MAPI в завернутый магазин PST.</span><span class="sxs-lookup"><span data-stu-id="ffb94-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="ffb94-125">В параметре возвращается объект хранения сообщений, в который могут войти шпалер MAPI и клиентские  `ppMDB` приложения.</span><span class="sxs-lookup"><span data-stu-id="ffb94-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="ffb94-126">ПРИМЕР CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="ffb94-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="ffb94-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ffb94-127">See also</span></span>

- [<span data-ttu-id="ffb94-128">О поставщике пакетных пакетов PST Store</span><span class="sxs-lookup"><span data-stu-id="ffb94-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="ffb94-129">Установка поставщика пакетных пакетов PST</span><span class="sxs-lookup"><span data-stu-id="ffb94-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="ffb94-130">Инициализация поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="ffb94-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ffb94-131">Использование поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="ffb94-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="ffb94-132">Отключение поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="ffb94-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

