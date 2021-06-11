---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Сохраняет изменения в указанной учетной записи.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429609"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="9a602-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9a602-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="9a602-104">Сохраняет изменения в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a602-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9a602-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9a602-105">Quick info</span></span>

<span data-ttu-id="9a602-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="9a602-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="9a602-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9a602-107">Parameters</span></span>

<span data-ttu-id="9a602-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="9a602-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="9a602-109">[in] ID учетной записи для сохранения.</span><span class="sxs-lookup"><span data-stu-id="9a602-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="9a602-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="9a602-110">_dwFlags_</span></span>
  
> <span data-ttu-id="9a602-111">[in] Flags to modify behavior.</span><span class="sxs-lookup"><span data-stu-id="9a602-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="9a602-112">OLK_ACCOUNT_NO_FLAGS является единственным поддерживаемым значением.</span><span class="sxs-lookup"><span data-stu-id="9a602-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9a602-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9a602-113">Return values</span></span>

|<span data-ttu-id="9a602-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a602-114">**HRESULT**</span></span>|<span data-ttu-id="9a602-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a602-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a602-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a602-116">S_OK</span></span>  <br/> |<span data-ttu-id="9a602-117">Вызов удался</span><span class="sxs-lookup"><span data-stu-id="9a602-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="9a602-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9a602-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="9a602-119">Указанную учетную запись невозможно найти.</span><span class="sxs-lookup"><span data-stu-id="9a602-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="9a602-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9a602-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="9a602-121">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="9a602-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a602-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a602-122">Remarks</span></span>

<span data-ttu-id="9a602-123">После изменения значения свойств учетных записей с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md)используйте **IOlkAccountManager::SaveChanges** или [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) для сохранения таких изменений.</span><span class="sxs-lookup"><span data-stu-id="9a602-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a602-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9a602-124">See also</span></span>

- [<span data-ttu-id="9a602-125">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="9a602-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="9a602-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9a602-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

