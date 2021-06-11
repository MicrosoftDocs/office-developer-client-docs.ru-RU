---
title: Функция NURBS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Возвращает неоформленную рациональную B-spline (NURBS). Эта функция используется в ячейке E в строках геометрии NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438458"
---
# <a name="nurbs-function"></a><span data-ttu-id="e4ae5-104">Функция NURBS</span><span class="sxs-lookup"><span data-stu-id="e4ae5-104">NURBS Function</span></span>

<span data-ttu-id="e4ae5-105">Возвращает неоформленную рациональную B-spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="e4ae5-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="e4ae5-106">Эта функция используется в ячейке E в строках геометрии NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e4ae5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4ae5-107">Syntax</span></span>

<span data-ttu-id="e4ae5-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span><span class="sxs-lookup"><span data-stu-id="e4ae5-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4ae5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4ae5-109">Parameters</span></span>

|<span data-ttu-id="e4ae5-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-110">**Name**</span></span>|<span data-ttu-id="e4ae5-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-111">**Required/Optional**</span></span>|<span data-ttu-id="e4ae5-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-112">**Data Type**</span></span>|<span data-ttu-id="e4ae5-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4ae5-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-114">_knotLast_</span></span> <br/> |<span data-ttu-id="e4ae5-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-115">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-116">**строка**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-116">**string**</span></span> <br/> | <span data-ttu-id="e4ae5-117">Последний узел.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-118">_степень_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-118">_degree_</span></span> <br/> |<span data-ttu-id="e4ae5-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-119">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-120">**Numeric**</span></span> <br/> |<span data-ttu-id="e4ae5-121">Степень spline.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-122">_xType_</span></span> <br/> |<span data-ttu-id="e4ae5-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-123">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-124">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-124">**Numeric**</span></span> <br/> |<span data-ttu-id="e4ae5-125">Указывает, как интерпретировать _данные ввода x._</span><span class="sxs-lookup"><span data-stu-id="e4ae5-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="e4ae5-126">Если  _xType_ — 0, все  _данные ввода x_ интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="e4ae5-127">Если  _xType_ — 1, все  _данные ввода x_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-128">_yType_</span></span> <br/> |<span data-ttu-id="e4ae5-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-129">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-130">**Numeric**</span></span> <br/> |<span data-ttu-id="e4ae5-131">Указывает, как интерпретировать _данные ввода y._</span><span class="sxs-lookup"><span data-stu-id="e4ae5-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="e4ae5-132">Если  _yType_ — 0, все  _данные ввода y_ интерпретируются как процент высоты.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="e4ae5-133">Если  _yType_ — 1, все  _данные ввода y_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-134">_x1_</span></span> <br/> |<span data-ttu-id="e4ae5-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-135">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-136">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-136">**String**</span></span> <br/> |<span data-ttu-id="e4ae5-137">X-coordinate.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-138">_y1_</span></span> <br/> |<span data-ttu-id="e4ae5-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-139">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-140">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-140">**String**</span></span> <br/> |<span data-ttu-id="e4ae5-141">y-coordinate.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-142">_knot1_</span></span> <br/> |<span data-ttu-id="e4ae5-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-143">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-144">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-144">**String**</span></span> <br/> |<span data-ttu-id="e4ae5-145">Узел на B-spline.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="e4ae5-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="e4ae5-146">_weight1_</span></span> <br/> |<span data-ttu-id="e4ae5-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4ae5-147">Required</span></span>  <br/> |<span data-ttu-id="e4ae5-148">**String**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-148">**String**</span></span> <br/> |<span data-ttu-id="e4ae5-149">Вес на B-spline.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4ae5-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4ae5-150">Remarks</span></span>

<span data-ttu-id="e4ae5-151">Для каждого  *аргумента x*  должен быть  *аргумент y;*  в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="e4ae5-152">Необходимо указать по крайней мере один *аргумент x*, *y*, *узел* и *вес;* в противном Visio возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

