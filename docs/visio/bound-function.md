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
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813326"
---
# <a name="bound-function"></a><span data-ttu-id="6dc43-103">Функция BOUND</span><span class="sxs-lookup"><span data-stu-id="6dc43-103">BOUND Function</span></span>

<span data-ttu-id="6dc43-104">Ограничивает значение ячейки диапазоном или набором диапазонов.</span><span class="sxs-lookup"><span data-stu-id="6dc43-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6dc43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dc43-105">Syntax</span></span>

<span data-ttu-id="6dc43-106">ПРИВЯЗКИ (** *значение* **, ** *Тип* **, ** *Игнорировать* **, ** *значение1* **, ** *значение2* ** ** * [, ignore(n), value1(n), value2(n),...] * **)</span><span class="sxs-lookup"><span data-stu-id="6dc43-106">BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6dc43-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6dc43-107">Parameters</span></span>

|<span data-ttu-id="6dc43-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6dc43-108">**Name**</span></span>|<span data-ttu-id="6dc43-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6dc43-109">**Required/Optional**</span></span>|<span data-ttu-id="6dc43-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6dc43-110">**Data Type**</span></span>|<span data-ttu-id="6dc43-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6dc43-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6dc43-112">_value_</span><span class="sxs-lookup"><span data-stu-id="6dc43-112">_value_</span></span> <br/> |<span data-ttu-id="6dc43-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6dc43-113">Required</span></span>  <br/> |<span data-ttu-id="6dc43-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6dc43-114">**Numeric**</span></span> <br/> |<span data-ttu-id="6dc43-115">Текущее значение ограничены.</span><span class="sxs-lookup"><span data-stu-id="6dc43-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="6dc43-116">_type_</span><span class="sxs-lookup"><span data-stu-id="6dc43-116">_type_</span></span> <br/> |<span data-ttu-id="6dc43-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6dc43-117">Required</span></span>  <br/> |<span data-ttu-id="6dc43-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6dc43-118">**Numeric**</span></span> <br/> |<span data-ttu-id="6dc43-119">Является ли ограничение включительно (0), монопольная (1) или отключено (2).</span><span class="sxs-lookup"><span data-stu-id="6dc43-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="6dc43-120">_Пропуск_</span><span class="sxs-lookup"><span data-stu-id="6dc43-120">_ignore_</span></span> <br/> |<span data-ttu-id="6dc43-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6dc43-121">Required</span></span>  <br/> |<span data-ttu-id="6dc43-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6dc43-122">**Boolean**</span></span> <br/> | <span data-ttu-id="6dc43-123">Значение TRUE, следует ли игнорировать диапазон; Значение FALSE, чтобы ограничить значения ячейки в диапазон.</span><span class="sxs-lookup"><span data-stu-id="6dc43-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="6dc43-124">_Значение1_</span><span class="sxs-lookup"><span data-stu-id="6dc43-124">_value1_</span></span> <br/> |<span data-ttu-id="6dc43-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6dc43-125">Required</span></span>  <br/> |<span data-ttu-id="6dc43-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6dc43-126">**Numeric**</span></span> <br/> |<span data-ttu-id="6dc43-127">Первое значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="6dc43-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="6dc43-128">_значение2_</span><span class="sxs-lookup"><span data-stu-id="6dc43-128">_value2_</span></span> <br/> |<span data-ttu-id="6dc43-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6dc43-129">Required</span></span>  <br/> |<span data-ttu-id="6dc43-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6dc43-130">**Numeric**</span></span> <br/> |<span data-ttu-id="6dc43-131">Второе значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="6dc43-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dc43-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="6dc43-132">Remarks</span></span>

<span data-ttu-id="6dc43-133">Используйте функцию ПРИВЯЗКИ для ограничения ячейки значение на верхнюю и нижнюю границу, например, для управления объектами, не должен быть растянут выше или ниже минимального и максимального высоту.</span><span class="sxs-lookup"><span data-stu-id="6dc43-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="6dc43-134">Ограничение может быть включительно или монопольной по отношению к диапазон или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="6dc43-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="6dc43-135">Если текущее значение не должен быть ограничен, установите для параметра _Тип_ 2 (отключено).</span><span class="sxs-lookup"><span data-stu-id="6dc43-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="6dc43-136">Вы можете определить несколько диапазонов, передав несколько вхождений _Игнорировать_ _значение1_и _значение2_ параметров.</span><span class="sxs-lookup"><span data-stu-id="6dc43-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="6dc43-137">Используйте параметр _Игнорировать_ отключить ограничения, определенного диапазона.</span><span class="sxs-lookup"><span data-stu-id="6dc43-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="6dc43-138">Формула, содержащий ПРИВЯЗАННОЙ функции не будет перезаписан при изменении значения; Вместо этого сохраняются формулы и новое значение помещается в качестве _значения_ параметра.</span><span class="sxs-lookup"><span data-stu-id="6dc43-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6dc43-139">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6dc43-139">Example 1</span></span>

<span data-ttu-id="6dc43-140">В этом примере функция ПРИВЯЗАННОЙ используется для принудительной дескриптор управления оставаться внутри прямоугольника фигуры.</span><span class="sxs-lookup"><span data-stu-id="6dc43-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="6dc43-141">Controls.X1 = ГРАНИЦУ (ширина\*0,5, 0, значение FALSE, ширина\*ширину 0,\*1)</span><span class="sxs-lookup"><span data-stu-id="6dc43-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="6dc43-142">Controls.Y1 = ГРАНИЦУ (высота\*0,5, 0, значение FALSE, высота\*0, высота\*1)</span><span class="sxs-lookup"><span data-stu-id="6dc43-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6dc43-143">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6dc43-143">Example 2</span></span>

<span data-ttu-id="6dc43-144">В этом примере функция ограничение ширины фигуры на 2 дюйма, 4 дюйма или 6 дюймов ПРИВЯЗКИ.</span><span class="sxs-lookup"><span data-stu-id="6dc43-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="6dc43-145">Ширина = ГРАНИЦУ (, 0, FALSE, 2 в 2 в значение FALSE, 4, 4 в случае — FALSE, 6, 6 in)</span><span class="sxs-lookup"><span data-stu-id="6dc43-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

