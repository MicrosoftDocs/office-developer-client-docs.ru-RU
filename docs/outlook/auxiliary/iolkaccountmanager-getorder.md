---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает упорядочение указанной категории учетных записей.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424625"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="7bb4e-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="7bb4e-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="7bb4e-104">Получает упорядочение указанной категории учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7bb4e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7bb4e-105">Quick info</span></span>

<span data-ttu-id="7bb4e-106">См. [в окне IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="7bb4e-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="7bb4e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="7bb4e-107">Parameters</span></span>

<span data-ttu-id="7bb4e-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="7bb4e-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="7bb4e-109">[in] ID класса категории, для которого необходимо получить заказ.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="7bb4e-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="7bb4e-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="7bb4e-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="7bb4e-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="7bb4e-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="7bb4e-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="7bb4e-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="7bb4e-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="7bb4e-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="7bb4e-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="7bb4e-115">[вышел] Количество учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="7bb4e-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="7bb4e-116">_prgAccts_</span></span>
  
> <span data-ttu-id="7bb4e-117">[вышел] Указатель на массив учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7bb4e-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7bb4e-118">Return values</span></span>

|<span data-ttu-id="7bb4e-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7bb4e-119">**HRESULT**</span></span>|<span data-ttu-id="7bb4e-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="7bb4e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bb4e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bb4e-121">S_OK</span></span>  <br/> |<span data-ttu-id="7bb4e-122">Вызов удался</span><span class="sxs-lookup"><span data-stu-id="7bb4e-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="7bb4e-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7bb4e-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="7bb4e-124">Один или несколько аргументов являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="7bb4e-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7bb4e-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7bb4e-126">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="7bb4e-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bb4e-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7bb4e-127">Remarks</span></span>

<span data-ttu-id="7bb4e-128">Перед вызовом этого метода вызываемая компания выделяет только *prgAccts* указателя массива, но не имеет памяти для массива, на котором *указывает prgAccts.*</span><span class="sxs-lookup"><span data-stu-id="7bb4e-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="7bb4e-129">После возвращения этого метода звонящего необходимо использовать [IOlkAccountManager::FreeMemory,](iolkaccountmanager-freememory.md) чтобы освободить память, выделенную *для prgAccts.*</span><span class="sxs-lookup"><span data-stu-id="7bb4e-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bb4e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7bb4e-130">See also</span></span>

- [<span data-ttu-id="7bb4e-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="7bb4e-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="7bb4e-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="7bb4e-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

