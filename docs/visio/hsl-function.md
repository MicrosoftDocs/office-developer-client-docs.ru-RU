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
description: Возвращает значение, представляющее индекс в цветовой палитре документа. Он определяет цвет по его оттенку, насыщенности и компоненты luminosity.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420964"
---
# <a name="hsl-function"></a><span data-ttu-id="e2321-104">Функция HSL</span><span class="sxs-lookup"><span data-stu-id="e2321-104">HSL Function</span></span>

<span data-ttu-id="e2321-105">Возвращает значение, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="e2321-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="e2321-106">Он определяет цвет по его оттенку, насыщенности и компоненты luminosity.</span><span class="sxs-lookup"><span data-stu-id="e2321-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e2321-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2321-107">Syntax</span></span>

<span data-ttu-id="e2321-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e2321-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e2321-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2321-109">Parameters</span></span>

|<span data-ttu-id="e2321-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e2321-110">**Name**</span></span>|<span data-ttu-id="e2321-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e2321-111">**Required/Optional**</span></span>|<span data-ttu-id="e2321-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e2321-112">**Data Type**</span></span>|<span data-ttu-id="e2321-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2321-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e2321-114">_hue_</span><span class="sxs-lookup"><span data-stu-id="e2321-114">_hue_</span></span> <br/> |<span data-ttu-id="e2321-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e2321-115">Required</span></span>  <br/> |<span data-ttu-id="e2321-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="e2321-116">**Number**</span></span> <br/> |<span data-ttu-id="e2321-117">Цвет, выраженный числом в диапазоне от 0 до 239 включительно или выражением, оценивающим такое число.</span><span class="sxs-lookup"><span data-stu-id="e2321-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="e2321-118">_saturation_</span><span class="sxs-lookup"><span data-stu-id="e2321-118">_saturation_</span></span> <br/> |<span data-ttu-id="e2321-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e2321-119">Required</span></span>  <br/> |<span data-ttu-id="e2321-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="e2321-120">**Number**</span></span> <br/> |<span data-ttu-id="e2321-121">Насыщенность цвета, выраженная числом в диапазоне от 0 до 240 включительно или выражением, оценивающим такое число.</span><span class="sxs-lookup"><span data-stu-id="e2321-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="e2321-122">_luminosity_</span><span class="sxs-lookup"><span data-stu-id="e2321-122">_luminosity_</span></span> <br/> |<span data-ttu-id="e2321-123">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e2321-123">Required</span></span>  <br/> |<span data-ttu-id="e2321-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="e2321-124">**Number**</span></span> <br/> | <span data-ttu-id="e2321-125">Luminosity цвета, выраженное числом в диапазоне от 0 до 240 включительно или выражением, оценивающим такое число.</span><span class="sxs-lookup"><span data-stu-id="e2321-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e2321-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2321-126">Return value</span></span>

<span data-ttu-id="e2321-127">Числовой</span><span class="sxs-lookup"><span data-stu-id="e2321-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2321-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2321-128">Remarks</span></span>

<span data-ttu-id="e2321-129">Если цвет, возвращенный функцией, еще не существует в цветовой палитре текущего документа, он добавляется в список доступных цветов документа.</span><span class="sxs-lookup"><span data-stu-id="e2321-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="e2321-130">В следующей таблице перечислены некоторые стандартные цвета, а также их оттенки, насыщенность и luminosity.</span><span class="sxs-lookup"><span data-stu-id="e2321-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="e2321-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="e2321-131">**Color**</span></span>|<span data-ttu-id="e2321-132">**Значение hue**</span><span class="sxs-lookup"><span data-stu-id="e2321-132">**Hue value**</span></span>|<span data-ttu-id="e2321-133">**Значение насыщенности**</span><span class="sxs-lookup"><span data-stu-id="e2321-133">**Saturation value**</span></span>|<span data-ttu-id="e2321-134">**Значение luminosity**</span><span class="sxs-lookup"><span data-stu-id="e2321-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2321-135">Черный</span><span class="sxs-lookup"><span data-stu-id="e2321-135">Black</span></span>  <br/> |<span data-ttu-id="e2321-136">0</span><span class="sxs-lookup"><span data-stu-id="e2321-136">0</span></span>  <br/> |<span data-ttu-id="e2321-137">0</span><span class="sxs-lookup"><span data-stu-id="e2321-137">0</span></span>  <br/> |<span data-ttu-id="e2321-138">24</span><span class="sxs-lookup"><span data-stu-id="e2321-138">24</span></span>  <br/> |
|<span data-ttu-id="e2321-139">Синий</span><span class="sxs-lookup"><span data-stu-id="e2321-139">Blue</span></span>  <br/> |<span data-ttu-id="e2321-140">160</span><span class="sxs-lookup"><span data-stu-id="e2321-140">160</span></span>  <br/> |<span data-ttu-id="e2321-141">240</span><span class="sxs-lookup"><span data-stu-id="e2321-141">240</span></span>  <br/> |<span data-ttu-id="e2321-142">120</span><span class="sxs-lookup"><span data-stu-id="e2321-142">120</span></span>  <br/> |
|<span data-ttu-id="e2321-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="e2321-143">Green</span></span>  <br/> |<span data-ttu-id="e2321-144">80</span><span class="sxs-lookup"><span data-stu-id="e2321-144">80</span></span>  <br/> |<span data-ttu-id="e2321-145">240</span><span class="sxs-lookup"><span data-stu-id="e2321-145">240</span></span>  <br/> |<span data-ttu-id="e2321-146">120</span><span class="sxs-lookup"><span data-stu-id="e2321-146">120</span></span>  <br/> |
|<span data-ttu-id="e2321-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="e2321-147">Cyan</span></span>  <br/> |<span data-ttu-id="e2321-148">120</span><span class="sxs-lookup"><span data-stu-id="e2321-148">120</span></span>  <br/> |<span data-ttu-id="e2321-149">240</span><span class="sxs-lookup"><span data-stu-id="e2321-149">240</span></span>  <br/> |<span data-ttu-id="e2321-150">120</span><span class="sxs-lookup"><span data-stu-id="e2321-150">120</span></span>  <br/> |
|<span data-ttu-id="e2321-151">Красный</span><span class="sxs-lookup"><span data-stu-id="e2321-151">Red</span></span>  <br/> |<span data-ttu-id="e2321-152">0</span><span class="sxs-lookup"><span data-stu-id="e2321-152">0</span></span>  <br/> |<span data-ttu-id="e2321-153">240</span><span class="sxs-lookup"><span data-stu-id="e2321-153">240</span></span>  <br/> |<span data-ttu-id="e2321-154">120</span><span class="sxs-lookup"><span data-stu-id="e2321-154">120</span></span>  <br/> |
|<span data-ttu-id="e2321-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="e2321-155">Magenta</span></span>  <br/> |<span data-ttu-id="e2321-156">200</span><span class="sxs-lookup"><span data-stu-id="e2321-156">200</span></span>  <br/> |<span data-ttu-id="e2321-157">240</span><span class="sxs-lookup"><span data-stu-id="e2321-157">240</span></span>  <br/> |<span data-ttu-id="e2321-158">120</span><span class="sxs-lookup"><span data-stu-id="e2321-158">120</span></span>  <br/> |
|<span data-ttu-id="e2321-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="e2321-159">Yellow</span></span>  <br/> |<span data-ttu-id="e2321-160">40</span><span class="sxs-lookup"><span data-stu-id="e2321-160">40</span></span>  <br/> |<span data-ttu-id="e2321-161">240</span><span class="sxs-lookup"><span data-stu-id="e2321-161">240</span></span>  <br/> |<span data-ttu-id="e2321-162">120</span><span class="sxs-lookup"><span data-stu-id="e2321-162">120</span></span>  <br/> |
|<span data-ttu-id="e2321-163">Белый</span><span class="sxs-lookup"><span data-stu-id="e2321-163">White</span></span>  <br/> |<span data-ttu-id="e2321-164">0</span><span class="sxs-lookup"><span data-stu-id="e2321-164">0</span></span>  <br/> |<span data-ttu-id="e2321-165">0</span><span class="sxs-lookup"><span data-stu-id="e2321-165">0</span></span>  <br/> |<span data-ttu-id="e2321-166">240</span><span class="sxs-lookup"><span data-stu-id="e2321-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="e2321-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2321-167">Example 1</span></span>

<span data-ttu-id="e2321-168">HSL(160 240 120)</span><span class="sxs-lookup"><span data-stu-id="e2321-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="e2321-169">Возвращает индекс синего цвета.</span><span class="sxs-lookup"><span data-stu-id="e2321-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e2321-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2321-170">Example 2</span></span>

<span data-ttu-id="e2321-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="e2321-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="e2321-172">Возвращает индекс цвета, который зеркально отражает цвет переднего плана заливки с повышенной luminosity.</span><span class="sxs-lookup"><span data-stu-id="e2321-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

