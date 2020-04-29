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
description: Возвращает значение, представляющее индекс в цветовой палитре документа. Он определяет цвет с помощью красного, зеленого и синего компонентов, каждый из которых является числом в диапазоне от 0 до 255 включительно, или выражение, результатом которого является такое число.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426305"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="10d60-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="10d60-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="10d60-105">Возвращает значение, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="10d60-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="10d60-106">Он определяет цвет с помощью красного, зеленого и синего компонентов, каждый из которых является числом в диапазоне от 0 до 255 включительно, или выражение, результатом которого является такое число.</span><span class="sxs-lookup"><span data-stu-id="10d60-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="10d60-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10d60-107">Syntax</span></span>

<span data-ttu-id="10d60-108">RGB (\* \* *Red* \* \*, \* \* *Green* \* \*, \* \* *Blue* \* \*)</span><span class="sxs-lookup"><span data-stu-id="10d60-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="10d60-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="10d60-109">Parameters</span></span>

|<span data-ttu-id="10d60-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="10d60-110">**Name**</span></span>|<span data-ttu-id="10d60-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="10d60-111">**Required/Optional**</span></span>|<span data-ttu-id="10d60-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="10d60-112">**Data Type**</span></span>|<span data-ttu-id="10d60-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10d60-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="10d60-114">_отображаем_</span><span class="sxs-lookup"><span data-stu-id="10d60-114">_red_</span></span> <br/> |<span data-ttu-id="10d60-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="10d60-115">Required</span></span>  <br/> |<span data-ttu-id="10d60-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="10d60-116">**Number**</span></span> <br/> |<span data-ttu-id="10d60-117">Красный компонент.</span><span class="sxs-lookup"><span data-stu-id="10d60-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="10d60-118">_Интенсив_</span><span class="sxs-lookup"><span data-stu-id="10d60-118">_green_</span></span> <br/> |<span data-ttu-id="10d60-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="10d60-119">Required</span></span>  <br/> |<span data-ttu-id="10d60-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="10d60-120">**Number**</span></span> <br/> |<span data-ttu-id="10d60-121">Зеленый компонент.</span><span class="sxs-lookup"><span data-stu-id="10d60-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="10d60-122">_компонентов_</span><span class="sxs-lookup"><span data-stu-id="10d60-122">_blue_</span></span> <br/> |<span data-ttu-id="10d60-123">Обязательна</span><span class="sxs-lookup"><span data-stu-id="10d60-123">Required</span></span>  <br/> |<span data-ttu-id="10d60-124">**нмбер**</span><span class="sxs-lookup"><span data-stu-id="10d60-124">**Nmber**</span></span> <br/> |<span data-ttu-id="10d60-125">Синий компонент.</span><span class="sxs-lookup"><span data-stu-id="10d60-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="10d60-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10d60-126">Return value</span></span>

<span data-ttu-id="10d60-127">Номер</span><span class="sxs-lookup"><span data-stu-id="10d60-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10d60-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="10d60-128">Remarks</span></span>

<span data-ttu-id="10d60-129">Если цвет, возвращенный функцией, еще не существует в цветовой палитре текущего документа, он добавляется в палитру.</span><span class="sxs-lookup"><span data-stu-id="10d60-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="10d60-130">В приведенной ниже таблице перечислены некоторые стандартные цвета и их значения красного, зеленого и синего цвета.</span><span class="sxs-lookup"><span data-stu-id="10d60-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="10d60-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="10d60-131">**Color**</span></span>|<span data-ttu-id="10d60-132">**Значение красного**</span><span class="sxs-lookup"><span data-stu-id="10d60-132">**Red value**</span></span>|<span data-ttu-id="10d60-133">**Значение зеленого**</span><span class="sxs-lookup"><span data-stu-id="10d60-133">**Green value**</span></span>|<span data-ttu-id="10d60-134">**Значение синего**</span><span class="sxs-lookup"><span data-stu-id="10d60-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10d60-135">Черный</span><span class="sxs-lookup"><span data-stu-id="10d60-135">Black</span></span>  <br/> |<span data-ttu-id="10d60-136">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-136">0</span></span>  <br/> |<span data-ttu-id="10d60-137">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-137">0</span></span>  <br/> |<span data-ttu-id="10d60-138">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-138">0</span></span>  <br/> |
|<span data-ttu-id="10d60-139">Синий</span><span class="sxs-lookup"><span data-stu-id="10d60-139">Blue</span></span>  <br/> |<span data-ttu-id="10d60-140">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-140">0</span></span>  <br/> |<span data-ttu-id="10d60-141">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-141">0</span></span>  <br/> |<span data-ttu-id="10d60-142">255</span><span class="sxs-lookup"><span data-stu-id="10d60-142">255</span></span>  <br/> |
|<span data-ttu-id="10d60-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="10d60-143">Green</span></span>  <br/> |<span data-ttu-id="10d60-144">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-144">0</span></span>  <br/> |<span data-ttu-id="10d60-145">255</span><span class="sxs-lookup"><span data-stu-id="10d60-145">255</span></span>  <br/> |<span data-ttu-id="10d60-146">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-146">0</span></span>  <br/> |
|<span data-ttu-id="10d60-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="10d60-147">Cyan</span></span>  <br/> |<span data-ttu-id="10d60-148">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-148">0</span></span>  <br/> |<span data-ttu-id="10d60-149">255</span><span class="sxs-lookup"><span data-stu-id="10d60-149">255</span></span>  <br/> |<span data-ttu-id="10d60-150">255</span><span class="sxs-lookup"><span data-stu-id="10d60-150">255</span></span>  <br/> |
|<span data-ttu-id="10d60-151">Красный</span><span class="sxs-lookup"><span data-stu-id="10d60-151">Red</span></span>  <br/> |<span data-ttu-id="10d60-152">255</span><span class="sxs-lookup"><span data-stu-id="10d60-152">255</span></span>  <br/> |<span data-ttu-id="10d60-153">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-153">0</span></span>  <br/> |<span data-ttu-id="10d60-154">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-154">0</span></span>  <br/> |
|<span data-ttu-id="10d60-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="10d60-155">Magenta</span></span>  <br/> |<span data-ttu-id="10d60-156">255</span><span class="sxs-lookup"><span data-stu-id="10d60-156">255</span></span>  <br/> |<span data-ttu-id="10d60-157">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-157">0</span></span>  <br/> |<span data-ttu-id="10d60-158">255</span><span class="sxs-lookup"><span data-stu-id="10d60-158">255</span></span>  <br/> |
|<span data-ttu-id="10d60-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="10d60-159">Yellow</span></span>  <br/> |<span data-ttu-id="10d60-160">255</span><span class="sxs-lookup"><span data-stu-id="10d60-160">255</span></span>  <br/> |<span data-ttu-id="10d60-161">255</span><span class="sxs-lookup"><span data-stu-id="10d60-161">255</span></span>  <br/> |<span data-ttu-id="10d60-162">нуль</span><span class="sxs-lookup"><span data-stu-id="10d60-162">0</span></span>  <br/> |
|<span data-ttu-id="10d60-163">Белый</span><span class="sxs-lookup"><span data-stu-id="10d60-163">White</span></span>  <br/> |<span data-ttu-id="10d60-164">255</span><span class="sxs-lookup"><span data-stu-id="10d60-164">255</span></span>  <br/> |<span data-ttu-id="10d60-165">255</span><span class="sxs-lookup"><span data-stu-id="10d60-165">255</span></span>  <br/> |<span data-ttu-id="10d60-166">255</span><span class="sxs-lookup"><span data-stu-id="10d60-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="10d60-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10d60-167">Example 1</span></span>

<span data-ttu-id="10d60-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="10d60-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="10d60-169">Возвращает индекс для синего цвета.</span><span class="sxs-lookup"><span data-stu-id="10d60-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="10d60-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10d60-170">Example 2</span></span>

<span data-ttu-id="10d60-171">RGB (красный (sheet. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="10d60-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="10d60-172">Возвращает индекс цвета, для которого отображается лист с красными зеркалами. 1's Заливка переднего плана.</span><span class="sxs-lookup"><span data-stu-id="10d60-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

