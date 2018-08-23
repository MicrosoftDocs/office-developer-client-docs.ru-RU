---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578852"
---
# <a name="fbadprop"></a><span data-ttu-id="f3dd5-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f3dd5-103">FBadProp</span></span>

  
  
<span data-ttu-id="f3dd5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3dd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3dd5-105">Проверяет указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3dd5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f3dd5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3dd5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f3dd5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f3dd5-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f3dd5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f3dd5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f3dd5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f3dd5-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f3dd5-110">Called by:</span></span>  <br/> |<span data-ttu-id="f3dd5-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="f3dd5-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="f3dd5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3dd5-112">Parameters</span></span>

 <span data-ttu-id="f3dd5-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="f3dd5-113">_lpprop_</span></span>
  
> <span data-ttu-id="f3dd5-114">[in] Структура [SPropValue](spropvalue.md) , определение свойства для проверки.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3dd5-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f3dd5-115">Return value</span></span>

<span data-ttu-id="f3dd5-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="f3dd5-116">TRUE</span></span> 
  
> <span data-ttu-id="f3dd5-117">Указанное свойство является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="f3dd5-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="f3dd5-118">FALSE</span></span> 
  
> <span data-ttu-id="f3dd5-119">Указанное свойство является допустимым.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3dd5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f3dd5-120">Remarks</span></span>

<span data-ttu-id="f3dd5-121">Поставщик службы можно вызвать функцию **FBadProp** по ряду причин, например подготовить для вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md) , задав свойство.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="f3dd5-122">**FBadProp** проверяет указанное свойство в зависимости от типа свойства.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="f3dd5-123">Например, если свойство имеет логическое значение, **FBadProp** сделать sures, что его значением является либо TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="f3dd5-124">Если свойство имеет двоичный, **FBadProp** проверяет его указатель и размер и следит за тем, что он правильно выделенное.</span><span class="sxs-lookup"><span data-stu-id="f3dd5-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3dd5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f3dd5-125">See also</span></span>



[<span data-ttu-id="f3dd5-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="f3dd5-126">FBadPropTag</span></span>](fbadproptag.md)

