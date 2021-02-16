---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Получает значение указанного свойства учетной записи.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433740"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="afdb8-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="afdb8-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="afdb8-104">Получает значение указанного свойства учетной записи.</span><span class="sxs-lookup"><span data-stu-id="afdb8-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="afdb8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="afdb8-105">Quick info</span></span>

<span data-ttu-id="afdb8-106">См. [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="afdb8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="afdb8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="afdb8-107">Parameters</span></span>

<span data-ttu-id="afdb8-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="afdb8-108">_dwProp_</span></span>
  
> <span data-ttu-id="afdb8-109">[in] Тег свойства свойства учетной записи, который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="afdb8-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="afdb8-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="afdb8-110">_pVar_</span></span>
  
> <span data-ttu-id="afdb8-111">[out] Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="afdb8-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="afdb8-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="afdb8-112">Return values</span></span>

|<span data-ttu-id="afdb8-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="afdb8-113">**HRESULT**</span></span>|<span data-ttu-id="afdb8-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="afdb8-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afdb8-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="afdb8-115">S_OK</span></span>  <br/> |<span data-ttu-id="afdb8-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="afdb8-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="afdb8-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="afdb8-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="afdb8-118">Свойство не найдено для данной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="afdb8-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="afdb8-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="afdb8-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="afdb8-120">Указан недопустимый тег свойства.</span><span class="sxs-lookup"><span data-stu-id="afdb8-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afdb8-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="afdb8-121">Remarks</span></span>

<span data-ttu-id="afdb8-122">Если свойство учетной записи имеет двоичный или строковый тип, то после возврата этого метода необходимо освободить *pVar* с помощью [IOlkAccount::FreeMemory.](iolkaccount-freememory.md)</span><span class="sxs-lookup"><span data-stu-id="afdb8-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="afdb8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="afdb8-123">See also</span></span>

- [<span data-ttu-id="afdb8-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="afdb8-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="afdb8-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="afdb8-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="afdb8-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="afdb8-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

