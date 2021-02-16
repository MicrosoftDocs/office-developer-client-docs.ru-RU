---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Изменяет порядок указанной категории учетных записей.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422861"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="3130e-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="3130e-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="3130e-104">Изменяет порядок указанной категории учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3130e-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3130e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3130e-105">Quick info</span></span>

<span data-ttu-id="3130e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="3130e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="3130e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3130e-107">Parameters</span></span>

<span data-ttu-id="3130e-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="3130e-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="3130e-109">[in] ИД класса категории, для которого необходимо установить порядок.</span><span class="sxs-lookup"><span data-stu-id="3130e-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="3130e-110">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="3130e-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="3130e-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="3130e-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="3130e-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="3130e-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="3130e-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="3130e-113">_cAccts_</span></span>
  
> <span data-ttu-id="3130e-114">[in] Количество учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3130e-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="3130e-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="3130e-115">_rgAccts_</span></span>
  
> <span data-ttu-id="3130e-116">[in] Массив ИД учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3130e-116">[in] An array of account IDs.</span></span> <span data-ttu-id="3130e-117">Размер массива — _cAccts._</span><span class="sxs-lookup"><span data-stu-id="3130e-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="3130e-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3130e-118">Return values</span></span>

|<span data-ttu-id="3130e-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3130e-119">**HRESULT**</span></span>|<span data-ttu-id="3130e-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="3130e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3130e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3130e-121">S_OK</span></span>  <br/> |<span data-ttu-id="3130e-122">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="3130e-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="3130e-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="3130e-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="3130e-124">Новый порядок сортировки имеет другое количество учетных записей, чем старый порядок сортировки.</span><span class="sxs-lookup"><span data-stu-id="3130e-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="3130e-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3130e-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="3130e-126">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="3130e-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="3130e-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="3130e-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="3130e-128">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="3130e-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3130e-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="3130e-129">Remarks</span></span>

<span data-ttu-id="3130e-130">Вызываемая точка выделяет память для _prgAccts_ указателя массива, а также для массива, на котором _указывает prgAccts._</span><span class="sxs-lookup"><span data-stu-id="3130e-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3130e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3130e-131">See also</span></span>

- [<span data-ttu-id="3130e-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="3130e-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="3130e-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="3130e-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

