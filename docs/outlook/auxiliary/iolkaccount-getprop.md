---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Получает значение свойства указанной учетной записи.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807793"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="78559-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="78559-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="78559-104">Получает значение свойства указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78559-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="78559-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="78559-105">Quick info</span></span>

<span data-ttu-id="78559-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="78559-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="78559-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="78559-107">Parameters</span></span>

<span data-ttu-id="78559-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="78559-108">_dwProp_</span></span>
  
> <span data-ttu-id="78559-109">[in] Свойство tag свойства учетной записи для получения.</span><span class="sxs-lookup"><span data-stu-id="78559-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="78559-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="78559-110">_pVar_</span></span>
  
> <span data-ttu-id="78559-111">[out] Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="78559-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="78559-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="78559-112">Return values</span></span>

|<span data-ttu-id="78559-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78559-113">**HRESULT**</span></span>|<span data-ttu-id="78559-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="78559-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78559-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="78559-115">S_OK</span></span>  <br/> |<span data-ttu-id="78559-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="78559-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="78559-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="78559-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="78559-118">Свойство не найдено для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78559-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="78559-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="78559-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="78559-120">Был указан недопустимый свойства тега.</span><span class="sxs-lookup"><span data-stu-id="78559-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78559-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="78559-121">Remarks</span></span>

<span data-ttu-id="78559-122">После этого метода значение, если значение свойства учетной записи — это двоичный файл или строковый тип, необходимо освободить *pVar* с помощью [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="78559-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78559-123">См. также</span><span class="sxs-lookup"><span data-stu-id="78559-123">See also</span></span>

- [<span data-ttu-id="78559-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="78559-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="78559-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="78559-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="78559-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="78559-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

