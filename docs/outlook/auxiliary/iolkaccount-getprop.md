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
# <a name="iolkaccountgetprop"></a><span data-ttu-id="75f03-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="75f03-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="75f03-104">Получает значение указанного свойства учетной записи.</span><span class="sxs-lookup"><span data-stu-id="75f03-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="75f03-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="75f03-105">Quick info</span></span>

<span data-ttu-id="75f03-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="75f03-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="75f03-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="75f03-107">Parameters</span></span>

<span data-ttu-id="75f03-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="75f03-108">_dwProp_</span></span>
  
> <span data-ttu-id="75f03-109">[in] Тег свойства свойства свойства учетной записи, который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="75f03-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="75f03-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="75f03-110">_pVar_</span></span>
  
> <span data-ttu-id="75f03-111">[вышел] Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="75f03-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="75f03-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="75f03-112">Return values</span></span>

|<span data-ttu-id="75f03-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75f03-113">**HRESULT**</span></span>|<span data-ttu-id="75f03-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="75f03-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75f03-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="75f03-115">S_OK</span></span>  <br/> |<span data-ttu-id="75f03-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="75f03-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="75f03-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="75f03-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="75f03-118">Свойство не найдено для данной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="75f03-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="75f03-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="75f03-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="75f03-120">Указан недействительный тег свойства.</span><span class="sxs-lookup"><span data-stu-id="75f03-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75f03-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="75f03-121">Remarks</span></span>

<span data-ttu-id="75f03-122">После возвращения этого метода, если значение свойства учетной записи двоичного или строкового типа, вы должны освободить  *pVar*  с помощью [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="75f03-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75f03-123">См. также</span><span class="sxs-lookup"><span data-stu-id="75f03-123">See also</span></span>

- [<span data-ttu-id="75f03-124">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="75f03-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="75f03-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="75f03-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="75f03-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="75f03-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

