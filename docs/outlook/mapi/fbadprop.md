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
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578852"
---
# <a name="fbadprop"></a><span data-ttu-id="d8acb-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="d8acb-103">FBadProp</span></span>

  
  
<span data-ttu-id="d8acb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8acb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8acb-105">Проверяет определенное свойство.</span><span class="sxs-lookup"><span data-stu-id="d8acb-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8acb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8acb-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8acb-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d8acb-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d8acb-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d8acb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8acb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8acb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8acb-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d8acb-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8acb-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d8acb-111">Service Providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="d8acb-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8acb-112">Parameters</span></span>

 <span data-ttu-id="d8acb-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="d8acb-113">_lpprop_</span></span>
  
> <span data-ttu-id="d8acb-114">[in] Структура [SPropValue](spropvalue.md) определяет свойство, которое необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="d8acb-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8acb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8acb-115">Return value</span></span>

<span data-ttu-id="d8acb-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d8acb-116">TRUE</span></span> 
  
> <span data-ttu-id="d8acb-117">Указанное свойство недопустимо.</span><span class="sxs-lookup"><span data-stu-id="d8acb-117">The specified property name is invalid.</span></span> 
    
<span data-ttu-id="d8acb-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d8acb-118">FALSE</span></span> 
  
> <span data-ttu-id="d8acb-119">Указанное свойство допустимо.</span><span class="sxs-lookup"><span data-stu-id="d8acb-119">The specified unit is not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8acb-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8acb-120">Remarks</span></span>

<span data-ttu-id="d8acb-121">Существует несколько причин для вызова функции **FBadProp** поставщиком услуг. Например, это может быть сделано для подготовки вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md), задающего свойство.</span><span class="sxs-lookup"><span data-stu-id="d8acb-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="d8acb-122">**FBadProp** выбирает ход проверки для указанного свойства в зависимости от его типа.</span><span class="sxs-lookup"><span data-stu-id="d8acb-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="d8acb-123">Например, если свойство является логическим, **FBadProp** необходимо убедиться, что ему присвоено одно из значений: TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="d8acb-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="d8acb-124">Для двоичных свойств **FBadProp** проверяет указатель, размер и правильность выделения.</span><span class="sxs-lookup"><span data-stu-id="d8acb-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8acb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d8acb-125">See also</span></span>



[<span data-ttu-id="d8acb-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="d8acb-126">FBadPropTag</span></span>](fbadproptag.md)

