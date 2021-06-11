---
title: Функция BOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Ограничивает значение ячейки диапазоном или набором диапазонов.
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425962"
---
# <a name="bound-function"></a><span data-ttu-id="25c72-103">Функция BOUND</span><span class="sxs-lookup"><span data-stu-id="25c72-103">BOUND Function</span></span>

<span data-ttu-id="25c72-104">Ограничивает значение ячейки диапазоном или набором диапазонов.</span><span class="sxs-lookup"><span data-stu-id="25c72-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="25c72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25c72-105">Syntax</span></span>

<span data-ttu-id="25c72-106">BOUND (\*\* *значение* \*\*, \*\*\*\* тип \*\*, \*\*\*\* игнорировать \*\*, \*\* *значение1* \*\*, \*\* *значение2* \*\* \*\* \* [,игнорировать(n), value1(n), value2(n),...] \* \*\*</span><span class="sxs-lookup"><span data-stu-id="25c72-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="25c72-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="25c72-107">Parameters</span></span>

|<span data-ttu-id="25c72-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="25c72-108">**Name**</span></span>|<span data-ttu-id="25c72-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="25c72-109">**Required/Optional**</span></span>|<span data-ttu-id="25c72-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="25c72-110">**Data Type**</span></span>|<span data-ttu-id="25c72-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25c72-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="25c72-112">_value_</span><span class="sxs-lookup"><span data-stu-id="25c72-112">_value_</span></span> <br/> |<span data-ttu-id="25c72-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25c72-113">Required</span></span>  <br/> |<span data-ttu-id="25c72-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="25c72-114">**Numeric**</span></span> <br/> |<span data-ttu-id="25c72-115">Текущее ограниченное значение.</span><span class="sxs-lookup"><span data-stu-id="25c72-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="25c72-116">_type_</span><span class="sxs-lookup"><span data-stu-id="25c72-116">_type_</span></span> <br/> |<span data-ttu-id="25c72-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25c72-117">Required</span></span>  <br/> |<span data-ttu-id="25c72-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="25c72-118">**Numeric**</span></span> <br/> |<span data-ttu-id="25c72-119">Является ли ограничение включено (0), эксклюзивно (1) или отключено (2).</span><span class="sxs-lookup"><span data-stu-id="25c72-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="25c72-120">_игнорировать_</span><span class="sxs-lookup"><span data-stu-id="25c72-120">_ignore_</span></span> <br/> |<span data-ttu-id="25c72-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25c72-121">Required</span></span>  <br/> |<span data-ttu-id="25c72-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="25c72-122">**Boolean**</span></span> <br/> | <span data-ttu-id="25c72-123">TRUE, чтобы игнорировать диапазон; FALSE, чтобы ограничить значение ячейки в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="25c72-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="25c72-124">_value1_</span><span class="sxs-lookup"><span data-stu-id="25c72-124">_value1_</span></span> <br/> |<span data-ttu-id="25c72-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25c72-125">Required</span></span>  <br/> |<span data-ttu-id="25c72-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="25c72-126">**Numeric**</span></span> <br/> |<span data-ttu-id="25c72-127">Первое значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="25c72-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="25c72-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="25c72-128">_value2_</span></span> <br/> |<span data-ttu-id="25c72-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="25c72-129">Required</span></span>  <br/> |<span data-ttu-id="25c72-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="25c72-130">**Numeric**</span></span> <br/> |<span data-ttu-id="25c72-131">Второе значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="25c72-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25c72-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="25c72-132">Remarks</span></span>

<span data-ttu-id="25c72-133">Используйте функцию BOUND, чтобы ограничить значение ячейки верхней и нижней частью, например, для управления объектами, которые не должны растягиваться выше или ниже минимальной или максимальной высоты.</span><span class="sxs-lookup"><span data-stu-id="25c72-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="25c72-134">Ограничение может быть инклюзивным или эксклюзивным по отношению к диапазону или диапазонам.</span><span class="sxs-lookup"><span data-stu-id="25c72-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="25c72-135">Если текущее значение не должно быть ограничено, установите параметр  _типа_ 2 (отключен).</span><span class="sxs-lookup"><span data-stu-id="25c72-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="25c72-136">Вы можете определить несколько диапазонов, поставляя несколько вхождений параметров _ignore,_ _value1_ и _value2._</span><span class="sxs-lookup"><span data-stu-id="25c72-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="25c72-137">Используйте параметр  _ignore_ для отключения ограничений определенным диапазоном.</span><span class="sxs-lookup"><span data-stu-id="25c72-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="25c72-138">Формула, содержащая функцию BOUND, не перезаписывается при изменениях ее значения; вместо этого формула сохраняется и новое значение помещается в _параметр значения._</span><span class="sxs-lookup"><span data-stu-id="25c72-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="25c72-139">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25c72-139">Example 1</span></span>

<span data-ttu-id="25c72-140">В этом примере функция BOUND использует функцию BOUND, чтобы заставить ручку управления оставаться в границах фигуры.</span><span class="sxs-lookup"><span data-stu-id="25c72-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="25c72-141">Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)</span><span class="sxs-lookup"><span data-stu-id="25c72-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="25c72-142">Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)</span><span class="sxs-lookup"><span data-stu-id="25c72-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="25c72-143">Пример 2</span><span class="sxs-lookup"><span data-stu-id="25c72-143">Example 2</span></span>

<span data-ttu-id="25c72-144">В этом примере функция BOUND ограничивает ширину фигуры до 2 дюймов, 4 дюймов или 6 дюймов.</span><span class="sxs-lookup"><span data-stu-id="25c72-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="25c72-145">Ширина = BOUND(, 0, FALSE, 2 в, 2 в, FALSE, 4 в, 4, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="25c72-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

