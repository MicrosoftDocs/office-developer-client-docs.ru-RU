---
title: иолкаккаунтнотифинотифи
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Уведомляет клиента об изменениях указанной учетной записи.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424569"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="3c4fc-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="3c4fc-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="3c4fc-104">Уведомляет клиента об изменениях указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c4fc-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3c4fc-105">Quick info</span></span>

<span data-ttu-id="3c4fc-106">Обратитесь к разделу [иолкаккаунтнотифи](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="3c4fc-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="3c4fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c4fc-107">Parameters</span></span>

<span data-ttu-id="3c4fc-108">_двнотифи_</span><span class="sxs-lookup"><span data-stu-id="3c4fc-108">_dwNotify_</span></span>
  
> <span data-ttu-id="3c4fc-109">возврата Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-109">[in] The type of notification.</span></span> <span data-ttu-id="3c4fc-110">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="3c4fc-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="3c4fc-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3c4fc-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="3c4fc-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="3c4fc-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="3c4fc-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="3c4fc-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="3c4fc-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3c4fc-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="3c4fc-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="3c4fc-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="3c4fc-116">_двакктид_</span><span class="sxs-lookup"><span data-stu-id="3c4fc-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="3c4fc-117">возврата Идентификатор учетной записи, которая была создана, изменена, удалена или предварительно удалена.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="3c4fc-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="3c4fc-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="3c4fc-119">возврата Не используется.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-119">[in] Not used.</span></span> <span data-ttu-id="3c4fc-120">OLK_ACCOUNT_NO_FLAGS является единственным поддерживаемым значением.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3c4fc-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3c4fc-121">Return values</span></span>

<span data-ttu-id="3c4fc-122">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="3c4fc-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3c4fc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="3c4fc-123">See also</span></span>

- [<span data-ttu-id="3c4fc-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="3c4fc-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="3c4fc-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="3c4fc-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

