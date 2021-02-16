---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает порядок указанной категории учетных записей.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424625"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="c0cb9-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="c0cb9-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="c0cb9-104">Получает порядок указанной категории учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c0cb9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c0cb9-105">Quick info</span></span>

<span data-ttu-id="c0cb9-106">См. [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="c0cb9-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="c0cb9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0cb9-107">Parameters</span></span>

<span data-ttu-id="c0cb9-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="c0cb9-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="c0cb9-109">[in] ИД класса категории, для которого требуется получить заказ.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="c0cb9-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="c0cb9-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="c0cb9-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="c0cb9-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="c0cb9-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="c0cb9-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="c0cb9-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="c0cb9-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="c0cb9-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="c0cb9-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="c0cb9-115">[out] Количество учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="c0cb9-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="c0cb9-116">_prgAccts_</span></span>
  
> <span data-ttu-id="c0cb9-117">[out] Указатель на массив учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c0cb9-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c0cb9-118">Return values</span></span>

|<span data-ttu-id="c0cb9-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c0cb9-119">**HRESULT**</span></span>|<span data-ttu-id="c0cb9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0cb9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0cb9-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0cb9-121">S_OK</span></span>  <br/> |<span data-ttu-id="c0cb9-122">Вызов был успешным</span><span class="sxs-lookup"><span data-stu-id="c0cb9-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="c0cb9-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c0cb9-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="c0cb9-124">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="c0cb9-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c0cb9-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c0cb9-126">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="c0cb9-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0cb9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0cb9-127">Remarks</span></span>

<span data-ttu-id="c0cb9-128">Перед вызовом этого метода вызываемая точка выделяет только *prgAccts* указателя массива, но память для массива, на котором *указывает prgAccts.*</span><span class="sxs-lookup"><span data-stu-id="c0cb9-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="c0cb9-129">После возврата этого метода звонящего необходимо использовать [IOlkAccountManager::FreeMemory,](iolkaccountmanager-freememory.md) чтобы освободить память, выделенную *для prgAccts.*</span><span class="sxs-lookup"><span data-stu-id="c0cb9-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0cb9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c0cb9-130">See also</span></span>

- [<span data-ttu-id="c0cb9-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="c0cb9-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c0cb9-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="c0cb9-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

