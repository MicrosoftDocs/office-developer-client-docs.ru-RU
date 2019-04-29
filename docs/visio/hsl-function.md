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
description: Возвращает значение, представляющее индекс в цветовой палитре документа. Он определяет цвет с помощью компонентов тона, насыщенности и яркости.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420964"
---
# <a name="hsl-function"></a><span data-ttu-id="8256b-104">Функция HSL</span><span class="sxs-lookup"><span data-stu-id="8256b-104">HSL Function</span></span>

<span data-ttu-id="8256b-105">Возвращает значение, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="8256b-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="8256b-106">Он определяет цвет с помощью компонентов тона, насыщенности и яркости.</span><span class="sxs-lookup"><span data-stu-id="8256b-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8256b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8256b-107">Syntax</span></span>

<span data-ttu-id="8256b-108">HSL (\* \* *тон* \* \*, \* \* *насыщенность* \* \*, \* \* *яркость* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8256b-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8256b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8256b-109">Parameters</span></span>

|<span data-ttu-id="8256b-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8256b-110">**Name**</span></span>|<span data-ttu-id="8256b-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8256b-111">**Required/Optional**</span></span>|<span data-ttu-id="8256b-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8256b-112">**Data Type**</span></span>|<span data-ttu-id="8256b-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8256b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8256b-114">_тона_</span><span class="sxs-lookup"><span data-stu-id="8256b-114">_hue_</span></span> <br/> |<span data-ttu-id="8256b-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8256b-115">Required</span></span>  <br/> |<span data-ttu-id="8256b-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="8256b-116">**Number**</span></span> <br/> |<span data-ttu-id="8256b-117">Оттенок цвета, выраженный как число в диапазоне от 0 до 239 включительно или выражение, результатом которого является такое число.</span><span class="sxs-lookup"><span data-stu-id="8256b-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="8256b-118">_насыщенность_</span><span class="sxs-lookup"><span data-stu-id="8256b-118">_saturation_</span></span> <br/> |<span data-ttu-id="8256b-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8256b-119">Required</span></span>  <br/> |<span data-ttu-id="8256b-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="8256b-120">**Number**</span></span> <br/> |<span data-ttu-id="8256b-121">Насыщенность цвета, выраженная в виде числа в диапазоне от 0 до 240 включительно или выражение, результатом которого является такое число.</span><span class="sxs-lookup"><span data-stu-id="8256b-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="8256b-122">_яркости_</span><span class="sxs-lookup"><span data-stu-id="8256b-122">_luminosity_</span></span> <br/> |<span data-ttu-id="8256b-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8256b-123">Required</span></span>  <br/> |<span data-ttu-id="8256b-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="8256b-124">**Number**</span></span> <br/> | <span data-ttu-id="8256b-125">Яркость цвета, выраженная в виде числа в диапазоне от 0 до 240 включительно или выражение, результатом которого является такое число.</span><span class="sxs-lookup"><span data-stu-id="8256b-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8256b-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8256b-126">Return value</span></span>

<span data-ttu-id="8256b-127">Число</span><span class="sxs-lookup"><span data-stu-id="8256b-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8256b-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="8256b-128">Remarks</span></span>

<span data-ttu-id="8256b-129">Если цвет, возвращенный функцией, еще не существует в цветовой палитре текущего документа, он добавляется в список доступных цветов документа.</span><span class="sxs-lookup"><span data-stu-id="8256b-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="8256b-130">В приведенной ниже таблице перечислены некоторые стандартные цвета и значения тона, насыщенности и яркости.</span><span class="sxs-lookup"><span data-stu-id="8256b-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="8256b-131">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="8256b-131">**Color**</span></span>|<span data-ttu-id="8256b-132">**Значение тона**</span><span class="sxs-lookup"><span data-stu-id="8256b-132">**Hue value**</span></span>|<span data-ttu-id="8256b-133">**Значение насыщенности**</span><span class="sxs-lookup"><span data-stu-id="8256b-133">**Saturation value**</span></span>|<span data-ttu-id="8256b-134">**Значение яркости**</span><span class="sxs-lookup"><span data-stu-id="8256b-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8256b-135">Черный</span><span class="sxs-lookup"><span data-stu-id="8256b-135">Black</span></span>  <br/> |<span data-ttu-id="8256b-136">нуль</span><span class="sxs-lookup"><span data-stu-id="8256b-136">0</span></span>  <br/> |<span data-ttu-id="8256b-137">нуль</span><span class="sxs-lookup"><span data-stu-id="8256b-137">0</span></span>  <br/> |<span data-ttu-id="8256b-138">открыт</span><span class="sxs-lookup"><span data-stu-id="8256b-138">24</span></span>  <br/> |
|<span data-ttu-id="8256b-139">Синий</span><span class="sxs-lookup"><span data-stu-id="8256b-139">Blue</span></span>  <br/> |<span data-ttu-id="8256b-140">160</span><span class="sxs-lookup"><span data-stu-id="8256b-140">160</span></span>  <br/> |<span data-ttu-id="8256b-141">240</span><span class="sxs-lookup"><span data-stu-id="8256b-141">240</span></span>  <br/> |<span data-ttu-id="8256b-142">120</span><span class="sxs-lookup"><span data-stu-id="8256b-142">120</span></span>  <br/> |
|<span data-ttu-id="8256b-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="8256b-143">Green</span></span>  <br/> |<span data-ttu-id="8256b-144">80</span><span class="sxs-lookup"><span data-stu-id="8256b-144">80</span></span>  <br/> |<span data-ttu-id="8256b-145">240</span><span class="sxs-lookup"><span data-stu-id="8256b-145">240</span></span>  <br/> |<span data-ttu-id="8256b-146">120</span><span class="sxs-lookup"><span data-stu-id="8256b-146">120</span></span>  <br/> |
|<span data-ttu-id="8256b-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="8256b-147">Cyan</span></span>  <br/> |<span data-ttu-id="8256b-148">120</span><span class="sxs-lookup"><span data-stu-id="8256b-148">120</span></span>  <br/> |<span data-ttu-id="8256b-149">240</span><span class="sxs-lookup"><span data-stu-id="8256b-149">240</span></span>  <br/> |<span data-ttu-id="8256b-150">120</span><span class="sxs-lookup"><span data-stu-id="8256b-150">120</span></span>  <br/> |
|<span data-ttu-id="8256b-151">Красный</span><span class="sxs-lookup"><span data-stu-id="8256b-151">Red</span></span>  <br/> |<span data-ttu-id="8256b-152">нуль</span><span class="sxs-lookup"><span data-stu-id="8256b-152">0</span></span>  <br/> |<span data-ttu-id="8256b-153">240</span><span class="sxs-lookup"><span data-stu-id="8256b-153">240</span></span>  <br/> |<span data-ttu-id="8256b-154">120</span><span class="sxs-lookup"><span data-stu-id="8256b-154">120</span></span>  <br/> |
|<span data-ttu-id="8256b-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="8256b-155">Magenta</span></span>  <br/> |<span data-ttu-id="8256b-156">200</span><span class="sxs-lookup"><span data-stu-id="8256b-156">200</span></span>  <br/> |<span data-ttu-id="8256b-157">240</span><span class="sxs-lookup"><span data-stu-id="8256b-157">240</span></span>  <br/> |<span data-ttu-id="8256b-158">120</span><span class="sxs-lookup"><span data-stu-id="8256b-158">120</span></span>  <br/> |
|<span data-ttu-id="8256b-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="8256b-159">Yellow</span></span>  <br/> |<span data-ttu-id="8256b-160">40</span><span class="sxs-lookup"><span data-stu-id="8256b-160">40</span></span>  <br/> |<span data-ttu-id="8256b-161">240</span><span class="sxs-lookup"><span data-stu-id="8256b-161">240</span></span>  <br/> |<span data-ttu-id="8256b-162">120</span><span class="sxs-lookup"><span data-stu-id="8256b-162">120</span></span>  <br/> |
|<span data-ttu-id="8256b-163">Белый</span><span class="sxs-lookup"><span data-stu-id="8256b-163">White</span></span>  <br/> |<span data-ttu-id="8256b-164">нуль</span><span class="sxs-lookup"><span data-stu-id="8256b-164">0</span></span>  <br/> |<span data-ttu-id="8256b-165">нуль</span><span class="sxs-lookup"><span data-stu-id="8256b-165">0</span></span>  <br/> |<span data-ttu-id="8256b-166">240</span><span class="sxs-lookup"><span data-stu-id="8256b-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="8256b-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8256b-167">Example 1</span></span>

<span data-ttu-id="8256b-168">HSL (160240120)</span><span class="sxs-lookup"><span data-stu-id="8256b-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="8256b-169">Возвращает индекс для синего цвета.</span><span class="sxs-lookup"><span data-stu-id="8256b-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8256b-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8256b-170">Example 2</span></span>

<span data-ttu-id="8256b-171">HSL (отТЕНОК (FillForegnd), Кот (FillForegnd), MIN (яркость (FillForegnd) + 100240))</span><span class="sxs-lookup"><span data-stu-id="8256b-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="8256b-172">Возвращает индекс цвета, который отражает цвет переднего плана заливки с увеличенной яркостью.</span><span class="sxs-lookup"><span data-stu-id="8256b-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

