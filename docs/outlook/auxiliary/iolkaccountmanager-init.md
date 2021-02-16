---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетных записей для использования.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322038"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="285bd-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="285bd-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="285bd-104">Инициализирует диспетчер учетных записей для использования.</span><span class="sxs-lookup"><span data-stu-id="285bd-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="285bd-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="285bd-105">Quick info</span></span>

<span data-ttu-id="285bd-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="285bd-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="285bd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="285bd-107">Parameters</span></span>

<span data-ttu-id="285bd-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="285bd-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="285bd-109">[in] Интерфейс [IOlkAccountHelper,](iolkaccounthelper.md) который предоставляет дополнительные функции учетной записи.</span><span class="sxs-lookup"><span data-stu-id="285bd-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="285bd-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="285bd-110">_dwFlags_</span></span>
  
> <span data-ttu-id="285bd-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="285bd-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="285bd-112">**ACCT_INIT_NO_STORES_CHECK** – предотвращает синхронизацию учетной записи (например, учетной записи IMAP) со связанным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="285bd-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="285bd-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** – предотвращает синхронизацию служб MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="285bd-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="285bd-114">**ACCT_INIT_NO_NOTIFICATIONS** - предотвращает перехват диспетчером учетных записей сообщений вещания, предназначенных для других приложений.</span><span class="sxs-lookup"><span data-stu-id="285bd-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="285bd-115">**OLK_ACCOUNT_NO_FLAGS** синхронизирует службы MAPI с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="285bd-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="285bd-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="285bd-116">Return values</span></span>

|<span data-ttu-id="285bd-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="285bd-117">**HRESULT**</span></span>|<span data-ttu-id="285bd-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="285bd-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="285bd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="285bd-119">S_OK</span></span>  <br/> |<span data-ttu-id="285bd-120">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="285bd-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="285bd-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="285bd-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="285bd-122">**Init** has already been called.</span><span class="sxs-lookup"><span data-stu-id="285bd-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="285bd-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="285bd-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="285bd-124">Диспетчеру учетных записей не удалось получить доступ к требуемой настройке реестра.</span><span class="sxs-lookup"><span data-stu-id="285bd-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="285bd-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="285bd-125">Remarks</span></span>

<span data-ttu-id="285bd-126">Клиент должен вызвать **IOlkAccountManager::Init,** чтобы инициализировать диспетчер учетных записей, прежде чем использовать диспетчер учетных записей для доступа к учетным записям или настроить уведомления.</span><span class="sxs-lookup"><span data-stu-id="285bd-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="285bd-127">Так как Outlook автоматически синхронизирует службы MAPI с учетными записями при запуске, используйте ACCT_INIT_NOSYNCH_MAPI_ACCTS, если нет особой причины для синхронизации. </span><span class="sxs-lookup"><span data-stu-id="285bd-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="285bd-128">См. также</span><span class="sxs-lookup"><span data-stu-id="285bd-128">See also</span></span>

- [<span data-ttu-id="285bd-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="285bd-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

