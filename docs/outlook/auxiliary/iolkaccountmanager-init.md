---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетной записи для использования.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322038"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="4218b-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="4218b-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="4218b-104">Инициализирует диспетчер учетной записи для использования.</span><span class="sxs-lookup"><span data-stu-id="4218b-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4218b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4218b-105">Quick info</span></span>

<span data-ttu-id="4218b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="4218b-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="4218b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4218b-107">Parameters</span></span>

<span data-ttu-id="4218b-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="4218b-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="4218b-109">[in] Интерфейс [IOlkAccountHelper,](iolkaccounthelper.md) который предоставляет функции помощника учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4218b-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="4218b-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4218b-110">_dwFlags_</span></span>
  
> <span data-ttu-id="4218b-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="4218b-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="4218b-112">**ACCT_INIT_NO_STORES_CHECK** — предотвращает синхронизацию учетной записи (например, учетной записи IMAP) со связанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="4218b-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="4218b-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — предотвращает синхронизацию служб MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="4218b-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="4218b-114">**ACCT_INIT_NO_NOTIFICATIONS** — предотвращает перехват диспетчером учетных записей сообщений, предназначенных для других приложений.</span><span class="sxs-lookup"><span data-stu-id="4218b-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="4218b-115">**OLK_ACCOUNT_NO_FLAGS** — синхронизирует службы MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="4218b-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4218b-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4218b-116">Return values</span></span>

|<span data-ttu-id="4218b-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4218b-117">**HRESULT**</span></span>|<span data-ttu-id="4218b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4218b-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4218b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4218b-119">S_OK</span></span>  <br/> |<span data-ttu-id="4218b-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="4218b-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="4218b-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="4218b-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="4218b-122">**Init** уже был вызван.</span><span class="sxs-lookup"><span data-stu-id="4218b-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="4218b-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="4218b-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="4218b-124">Менеджер учетной записи не мог получить доступ к требуемой настройке реестра.</span><span class="sxs-lookup"><span data-stu-id="4218b-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4218b-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="4218b-125">Remarks</span></span>

<span data-ttu-id="4218b-126">Клиент должен вызвать **IOlkAccountManager:::Init,** чтобы инициализировать диспетчер учетной записи перед использованием диспетчера учетных записей для доступа к учетным записям или настройка уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4218b-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="4218b-127">Поскольку Outlook автоматически синхронизирует службы MAPI с учетными записями при запуске, используйте ACCT_INIT_NOSYNCH_MAPI_ACCTS, если нет конкретной причины для синхронизации. </span><span class="sxs-lookup"><span data-stu-id="4218b-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4218b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4218b-128">See also</span></span>

- [<span data-ttu-id="4218b-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="4218b-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

