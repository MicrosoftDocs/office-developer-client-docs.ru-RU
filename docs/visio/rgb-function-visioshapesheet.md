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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326742"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="df602-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="df602-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="df602-105">Возвращает значение, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="df602-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="df602-106">Он определяет цвет с помощью красного, зеленого и синего компонентов, каждый из которых является числом в диапазоне от 0 до 255 включительно, или выражение, результатом которого является такое число.</span><span class="sxs-lookup"><span data-stu-id="df602-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df602-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df602-107">Syntax</span></span>

<span data-ttu-id="df602-108">RGB (\* \* *Red* \* \*, \* \* *Green* \* \*, \* \* *Blue* \* \*)</span><span class="sxs-lookup"><span data-stu-id="df602-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df602-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df602-109">Parameters</span></span>

|<span data-ttu-id="df602-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="df602-110">**Name**</span></span>|<span data-ttu-id="df602-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="df602-111">**Required/Optional**</span></span>|<span data-ttu-id="df602-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="df602-112">**Data Type**</span></span>|<span data-ttu-id="df602-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df602-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df602-114">_отображаем_</span><span class="sxs-lookup"><span data-stu-id="df602-114">_red_</span></span> <br/> |<span data-ttu-id="df602-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df602-115">Required</span></span>  <br/> |<span data-ttu-id="df602-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="df602-116">**Number**</span></span> <br/> |<span data-ttu-id="df602-117">Красный компонент.</span><span class="sxs-lookup"><span data-stu-id="df602-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="df602-118">_Интенсив_</span><span class="sxs-lookup"><span data-stu-id="df602-118">_green_</span></span> <br/> |<span data-ttu-id="df602-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df602-119">Required</span></span>  <br/> |<span data-ttu-id="df602-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="df602-120">**Number**</span></span> <br/> |<span data-ttu-id="df602-121">Зеленый компонент.</span><span class="sxs-lookup"><span data-stu-id="df602-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="df602-122">_компонентов_</span><span class="sxs-lookup"><span data-stu-id="df602-122">_blue_</span></span> <br/> |<span data-ttu-id="df602-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df602-123">Required</span></span>  <br/> |<span data-ttu-id="df602-124">**Нмбер**</span><span class="sxs-lookup"><span data-stu-id="df602-124">**Nmber**</span></span> <br/> |<span data-ttu-id="df602-125">Синий компонент.</span><span class="sxs-lookup"><span data-stu-id="df602-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df602-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df602-126">Return value</span></span>

<span data-ttu-id="df602-127">Номер</span><span class="sxs-lookup"><span data-stu-id="df602-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df602-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="df602-128">Remarks</span></span>

<span data-ttu-id="df602-129">Если цвет, возвращенный функцией, еще не существует в цветовой палитре текущего документа, он добавляется в палитру.</span><span class="sxs-lookup"><span data-stu-id="df602-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="df602-130">В приведенной ниже таблице перечислены некоторые стандартные цвета и их значения красного, зеленого и синего цвета.</span><span class="sxs-lookup"><span data-stu-id="df602-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="df602-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="df602-131">**Color**</span></span>|<span data-ttu-id="df602-132">**Значение красного**</span><span class="sxs-lookup"><span data-stu-id="df602-132">**Red value**</span></span>|<span data-ttu-id="df602-133">**Значение зеленого**</span><span class="sxs-lookup"><span data-stu-id="df602-133">**Green value**</span></span>|<span data-ttu-id="df602-134">**Значение синего**</span><span class="sxs-lookup"><span data-stu-id="df602-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df602-135">Черный</span><span class="sxs-lookup"><span data-stu-id="df602-135">Black</span></span>  <br/> |<span data-ttu-id="df602-136">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-136">0</span></span>  <br/> |<span data-ttu-id="df602-137">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-137">0</span></span>  <br/> |<span data-ttu-id="df602-138">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-138">0</span></span>  <br/> |
|<span data-ttu-id="df602-139">Синий</span><span class="sxs-lookup"><span data-stu-id="df602-139">Blue</span></span>  <br/> |<span data-ttu-id="df602-140">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-140">0</span></span>  <br/> |<span data-ttu-id="df602-141">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-141">0</span></span>  <br/> |<span data-ttu-id="df602-142">255</span><span class="sxs-lookup"><span data-stu-id="df602-142">255</span></span>  <br/> |
|<span data-ttu-id="df602-143">Зеленый</span><span class="sxs-lookup"><span data-stu-id="df602-143">Green</span></span>  <br/> |<span data-ttu-id="df602-144">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-144">0</span></span>  <br/> |<span data-ttu-id="df602-145">255</span><span class="sxs-lookup"><span data-stu-id="df602-145">255</span></span>  <br/> |<span data-ttu-id="df602-146">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-146">0</span></span>  <br/> |
|<span data-ttu-id="df602-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="df602-147">Cyan</span></span>  <br/> |<span data-ttu-id="df602-148">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-148">0</span></span>  <br/> |<span data-ttu-id="df602-149">255</span><span class="sxs-lookup"><span data-stu-id="df602-149">255</span></span>  <br/> |<span data-ttu-id="df602-150">255</span><span class="sxs-lookup"><span data-stu-id="df602-150">255</span></span>  <br/> |
|<span data-ttu-id="df602-151">Красный</span><span class="sxs-lookup"><span data-stu-id="df602-151">Red</span></span>  <br/> |<span data-ttu-id="df602-152">255</span><span class="sxs-lookup"><span data-stu-id="df602-152">255</span></span>  <br/> |<span data-ttu-id="df602-153">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-153">0</span></span>  <br/> |<span data-ttu-id="df602-154">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-154">0</span></span>  <br/> |
|<span data-ttu-id="df602-155">Пурпурный</span><span class="sxs-lookup"><span data-stu-id="df602-155">Magenta</span></span>  <br/> |<span data-ttu-id="df602-156">255</span><span class="sxs-lookup"><span data-stu-id="df602-156">255</span></span>  <br/> |<span data-ttu-id="df602-157">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-157">0</span></span>  <br/> |<span data-ttu-id="df602-158">255</span><span class="sxs-lookup"><span data-stu-id="df602-158">255</span></span>  <br/> |
|<span data-ttu-id="df602-159">Желтый</span><span class="sxs-lookup"><span data-stu-id="df602-159">Yellow</span></span>  <br/> |<span data-ttu-id="df602-160">255</span><span class="sxs-lookup"><span data-stu-id="df602-160">255</span></span>  <br/> |<span data-ttu-id="df602-161">255</span><span class="sxs-lookup"><span data-stu-id="df602-161">255</span></span>  <br/> |<span data-ttu-id="df602-162">нуль</span><span class="sxs-lookup"><span data-stu-id="df602-162">0</span></span>  <br/> |
|<span data-ttu-id="df602-163">Белый</span><span class="sxs-lookup"><span data-stu-id="df602-163">White</span></span>  <br/> |<span data-ttu-id="df602-164">255</span><span class="sxs-lookup"><span data-stu-id="df602-164">255</span></span>  <br/> |<span data-ttu-id="df602-165">255</span><span class="sxs-lookup"><span data-stu-id="df602-165">255</span></span>  <br/> |<span data-ttu-id="df602-166">255</span><span class="sxs-lookup"><span data-stu-id="df602-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="df602-167">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df602-167">Example 1</span></span>

<span data-ttu-id="df602-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="df602-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="df602-169">Возвращает индекс для синего цвета.</span><span class="sxs-lookup"><span data-stu-id="df602-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="df602-170">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df602-170">Example 2</span></span>

<span data-ttu-id="df602-171">RGB (красный (sheet. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="df602-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="df602-172">Возвращает индекс цвета, для которого отображается лист с красными зеркалами. 1's Заливка переднего плана.</span><span class="sxs-lookup"><span data-stu-id="df602-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

