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
# <a name="bound-function"></a><span data-ttu-id="fa896-103">Функция BOUND</span><span class="sxs-lookup"><span data-stu-id="fa896-103">BOUND Function</span></span>

<span data-ttu-id="fa896-104">Ограничивает значение ячейки диапазоном или набором диапазонов.</span><span class="sxs-lookup"><span data-stu-id="fa896-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fa896-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa896-105">Syntax</span></span>

<span data-ttu-id="fa896-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fa896-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fa896-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa896-107">Parameters</span></span>

|<span data-ttu-id="fa896-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fa896-108">**Name**</span></span>|<span data-ttu-id="fa896-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fa896-109">**Required/Optional**</span></span>|<span data-ttu-id="fa896-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fa896-110">**Data Type**</span></span>|<span data-ttu-id="fa896-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fa896-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fa896-112">_value_</span><span class="sxs-lookup"><span data-stu-id="fa896-112">_value_</span></span> <br/> |<span data-ttu-id="fa896-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fa896-113">Required</span></span>  <br/> |<span data-ttu-id="fa896-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fa896-114">**Numeric**</span></span> <br/> |<span data-ttu-id="fa896-115">Текущее ограниченное значение.</span><span class="sxs-lookup"><span data-stu-id="fa896-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="fa896-116">_type_</span><span class="sxs-lookup"><span data-stu-id="fa896-116">_type_</span></span> <br/> |<span data-ttu-id="fa896-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fa896-117">Required</span></span>  <br/> |<span data-ttu-id="fa896-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fa896-118">**Numeric**</span></span> <br/> |<span data-ttu-id="fa896-119">Является ли ограничение инклюзивным (0), монопольным (1) или отключенным (2).</span><span class="sxs-lookup"><span data-stu-id="fa896-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="fa896-120">_ignore_</span><span class="sxs-lookup"><span data-stu-id="fa896-120">_ignore_</span></span> <br/> |<span data-ttu-id="fa896-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fa896-121">Required</span></span>  <br/> |<span data-ttu-id="fa896-122">**Логический**</span><span class="sxs-lookup"><span data-stu-id="fa896-122">**Boolean**</span></span> <br/> | <span data-ttu-id="fa896-123">TRUE для игнорирования диапазона; ЗНАЧЕНИЕ FALSE, чтобы ограничить значение ячейки диапазоном.</span><span class="sxs-lookup"><span data-stu-id="fa896-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="fa896-124">_value1_</span><span class="sxs-lookup"><span data-stu-id="fa896-124">_value1_</span></span> <br/> |<span data-ttu-id="fa896-125">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fa896-125">Required</span></span>  <br/> |<span data-ttu-id="fa896-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fa896-126">**Numeric**</span></span> <br/> |<span data-ttu-id="fa896-127">Первое значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="fa896-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="fa896-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="fa896-128">_value2_</span></span> <br/> |<span data-ttu-id="fa896-129">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fa896-129">Required</span></span>  <br/> |<span data-ttu-id="fa896-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fa896-130">**Numeric**</span></span> <br/> |<span data-ttu-id="fa896-131">Второе значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="fa896-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa896-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa896-132">Remarks</span></span>

<span data-ttu-id="fa896-133">Используйте функцию BOUND, чтобы ограничить значение ячейки верхней и нижней границами, например для управления объектами, которые не должны быть растянуты выше или ниже минимальной или максимальной высоты.</span><span class="sxs-lookup"><span data-stu-id="fa896-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="fa896-134">Ограничение может быть инклюзивным или монопольным в отношении диапазона или диапазонов.</span><span class="sxs-lookup"><span data-stu-id="fa896-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="fa896-135">Если текущее значение не должно быть ограничено, установите для параметра  _типа_ значение 2 (отключено).</span><span class="sxs-lookup"><span data-stu-id="fa896-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="fa896-136">Можно определить несколько диапазонов, заданы несколько вхождений параметров _ignore,_ _value1_ и _value2._</span><span class="sxs-lookup"><span data-stu-id="fa896-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="fa896-137">Параметр  _ignore_ используется для отключения ограничений для определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="fa896-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="fa896-138">Формула, содержащая функцию BOUND, не перезаписывается при смене ее значения; вместо этого формула сохраняется, а новое значение помещается в _параметр value._</span><span class="sxs-lookup"><span data-stu-id="fa896-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fa896-139">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa896-139">Example 1</span></span>

<span data-ttu-id="fa896-140">В этом примере функция BOUND используется для принудительного хранения окне управления в пределах границ фигуры.</span><span class="sxs-lookup"><span data-stu-id="fa896-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="fa896-141">Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)</span><span class="sxs-lookup"><span data-stu-id="fa896-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="fa896-142">Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)</span><span class="sxs-lookup"><span data-stu-id="fa896-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fa896-143">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa896-143">Example 2</span></span>

<span data-ttu-id="fa896-144">В этом примере функция BOUND используется для ограничения ширины фигуры до 2, 4 и 6 дюймов.</span><span class="sxs-lookup"><span data-stu-id="fa896-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="fa896-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span><span class="sxs-lookup"><span data-stu-id="fa896-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

