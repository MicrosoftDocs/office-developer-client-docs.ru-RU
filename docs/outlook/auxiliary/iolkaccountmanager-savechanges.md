---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Сохраняет изменения указанной учетной записи.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807861"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="f2962-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f2962-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="f2962-104">Сохраняет изменения указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f2962-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f2962-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f2962-105">Quick info</span></span>

<span data-ttu-id="f2962-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f2962-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="f2962-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2962-107">Parameters</span></span>

<span data-ttu-id="f2962-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="f2962-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="f2962-109">[in] Идентификатор учетной записи, чтобы сохранить.</span><span class="sxs-lookup"><span data-stu-id="f2962-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="f2962-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f2962-110">_dwFlags_</span></span>
  
> <span data-ttu-id="f2962-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="f2962-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="f2962-112">OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение.</span><span class="sxs-lookup"><span data-stu-id="f2962-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f2962-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f2962-113">Return values</span></span>

|<span data-ttu-id="f2962-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2962-114">**HRESULT**</span></span>|<span data-ttu-id="f2962-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f2962-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2962-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f2962-116">S_OK</span></span>  <br/> |<span data-ttu-id="f2962-117">Вызов успешно завершен</span><span class="sxs-lookup"><span data-stu-id="f2962-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="f2962-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f2962-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="f2962-119">Не удается найти указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f2962-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="f2962-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f2962-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f2962-121">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="f2962-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2962-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2962-122">Remarks</span></span>

<span data-ttu-id="f2962-123">После изменения значения свойства учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md), используйте **IOlkAccountManager::SaveChanges** или [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) для сохранения такие изменения.</span><span class="sxs-lookup"><span data-stu-id="f2962-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2962-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f2962-124">See also</span></span>

- [<span data-ttu-id="f2962-125">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f2962-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="f2962-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f2962-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

