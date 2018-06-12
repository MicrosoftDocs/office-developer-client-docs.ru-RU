---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Уведомляет клиента о изменения для указанной учетной записи.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807866"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="5a449-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="5a449-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="5a449-104">Уведомляет клиента о изменения для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5a449-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5a449-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5a449-105">Quick info</span></span>

<span data-ttu-id="5a449-106">В разделе [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="5a449-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="5a449-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a449-107">Parameters</span></span>

<span data-ttu-id="5a449-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="5a449-108">_dwNotify_</span></span>
  
> <span data-ttu-id="5a449-109">[in] Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="5a449-109">[in] The type of notification.</span></span> <span data-ttu-id="5a449-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="5a449-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="5a449-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5a449-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="5a449-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="5a449-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="5a449-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="5a449-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="5a449-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5a449-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="5a449-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="5a449-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="5a449-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="5a449-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="5a449-117">[in] Идентификатор учетной записи для учетной записи, которые были созданы, изменяется, удаления или предварительно удален.</span><span class="sxs-lookup"><span data-stu-id="5a449-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="5a449-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5a449-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="5a449-119">[in] Не используется.</span><span class="sxs-lookup"><span data-stu-id="5a449-119">[in] Not used.</span></span> <span data-ttu-id="5a449-120">OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение.</span><span class="sxs-lookup"><span data-stu-id="5a449-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5a449-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5a449-121">Return values</span></span>

<span data-ttu-id="5a449-122">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="5a449-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a449-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5a449-123">See also</span></span>

- [<span data-ttu-id="5a449-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="5a449-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="5a449-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="5a449-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

