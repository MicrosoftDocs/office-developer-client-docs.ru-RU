---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Возвращает значение, представляющее индекса в документе цветовой палитры. Он указывает цвет по его красного, зеленого и синего компонентов, где каждый — число в диапазоне от 0 до 255 включительно, или выражение, которое оценивается как такое число.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814610"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="bd396-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bd396-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bd396-105">Возвращает значение, представляющее индекса в документе цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="bd396-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="bd396-106">Он указывает цвет по его красного, зеленого и синего компонентов, где каждый — число в диапазоне от 0 до 255 включительно, или выражение, которое оценивается как такое число.</span><span class="sxs-lookup"><span data-stu-id="bd396-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bd396-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd396-107">Syntax</span></span>

<span data-ttu-id="bd396-108">RGB (** *красной* **, ** *зеленой* **, ** *Синий* **)</span><span class="sxs-lookup"><span data-stu-id="bd396-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bd396-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd396-109">Parameters</span></span>

|<span data-ttu-id="bd396-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bd396-110">**Name**</span></span>|<span data-ttu-id="bd396-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bd396-111">**Required/Optional**</span></span>|<span data-ttu-id="bd396-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bd396-112">**Data Type**</span></span>|<span data-ttu-id="bd396-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd396-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd396-114">_красный_</span><span class="sxs-lookup"><span data-stu-id="bd396-114">_red_</span></span> <br/> |<span data-ttu-id="bd396-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bd396-115">Required</span></span>  <br/> |<span data-ttu-id="bd396-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="bd396-116">**Number**</span></span> <br/> |<span data-ttu-id="bd396-117">Красный компонент.</span><span class="sxs-lookup"><span data-stu-id="bd396-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="bd396-118">_Зеленый_</span><span class="sxs-lookup"><span data-stu-id="bd396-118">_green_</span></span> <br/> |<span data-ttu-id="bd396-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bd396-119">Required</span></span>  <br/> |<span data-ttu-id="bd396-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="bd396-120">**Number**</span></span> <br/> |<span data-ttu-id="bd396-121">Зеленый компонент.</span><span class="sxs-lookup"><span data-stu-id="bd396-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="bd396-122">_синий_</span><span class="sxs-lookup"><span data-stu-id="bd396-122">_blue_</span></span> <br/> |<span data-ttu-id="bd396-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bd396-123">Required</span></span>  <br/> |<span data-ttu-id="bd396-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="bd396-124">**Nmber**</span></span> <br/> |<span data-ttu-id="bd396-125">Синий компонент.</span><span class="sxs-lookup"><span data-stu-id="bd396-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bd396-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="bd396-127">Number</span><span class="sxs-lookup"><span data-stu-id="bd396-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd396-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd396-128">Remarks</span></span>

<span data-ttu-id="bd396-129">Если цвет, возвращаемого функцией еще не включенное в текущем документе цветовой палитры, добавляется палитры.</span><span class="sxs-lookup"><span data-stu-id="bd396-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="bd396-130">В следующей таблице перечислены некоторые стандартные цвета и их значения красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="bd396-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="bd396-131">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="bd396-131">**Color**</span></span>|<span data-ttu-id="bd396-132">**Значение красного**</span><span class="sxs-lookup"><span data-stu-id="bd396-132">**Red value**</span></span>|<span data-ttu-id="bd396-133">**Значение зеленого**</span><span class="sxs-lookup"><span data-stu-id="bd396-133">**Green value**</span></span>|<span data-ttu-id="bd396-134">**Значение синего**</span><span class="sxs-lookup"><span data-stu-id="bd396-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd396-135">Черный</span><span class="sxs-lookup"><span data-stu-id="bd396-135">Black</span></span>  <br/> |<span data-ttu-id="bd396-136">0</span><span class="sxs-lookup"><span data-stu-id="bd396-136">0</span></span>  <br/> |<span data-ttu-id="bd396-137">0</span><span class="sxs-lookup"><span data-stu-id="bd396-137">0</span></span>  <br/> |<span data-ttu-id="bd396-138">0</span><span class="sxs-lookup"><span data-stu-id="bd396-138">0</span></span>  <br/> |
|<span data-ttu-id="bd396-139">Синий</span><span class="sxs-lookup"><span data-stu-id="bd396-139">Blue</span></span>  <br/> |<span data-ttu-id="bd396-140">0</span><span class="sxs-lookup"><span data-stu-id="bd396-140">0</span></span>  <br/> |<span data-ttu-id="bd396-141">0</span><span class="sxs-lookup"><span data-stu-id="bd396-141">0</span></span>  <br/> |<span data-ttu-id="bd396-142">255</span><span class="sxs-lookup"><span data-stu-id="bd396-142">255</span></span>  <br/> |
|<span data-ttu-id="bd396-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="bd396-143">Green</span></span>  <br/> |<span data-ttu-id="bd396-144">0</span><span class="sxs-lookup"><span data-stu-id="bd396-144">0</span></span>  <br/> |<span data-ttu-id="bd396-145">255</span><span class="sxs-lookup"><span data-stu-id="bd396-145">255</span></span>  <br/> |<span data-ttu-id="bd396-146">0</span><span class="sxs-lookup"><span data-stu-id="bd396-146">0</span></span>  <br/> |
|<span data-ttu-id="bd396-147">Голубой</span><span class="sxs-lookup"><span data-stu-id="bd396-147">Cyan</span></span>  <br/> |<span data-ttu-id="bd396-148">0</span><span class="sxs-lookup"><span data-stu-id="bd396-148">0</span></span>  <br/> |<span data-ttu-id="bd396-149">255</span><span class="sxs-lookup"><span data-stu-id="bd396-149">255</span></span>  <br/> |<span data-ttu-id="bd396-150">255</span><span class="sxs-lookup"><span data-stu-id="bd396-150">255</span></span>  <br/> |
|<span data-ttu-id="bd396-151">Красный</span><span class="sxs-lookup"><span data-stu-id="bd396-151">Red</span></span>  <br/> |<span data-ttu-id="bd396-152">255</span><span class="sxs-lookup"><span data-stu-id="bd396-152">255</span></span>  <br/> |<span data-ttu-id="bd396-153">0</span><span class="sxs-lookup"><span data-stu-id="bd396-153">0</span></span>  <br/> |<span data-ttu-id="bd396-154">0</span><span class="sxs-lookup"><span data-stu-id="bd396-154">0</span></span>  <br/> |
|<span data-ttu-id="bd396-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="bd396-155">Magenta</span></span>  <br/> |<span data-ttu-id="bd396-156">255</span><span class="sxs-lookup"><span data-stu-id="bd396-156">255</span></span>  <br/> |<span data-ttu-id="bd396-157">0</span><span class="sxs-lookup"><span data-stu-id="bd396-157">0</span></span>  <br/> |<span data-ttu-id="bd396-158">255</span><span class="sxs-lookup"><span data-stu-id="bd396-158">255</span></span>  <br/> |
|<span data-ttu-id="bd396-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="bd396-159">Yellow</span></span>  <br/> |<span data-ttu-id="bd396-160">255</span><span class="sxs-lookup"><span data-stu-id="bd396-160">255</span></span>  <br/> |<span data-ttu-id="bd396-161">255</span><span class="sxs-lookup"><span data-stu-id="bd396-161">255</span></span>  <br/> |<span data-ttu-id="bd396-162">0</span><span class="sxs-lookup"><span data-stu-id="bd396-162">0</span></span>  <br/> |
|<span data-ttu-id="bd396-163">Белый</span><span class="sxs-lookup"><span data-stu-id="bd396-163">White</span></span>  <br/> |<span data-ttu-id="bd396-164">255</span><span class="sxs-lookup"><span data-stu-id="bd396-164">255</span></span>  <br/> |<span data-ttu-id="bd396-165">255</span><span class="sxs-lookup"><span data-stu-id="bd396-165">255</span></span>  <br/> |<span data-ttu-id="bd396-166">255</span><span class="sxs-lookup"><span data-stu-id="bd396-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="bd396-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd396-167">Example 1</span></span>

<span data-ttu-id="bd396-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="bd396-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="bd396-169">Возвращает индекс цвета синего.</span><span class="sxs-lookup"><span data-stu-id="bd396-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bd396-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd396-170">Example 2</span></span>

<span data-ttu-id="bd396-171">RGB (красный (Sheet.1! FillForegnd) 120, 0)</span><span class="sxs-lookup"><span data-stu-id="bd396-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="bd396-172">Возвращает индекс для цвета, красный компонент отражает листе. 1 заливки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="bd396-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

