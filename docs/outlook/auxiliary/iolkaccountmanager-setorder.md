---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Изменяет порядок использования учетных записей в указанной категории.
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807849"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="b590c-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="b590c-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="b590c-104">Изменяет порядок использования учетных записей в указанной категории.</span><span class="sxs-lookup"><span data-stu-id="b590c-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b590c-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b590c-105">Quick info</span></span>

<span data-ttu-id="b590c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b590c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="b590c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b590c-107">Parameters</span></span>

<span data-ttu-id="b590c-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="b590c-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="b590c-109">[in] КОД класса категории, для которого необходимо задать порядок.</span><span class="sxs-lookup"><span data-stu-id="b590c-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="b590c-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="b590c-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b590c-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="b590c-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="b590c-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="b590c-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="b590c-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="b590c-113">_cAccts_</span></span>
  
> <span data-ttu-id="b590c-114">[in] Число учетных записей.</span><span class="sxs-lookup"><span data-stu-id="b590c-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="b590c-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="b590c-115">_rgAccts_</span></span>
  
> <span data-ttu-id="b590c-116">[in] Массив идентификаторов учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b590c-116">[in] An array of account IDs.</span></span> <span data-ttu-id="b590c-117">Размер массива — _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="b590c-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b590c-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b590c-118">Return values</span></span>

|<span data-ttu-id="b590c-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b590c-119">**HRESULT**</span></span>|<span data-ttu-id="b590c-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="b590c-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b590c-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b590c-121">S_OK</span></span>  <br/> |<span data-ttu-id="b590c-122">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="b590c-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b590c-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="b590c-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="b590c-124">Порядок сортировки имеет ряд различных учетных записей более старые порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="b590c-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="b590c-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b590c-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b590c-126">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="b590c-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="b590c-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b590c-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b590c-128">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="b590c-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b590c-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="b590c-129">Remarks</span></span>

<span data-ttu-id="b590c-130">Звонящий выделение памяти для массива указатель _prgAccts_ , а также для массива, на который указывает _prgAccts_ .</span><span class="sxs-lookup"><span data-stu-id="b590c-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b590c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b590c-131">See also</span></span>

- [<span data-ttu-id="b590c-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="b590c-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b590c-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="b590c-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

