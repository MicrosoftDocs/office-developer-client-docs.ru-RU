---
title: Функция HSL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Возвращает значение, представляющее индекса в документе цветовой палитры. Он указывает цвет по его тона, насыщенность и яркость компонентов.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813920"
---
# <a name="hsl-function"></a><span data-ttu-id="7b2fc-104">Функция HSL</span><span class="sxs-lookup"><span data-stu-id="7b2fc-104">HSL Function</span></span>

<span data-ttu-id="7b2fc-105">Возвращает значение, представляющее индекса в документе цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="7b2fc-106">Он указывает цвет по его тона, насыщенность и яркость компонентов.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7b2fc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b2fc-107">Syntax</span></span>

<span data-ttu-id="7b2fc-108">HSL (** *тона* **, ** *насыщенность* **, ** *яркость* **)</span><span class="sxs-lookup"><span data-stu-id="7b2fc-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b2fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b2fc-109">Parameters</span></span>

|<span data-ttu-id="7b2fc-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-110">**Name**</span></span>|<span data-ttu-id="7b2fc-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-111">**Required/Optional**</span></span>|<span data-ttu-id="7b2fc-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-112">**Data Type**</span></span>|<span data-ttu-id="7b2fc-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b2fc-114">_тона_</span><span class="sxs-lookup"><span data-stu-id="7b2fc-114">_hue_</span></span> <br/> |<span data-ttu-id="7b2fc-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-115">Required</span></span>  <br/> |<span data-ttu-id="7b2fc-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-116">**Number**</span></span> <br/> |<span data-ttu-id="7b2fc-117">Цветового тона, выраженное как число в диапазоне 0 для 239 включительно, или выражение, которое оценивается как такое число.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="7b2fc-118">_насыщенность_</span><span class="sxs-lookup"><span data-stu-id="7b2fc-118">_saturation_</span></span> <br/> |<span data-ttu-id="7b2fc-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-119">Required</span></span>  <br/> |<span data-ttu-id="7b2fc-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-120">**Number**</span></span> <br/> |<span data-ttu-id="7b2fc-121">Насыщенность цвета, выраженное как число в диапазоне от 0 до 240 включительно, или выражение, которое оценивается как такое число.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="7b2fc-122">_«яркость»_</span><span class="sxs-lookup"><span data-stu-id="7b2fc-122">_luminosity_</span></span> <br/> |<span data-ttu-id="7b2fc-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-123">Required</span></span>  <br/> |<span data-ttu-id="7b2fc-124">**Число**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-124">**Number**</span></span> <br/> | <span data-ttu-id="7b2fc-125">Яркость цвета, выраженное как число в диапазоне от 0 до 240 включительно, или выражение, которое оценивается как такое число.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7b2fc-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7b2fc-126">Return value</span></span>

<span data-ttu-id="7b2fc-127">Number</span><span class="sxs-lookup"><span data-stu-id="7b2fc-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b2fc-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b2fc-128">Remarks</span></span>

<span data-ttu-id="7b2fc-129">Если цвет, возвращаемого функцией еще не включенное в текущем документе цветовой палитры, добавляется документа списка доступных цветов.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="7b2fc-130">В следующей таблице перечислены некоторые стандартные цвета и тона, насыщенность и яркость значения.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="7b2fc-131">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-131">**Color**</span></span>|<span data-ttu-id="7b2fc-132">**Значение тона**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-132">**Hue value**</span></span>|<span data-ttu-id="7b2fc-133">**Насыщенность значение**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-133">**Saturation value**</span></span>|<span data-ttu-id="7b2fc-134">**Значение яркости**</span><span class="sxs-lookup"><span data-stu-id="7b2fc-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b2fc-135">Черный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-135">Black</span></span>  <br/> |<span data-ttu-id="7b2fc-136">0</span><span class="sxs-lookup"><span data-stu-id="7b2fc-136">0</span></span>  <br/> |<span data-ttu-id="7b2fc-137">0</span><span class="sxs-lookup"><span data-stu-id="7b2fc-137">0</span></span>  <br/> |<span data-ttu-id="7b2fc-138">24</span><span class="sxs-lookup"><span data-stu-id="7b2fc-138">24</span></span>  <br/> |
|<span data-ttu-id="7b2fc-139">Синий</span><span class="sxs-lookup"><span data-stu-id="7b2fc-139">Blue</span></span>  <br/> |<span data-ttu-id="7b2fc-140">160</span><span class="sxs-lookup"><span data-stu-id="7b2fc-140">160</span></span>  <br/> |<span data-ttu-id="7b2fc-141">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-141">240</span></span>  <br/> |<span data-ttu-id="7b2fc-142">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-142">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="7b2fc-143">Green</span></span>  <br/> |<span data-ttu-id="7b2fc-144">80</span><span class="sxs-lookup"><span data-stu-id="7b2fc-144">80</span></span>  <br/> |<span data-ttu-id="7b2fc-145">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-145">240</span></span>  <br/> |<span data-ttu-id="7b2fc-146">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-146">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-147">Голубой</span><span class="sxs-lookup"><span data-stu-id="7b2fc-147">Cyan</span></span>  <br/> |<span data-ttu-id="7b2fc-148">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-148">120</span></span>  <br/> |<span data-ttu-id="7b2fc-149">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-149">240</span></span>  <br/> |<span data-ttu-id="7b2fc-150">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-150">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-151">Красный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-151">Red</span></span>  <br/> |<span data-ttu-id="7b2fc-152">0</span><span class="sxs-lookup"><span data-stu-id="7b2fc-152">0</span></span>  <br/> |<span data-ttu-id="7b2fc-153">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-153">240</span></span>  <br/> |<span data-ttu-id="7b2fc-154">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-154">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="7b2fc-155">Magenta</span></span>  <br/> |<span data-ttu-id="7b2fc-156">200</span><span class="sxs-lookup"><span data-stu-id="7b2fc-156">200</span></span>  <br/> |<span data-ttu-id="7b2fc-157">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-157">240</span></span>  <br/> |<span data-ttu-id="7b2fc-158">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-158">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="7b2fc-159">Yellow</span></span>  <br/> |<span data-ttu-id="7b2fc-160">40</span><span class="sxs-lookup"><span data-stu-id="7b2fc-160">40</span></span>  <br/> |<span data-ttu-id="7b2fc-161">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-161">240</span></span>  <br/> |<span data-ttu-id="7b2fc-162">120</span><span class="sxs-lookup"><span data-stu-id="7b2fc-162">120</span></span>  <br/> |
|<span data-ttu-id="7b2fc-163">Белый</span><span class="sxs-lookup"><span data-stu-id="7b2fc-163">White</span></span>  <br/> |<span data-ttu-id="7b2fc-164">0</span><span class="sxs-lookup"><span data-stu-id="7b2fc-164">0</span></span>  <br/> |<span data-ttu-id="7b2fc-165">0</span><span class="sxs-lookup"><span data-stu-id="7b2fc-165">0</span></span>  <br/> |<span data-ttu-id="7b2fc-166">240</span><span class="sxs-lookup"><span data-stu-id="7b2fc-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="7b2fc-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b2fc-167">Example 1</span></span>

<span data-ttu-id="7b2fc-168">HSL(160,240,120)</span><span class="sxs-lookup"><span data-stu-id="7b2fc-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="7b2fc-169">Возвращает индекс цвета синего.</span><span class="sxs-lookup"><span data-stu-id="7b2fc-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7b2fc-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7b2fc-170">Example 2</span></span>

<span data-ttu-id="7b2fc-171">HSL(HUE(FillForegnd),sat(FillForegnd),Min(LUM(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="7b2fc-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="7b2fc-172">Возвращает индекс для цвета, который отражает цвет заливки с повышенной «яркость».</span><span class="sxs-lookup"><span data-stu-id="7b2fc-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

