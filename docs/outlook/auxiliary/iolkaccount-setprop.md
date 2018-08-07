---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Задает значение свойства указанной учетной записи.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807810"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="f2ed7-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="f2ed7-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="f2ed7-104">Задает значение свойства указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f2ed7-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f2ed7-105">Quick info</span></span>

<span data-ttu-id="f2ed7-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f2ed7-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="f2ed7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2ed7-107">Parameters</span></span>

<span data-ttu-id="f2ed7-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="f2ed7-108">_dwProp_</span></span>
  
> <span data-ttu-id="f2ed7-109">[in] Свойство tag свойства учетной записи для установки.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="f2ed7-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="f2ed7-110">_pVar_</span></span>
  
> <span data-ttu-id="f2ed7-111">[in] Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f2ed7-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f2ed7-112">Return values</span></span>

|<span data-ttu-id="f2ed7-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f2ed7-113">**HRESULT**</span></span>|<span data-ttu-id="f2ed7-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="f2ed7-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2ed7-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f2ed7-115">S_OK</span></span>  <br/> |<span data-ttu-id="f2ed7-116">Вызов метода прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="f2ed7-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f2ed7-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f2ed7-118">Указан недопустимый свойства тега.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2ed7-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2ed7-119">Remarks</span></span>

<span data-ttu-id="f2ed7-120">Используйте [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , чтобы сохранить изменения значений свойств учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f2ed7-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2ed7-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f2ed7-121">See also</span></span>

- [<span data-ttu-id="f2ed7-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f2ed7-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="f2ed7-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="f2ed7-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

