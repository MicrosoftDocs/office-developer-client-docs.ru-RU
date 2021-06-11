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
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="588c9-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="588c9-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="588c9-104">Изменяет порядок указанной категории учетных записей.</span><span class="sxs-lookup"><span data-stu-id="588c9-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="588c9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="588c9-105">Quick info</span></span>

<span data-ttu-id="588c9-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="588c9-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="588c9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="588c9-107">Parameters</span></span>

<span data-ttu-id="588c9-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="588c9-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="588c9-109">[in] ID класса категории, для которого необходимо установить порядок.</span><span class="sxs-lookup"><span data-stu-id="588c9-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="588c9-110">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="588c9-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="588c9-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="588c9-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="588c9-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="588c9-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="588c9-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="588c9-113">_cAccts_</span></span>
  
> <span data-ttu-id="588c9-114">[in] Количество учетных записей.</span><span class="sxs-lookup"><span data-stu-id="588c9-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="588c9-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="588c9-115">_rgAccts_</span></span>
  
> <span data-ttu-id="588c9-116">[in] Массив ID учетных записей.</span><span class="sxs-lookup"><span data-stu-id="588c9-116">[in] An array of account IDs.</span></span> <span data-ttu-id="588c9-117">Размер массива _— cAccts._</span><span class="sxs-lookup"><span data-stu-id="588c9-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="588c9-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="588c9-118">Return values</span></span>

|<span data-ttu-id="588c9-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="588c9-119">**HRESULT**</span></span>|<span data-ttu-id="588c9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="588c9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="588c9-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="588c9-121">S_OK</span></span>  <br/> |<span data-ttu-id="588c9-122">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="588c9-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="588c9-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="588c9-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="588c9-124">Новый порядок сортировки имеет другое количество учетных записей, чем старый.</span><span class="sxs-lookup"><span data-stu-id="588c9-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="588c9-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="588c9-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="588c9-126">Один или несколько аргументов являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="588c9-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="588c9-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="588c9-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="588c9-128">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="588c9-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="588c9-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="588c9-129">Remarks</span></span>

<span data-ttu-id="588c9-130">Вызыватель выделяет память для _prgAccts_ указателя массива, а также массива, на котором _указывает prgAccts._</span><span class="sxs-lookup"><span data-stu-id="588c9-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="588c9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="588c9-131">See also</span></span>

- [<span data-ttu-id="588c9-132">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="588c9-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="588c9-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="588c9-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

