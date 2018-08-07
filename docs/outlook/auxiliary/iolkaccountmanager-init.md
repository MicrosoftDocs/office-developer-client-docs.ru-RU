---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетных записей для использования.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807843"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="e56e0-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="e56e0-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="e56e0-104">Инициализирует диспетчер учетных записей для использования.</span><span class="sxs-lookup"><span data-stu-id="e56e0-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e56e0-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e56e0-105">Quick info</span></span>

<span data-ttu-id="e56e0-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="e56e0-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="e56e0-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e56e0-107">Parameters</span></span>

<span data-ttu-id="e56e0-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="e56e0-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="e56e0-109">[in] Интерфейс [IOlkAccountHelper](iolkaccounthelper.md) , предоставляющая функциональные возможности модуля поддержки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e56e0-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="e56e0-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e56e0-110">_dwFlags_</span></span>
  
> <span data-ttu-id="e56e0-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="e56e0-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="e56e0-112">**ACCT_INIT_NO_STORES_CHECK** — запрещает синхронизацию с связанного хранилища учетной записи (например, учетной записи IMAP).</span><span class="sxs-lookup"><span data-stu-id="e56e0-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="e56e0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — служб MAPI, не позволяет синхронизировать с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="e56e0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="e56e0-114">**OLK_ACCOUNT_NO_FLAGS** — служб MAPI синхронизируется с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="e56e0-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e56e0-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e56e0-115">Return values</span></span>

|<span data-ttu-id="e56e0-116">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e56e0-116">**HRESULT**</span></span>|<span data-ttu-id="e56e0-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="e56e0-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e56e0-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e56e0-118">S_OK</span></span>  <br/> |<span data-ttu-id="e56e0-119">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="e56e0-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e56e0-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e56e0-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e56e0-121">Уже был вызван **init** .</span><span class="sxs-lookup"><span data-stu-id="e56e0-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="e56e0-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="e56e0-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="e56e0-123">Диспетчер учетных записей не удалось получить доступ к требуемые разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="e56e0-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e56e0-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="e56e0-124">Remarks</span></span>

<span data-ttu-id="e56e0-125">Клиента необходимо вызвать **IOlkAccountManager::Init** для инициализации учетной записи диспетчера перед использованием диспетчера учетной записи для доступа к учетных записей или настроить уведомления.</span><span class="sxs-lookup"><span data-stu-id="e56e0-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="e56e0-126">Так как Outlook автоматически синхронизирует служб MAPI с учетных записей при загрузке системы, используйте **ACCT_INIT_NOSYNCH_MAPI_ACCTS** при отсутствии определенных причина для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e56e0-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e56e0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e56e0-127">See also</span></span>

- [<span data-ttu-id="e56e0-128">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="e56e0-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

