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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426718"
---
# <a name="fbadprop"></a><span data-ttu-id="93337-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="93337-103">FBadProp</span></span>

  
  
<span data-ttu-id="93337-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93337-105">Проверяет определенное свойство.</span><span class="sxs-lookup"><span data-stu-id="93337-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93337-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="93337-106">Header file:</span></span>  <br/> |<span data-ttu-id="93337-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="93337-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="93337-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="93337-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93337-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93337-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93337-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="93337-110">Called by:</span></span>  <br/> |<span data-ttu-id="93337-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="93337-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="93337-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="93337-112">Parameters</span></span>

 <span data-ttu-id="93337-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="93337-113">_lpprop_</span></span>
  
> <span data-ttu-id="93337-114">[in] Структура [SPropValue](spropvalue.md) определяет свойство, которое необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="93337-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93337-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93337-115">Return value</span></span>

<span data-ttu-id="93337-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="93337-116">TRUE</span></span> 
  
> <span data-ttu-id="93337-117">Указанное свойство недопустимо.</span><span class="sxs-lookup"><span data-stu-id="93337-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="93337-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="93337-118">FALSE</span></span> 
  
> <span data-ttu-id="93337-119">Указанное свойство допустимо.</span><span class="sxs-lookup"><span data-stu-id="93337-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93337-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="93337-120">Remarks</span></span>

<span data-ttu-id="93337-121">Существует несколько причин для вызова функции **FBadProp** поставщиком услуг. Например, это может быть сделано для подготовки вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md), задающего свойство.</span><span class="sxs-lookup"><span data-stu-id="93337-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="93337-122">**FBadProp** выбирает ход проверки для указанного свойства в зависимости от его типа.</span><span class="sxs-lookup"><span data-stu-id="93337-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="93337-123">Например, если свойство является логическим, **FBadProp** необходимо убедиться, что ему присвоено одно из значений: TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="93337-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="93337-124">Для двоичных свойств **FBadProp** проверяет указатель, размер и правильность выделения.</span><span class="sxs-lookup"><span data-stu-id="93337-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93337-125">См. также</span><span class="sxs-lookup"><span data-stu-id="93337-125">See also</span></span>



[<span data-ttu-id="93337-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="93337-126">FBadPropTag</span></span>](fbadproptag.md)

