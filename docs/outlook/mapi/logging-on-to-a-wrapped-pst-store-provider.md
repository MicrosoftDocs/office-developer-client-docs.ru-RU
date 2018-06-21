---
title: Вход в систему на оболочку поставщик хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 2dfa3820d8d2ab57f278e90bef5d5a40164da6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19809647"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="71f04-103">Вход в систему на оболочку поставщик хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="71f04-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71f04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71f04-105">Чтобы выполнить вход на MAPI оболочку поставщика хранилища PST-файлов, необходимо инициализировать и настроить оболочку поставщика хранилища личных папок (PST) файла.</span><span class="sxs-lookup"><span data-stu-id="71f04-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="71f04-106">Для получения дополнительных сведений см. [В оболочку поставщика хранилища PST -файлов](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="71f04-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="71f04-107">После инициализации и настройки оболочку поставщика хранилища PST-файлов необходимо реализовать две процедуры входа в систему.</span><span class="sxs-lookup"><span data-stu-id="71f04-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="71f04-108">Функция **[IMSProvider::Logon](imsprovider-logon.md)** входит MAPI оболочку поставщика хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="71f04-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="71f04-109">Функция **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** входит в систему диспетчер очереди MAPI на оболочку поставщик хранилища PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="71f04-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="71f04-110">В этом разделе функции **IMSProvider::Logon** и **IMSProvider::SpoolerLogon** демонстрируются с помощью примеров кода с переносом PST поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="71f04-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="71f04-111">В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации.</span><span class="sxs-lookup"><span data-stu-id="71f04-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="71f04-112">Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см.</span><span class="sxs-lookup"><span data-stu-id="71f04-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="71f04-113">Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="71f04-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="71f04-114">После входа MAPI и диспетчер очереди MAPI на оболочку PST хранилища поставщика, его можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="71f04-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="71f04-115">[Оболочку поставщика хранилища PST -файлов](using-a-wrapped-pst-store-provider.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="71f04-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="71f04-116">Процедура входа в систему MAPI</span><span class="sxs-lookup"><span data-stu-id="71f04-116">MAPI Logon routine</span></span>

<span data-ttu-id="71f04-117">После инициализации оболочку поставщика хранилища PST-файлов, необходимо реализовать функцию **[IMSProvider::Logon](imsprovider-logon.md)** для входа на MAPI оболочку PST-хранилище.</span><span class="sxs-lookup"><span data-stu-id="71f04-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="71f04-118">Эта функция проверяет учетные данные пользователя и получает свойства конфигурации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="71f04-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="71f04-119">Кроме того, необходимо реализовать `SetOLFIInOST` функцию, чтобы задать автономный режим сведения о файле (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="71f04-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="71f04-120">**OLFI** — это очереди долгосрочного структур идентификатор, используемый поставщиком хранилища оболочку PST-файлов для назначения идентификатор записи для нового сообщения или папки в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="71f04-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="71f04-121">И, наконец, функция **IMSProvider::Logon** возвращает объект хранилища сообщений, очереди и клиентских приложений MAPI может входить в `ppMDB` параметр.</span><span class="sxs-lookup"><span data-stu-id="71f04-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="71f04-122">Пример CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="71f04-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="71f04-123">Процедура входа в систему очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="71f04-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="71f04-124">Как и **IMSProvider::Logon**, необходимо реализовать функцию **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** для записи в журнал очереди MAPI на оболочку PST-хранилище.</span><span class="sxs-lookup"><span data-stu-id="71f04-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="71f04-125">Объект хранилища сообщений, очереди и клиентских приложений MAPI могут войти на возвращается в `ppMDB` параметр.</span><span class="sxs-lookup"><span data-stu-id="71f04-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="71f04-126">Пример CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="71f04-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="71f04-127">См. также</span><span class="sxs-lookup"><span data-stu-id="71f04-127">See also</span></span>

- [<span data-ttu-id="71f04-128">О примере оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="71f04-129">Установка примера оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="71f04-130">Инициализация поставщика оболочку хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="71f04-131">С помощью поставщика оболочку хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="71f04-132">Завершение работы поставщика оболочку хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="71f04-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

