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
description: Возвращает значение, представляющее индекс в цветовой палитре документа. Он указывает цвет по своим красным, зеленым и синим компонентам, где каждый из них имеет число в диапазоне от 0 до 255 включительно или выражение, которое оценивается до такого числа.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426305"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="56fcb-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="56fcb-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="56fcb-105">Возвращает значение, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="56fcb-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="56fcb-106">Он указывает цвет по своим красным, зеленым и синим компонентам, где каждый из них имеет число в диапазоне от 0 до 255 включительно или выражение, которое оценивается до такого числа.</span><span class="sxs-lookup"><span data-stu-id="56fcb-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="56fcb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56fcb-107">Syntax</span></span>

<span data-ttu-id="56fcb-108">RGB(\*\* *красный* \*\*, \*\* *зеленый* \*\*, \*\* *синий* \*\* )</span><span class="sxs-lookup"><span data-stu-id="56fcb-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="56fcb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="56fcb-109">Parameters</span></span>

|<span data-ttu-id="56fcb-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="56fcb-110">**Name**</span></span>|<span data-ttu-id="56fcb-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="56fcb-111">**Required/Optional**</span></span>|<span data-ttu-id="56fcb-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="56fcb-112">**Data Type**</span></span>|<span data-ttu-id="56fcb-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56fcb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="56fcb-114">_красный_</span><span class="sxs-lookup"><span data-stu-id="56fcb-114">_red_</span></span> <br/> |<span data-ttu-id="56fcb-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56fcb-115">Required</span></span>  <br/> |<span data-ttu-id="56fcb-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="56fcb-116">**Number**</span></span> <br/> |<span data-ttu-id="56fcb-117">Красный компонент.</span><span class="sxs-lookup"><span data-stu-id="56fcb-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="56fcb-118">_зеленый цвет_</span><span class="sxs-lookup"><span data-stu-id="56fcb-118">_green_</span></span> <br/> |<span data-ttu-id="56fcb-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56fcb-119">Required</span></span>  <br/> |<span data-ttu-id="56fcb-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="56fcb-120">**Number**</span></span> <br/> |<span data-ttu-id="56fcb-121">Зеленый компонент.</span><span class="sxs-lookup"><span data-stu-id="56fcb-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="56fcb-122">_синий_</span><span class="sxs-lookup"><span data-stu-id="56fcb-122">_blue_</span></span> <br/> |<span data-ttu-id="56fcb-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="56fcb-123">Required</span></span>  <br/> |<span data-ttu-id="56fcb-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="56fcb-124">**Nmber**</span></span> <br/> |<span data-ttu-id="56fcb-125">Синий компонент.</span><span class="sxs-lookup"><span data-stu-id="56fcb-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="56fcb-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56fcb-126">Return value</span></span>

<span data-ttu-id="56fcb-127">Номер</span><span class="sxs-lookup"><span data-stu-id="56fcb-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56fcb-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="56fcb-128">Remarks</span></span>

<span data-ttu-id="56fcb-129">Если цвет, возвращаемый функцией, еще не существует в цветовой палитре текущего документа, он добавляется в палитру.</span><span class="sxs-lookup"><span data-stu-id="56fcb-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="56fcb-130">В следующей таблице перечислены некоторые стандартные цвета и их красные, зеленые и синие значения.</span><span class="sxs-lookup"><span data-stu-id="56fcb-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="56fcb-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="56fcb-131">**Color**</span></span>|<span data-ttu-id="56fcb-132">**Красное значение**</span><span class="sxs-lookup"><span data-stu-id="56fcb-132">**Red value**</span></span>|<span data-ttu-id="56fcb-133">**Зеленое значение**</span><span class="sxs-lookup"><span data-stu-id="56fcb-133">**Green value**</span></span>|<span data-ttu-id="56fcb-134">**Синее значение**</span><span class="sxs-lookup"><span data-stu-id="56fcb-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="56fcb-135">Черный</span><span class="sxs-lookup"><span data-stu-id="56fcb-135">Black</span></span>  <br/> |<span data-ttu-id="56fcb-136">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-136">0</span></span>  <br/> |<span data-ttu-id="56fcb-137">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-137">0</span></span>  <br/> |<span data-ttu-id="56fcb-138">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-138">0</span></span>  <br/> |
|<span data-ttu-id="56fcb-139">Синий</span><span class="sxs-lookup"><span data-stu-id="56fcb-139">Blue</span></span>  <br/> |<span data-ttu-id="56fcb-140">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-140">0</span></span>  <br/> |<span data-ttu-id="56fcb-141">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-141">0</span></span>  <br/> |<span data-ttu-id="56fcb-142">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-142">255</span></span>  <br/> |
|<span data-ttu-id="56fcb-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="56fcb-143">Green</span></span>  <br/> |<span data-ttu-id="56fcb-144">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-144">0</span></span>  <br/> |<span data-ttu-id="56fcb-145">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-145">255</span></span>  <br/> |<span data-ttu-id="56fcb-146">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-146">0</span></span>  <br/> |
|<span data-ttu-id="56fcb-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="56fcb-147">Cyan</span></span>  <br/> |<span data-ttu-id="56fcb-148">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-148">0</span></span>  <br/> |<span data-ttu-id="56fcb-149">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-149">255</span></span>  <br/> |<span data-ttu-id="56fcb-150">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-150">255</span></span>  <br/> |
|<span data-ttu-id="56fcb-151">Красный</span><span class="sxs-lookup"><span data-stu-id="56fcb-151">Red</span></span>  <br/> |<span data-ttu-id="56fcb-152">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-152">255</span></span>  <br/> |<span data-ttu-id="56fcb-153">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-153">0</span></span>  <br/> |<span data-ttu-id="56fcb-154">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-154">0</span></span>  <br/> |
|<span data-ttu-id="56fcb-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="56fcb-155">Magenta</span></span>  <br/> |<span data-ttu-id="56fcb-156">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-156">255</span></span>  <br/> |<span data-ttu-id="56fcb-157">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-157">0</span></span>  <br/> |<span data-ttu-id="56fcb-158">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-158">255</span></span>  <br/> |
|<span data-ttu-id="56fcb-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="56fcb-159">Yellow</span></span>  <br/> |<span data-ttu-id="56fcb-160">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-160">255</span></span>  <br/> |<span data-ttu-id="56fcb-161">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-161">255</span></span>  <br/> |<span data-ttu-id="56fcb-162">0</span><span class="sxs-lookup"><span data-stu-id="56fcb-162">0</span></span>  <br/> |
|<span data-ttu-id="56fcb-163">Белый</span><span class="sxs-lookup"><span data-stu-id="56fcb-163">White</span></span>  <br/> |<span data-ttu-id="56fcb-164">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-164">255</span></span>  <br/> |<span data-ttu-id="56fcb-165">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-165">255</span></span>  <br/> |<span data-ttu-id="56fcb-166">255</span><span class="sxs-lookup"><span data-stu-id="56fcb-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="56fcb-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56fcb-167">Example 1</span></span>

<span data-ttu-id="56fcb-168">RGB (0,0,255)</span><span class="sxs-lookup"><span data-stu-id="56fcb-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="56fcb-169">Возвращает индекс для синего цвета.</span><span class="sxs-lookup"><span data-stu-id="56fcb-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="56fcb-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="56fcb-170">Example 2</span></span>

<span data-ttu-id="56fcb-171">RGB(RED(Sheet.1! FillForegnd),120,0)</span><span class="sxs-lookup"><span data-stu-id="56fcb-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="56fcb-172">Возвращает индекс для цвета, красный компонент которого отражает на переднем плане заполнения Sheet.1.</span><span class="sxs-lookup"><span data-stu-id="56fcb-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

