---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Получает порядок использования учетных записей в указанной категории.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807853"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="86b73-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="86b73-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="86b73-104">Получает порядок использования учетных записей в указанной категории.</span><span class="sxs-lookup"><span data-stu-id="86b73-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="86b73-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="86b73-105">Quick info</span></span>

<span data-ttu-id="86b73-106">Просмотреть [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="86b73-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="86b73-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="86b73-107">Parameters</span></span>

<span data-ttu-id="86b73-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="86b73-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="86b73-109">[in] Идентификатор класса категории, для которого необходимо получить порядке.</span><span class="sxs-lookup"><span data-stu-id="86b73-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="86b73-110">The value must be one of the following:</span><span class="sxs-lookup"><span data-stu-id="86b73-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="86b73-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="86b73-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="86b73-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="86b73-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="86b73-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="86b73-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="86b73-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="86b73-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="86b73-115">[out] Число учетных записей.</span><span class="sxs-lookup"><span data-stu-id="86b73-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="86b73-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="86b73-116">_prgAccts_</span></span>
  
> <span data-ttu-id="86b73-117">[out] Указатель на массив учетных записей.</span><span class="sxs-lookup"><span data-stu-id="86b73-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="86b73-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="86b73-118">Return values</span></span>

|<span data-ttu-id="86b73-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="86b73-119">**HRESULT**</span></span>|<span data-ttu-id="86b73-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="86b73-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86b73-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="86b73-121">S_OK</span></span>  <br/> |<span data-ttu-id="86b73-122">Вызов успешно завершен</span><span class="sxs-lookup"><span data-stu-id="86b73-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="86b73-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="86b73-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="86b73-124">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="86b73-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="86b73-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="86b73-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="86b73-126">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="86b73-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86b73-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="86b73-127">Remarks</span></span>

<span data-ttu-id="86b73-128">Прежде чем вызывать этот метод, вызывающего выделяет только массива указатель *prgAccts* , но не памяти для массива, на который указывает *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="86b73-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="86b73-129">После этот метод возвращает, вызывающего необходимо использовать [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) для освобождения памяти, выделенной для *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="86b73-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86b73-130">См. также</span><span class="sxs-lookup"><span data-stu-id="86b73-130">See also</span></span>

- [<span data-ttu-id="86b73-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="86b73-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="86b73-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="86b73-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

