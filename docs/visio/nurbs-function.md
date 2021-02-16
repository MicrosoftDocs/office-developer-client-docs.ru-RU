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
description: Возвращает несвязавный логический B-spline (NURBS). Эта функция используется в ячейке E в геометрических строках NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438458"
---
# <a name="nurbs-function"></a><span data-ttu-id="286f0-104">Функция NURBS</span><span class="sxs-lookup"><span data-stu-id="286f0-104">NURBS Function</span></span>

<span data-ttu-id="286f0-105">Возвращает несвязавный логический B-spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="286f0-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="286f0-106">Эта функция используется в ячейке E в геометрических строках NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="286f0-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="286f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="286f0-107">Syntax</span></span>

<span data-ttu-id="286f0-108">NURBS(\*\* *etcLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\*т1 \*\*, \*\* *weight1* \*\*, ...) </span><span class="sxs-lookup"><span data-stu-id="286f0-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="286f0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="286f0-109">Parameters</span></span>

|<span data-ttu-id="286f0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="286f0-110">**Name**</span></span>|<span data-ttu-id="286f0-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="286f0-111">**Required/Optional**</span></span>|<span data-ttu-id="286f0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="286f0-112">**Data Type**</span></span>|<span data-ttu-id="286f0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="286f0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="286f0-114">_last_</span><span class="sxs-lookup"><span data-stu-id="286f0-114">_knotLast_</span></span> <br/> |<span data-ttu-id="286f0-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="286f0-115">Required</span></span>  <br/> |<span data-ttu-id="286f0-116">**строка**</span><span class="sxs-lookup"><span data-stu-id="286f0-116">**string**</span></span> <br/> | <span data-ttu-id="286f0-117">Последняя ветвь.</span><span class="sxs-lookup"><span data-stu-id="286f0-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="286f0-118">_degree_</span><span class="sxs-lookup"><span data-stu-id="286f0-118">_degree_</span></span> <br/> |<span data-ttu-id="286f0-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="286f0-119">Required</span></span>  <br/> |<span data-ttu-id="286f0-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="286f0-120">**Numeric**</span></span> <br/> |<span data-ttu-id="286f0-121">Степень spline.</span><span class="sxs-lookup"><span data-stu-id="286f0-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="286f0-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="286f0-122">_xType_</span></span> <br/> |<span data-ttu-id="286f0-123">Обязательна</span><span class="sxs-lookup"><span data-stu-id="286f0-123">Required</span></span>  <br/> |<span data-ttu-id="286f0-124">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="286f0-124">**Numeric**</span></span> <br/> |<span data-ttu-id="286f0-125">Указывает, как интерпретировать _входные данные x._</span><span class="sxs-lookup"><span data-stu-id="286f0-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="286f0-126">Если  _xType_ имеет 0, все входные  _данные x_ интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="286f0-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="286f0-127">Если  _xType_ имеет 1, все  _входные данные x_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="286f0-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="286f0-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="286f0-128">_yType_</span></span> <br/> |<span data-ttu-id="286f0-129">Обязательна</span><span class="sxs-lookup"><span data-stu-id="286f0-129">Required</span></span>  <br/> |<span data-ttu-id="286f0-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="286f0-130">**Numeric**</span></span> <br/> |<span data-ttu-id="286f0-131">Указывает, как интерпретировать _входные данные y._</span><span class="sxs-lookup"><span data-stu-id="286f0-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="286f0-132">Если  _yType_ имеет 0, все входные  _данные Y_ интерпретируются как процент высоты.</span><span class="sxs-lookup"><span data-stu-id="286f0-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="286f0-133">Если  _yType_ имеет 1, все входные  _данные Y_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="286f0-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="286f0-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="286f0-134">_x1_</span></span> <br/> |<span data-ttu-id="286f0-135">Обязательно</span><span class="sxs-lookup"><span data-stu-id="286f0-135">Required</span></span>  <br/> |<span data-ttu-id="286f0-136">**Строка**</span><span class="sxs-lookup"><span data-stu-id="286f0-136">**String**</span></span> <br/> |<span data-ttu-id="286f0-137">X-координата.</span><span class="sxs-lookup"><span data-stu-id="286f0-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="286f0-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="286f0-138">_y1_</span></span> <br/> |<span data-ttu-id="286f0-139">Обязательно</span><span class="sxs-lookup"><span data-stu-id="286f0-139">Required</span></span>  <br/> |<span data-ttu-id="286f0-140">**Строка**</span><span class="sxs-lookup"><span data-stu-id="286f0-140">**String**</span></span> <br/> |<span data-ttu-id="286f0-141">Координата Y.</span><span class="sxs-lookup"><span data-stu-id="286f0-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="286f0-142">_1_</span><span class="sxs-lookup"><span data-stu-id="286f0-142">_knot1_</span></span> <br/> |<span data-ttu-id="286f0-143">Обязательно</span><span class="sxs-lookup"><span data-stu-id="286f0-143">Required</span></span>  <br/> |<span data-ttu-id="286f0-144">**Строка**</span><span class="sxs-lookup"><span data-stu-id="286f0-144">**String**</span></span> <br/> |<span data-ttu-id="286f0-145">Заметь на B-spline.</span><span class="sxs-lookup"><span data-stu-id="286f0-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="286f0-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="286f0-146">_weight1_</span></span> <br/> |<span data-ttu-id="286f0-147">Обязательно</span><span class="sxs-lookup"><span data-stu-id="286f0-147">Required</span></span>  <br/> |<span data-ttu-id="286f0-148">**Строка**</span><span class="sxs-lookup"><span data-stu-id="286f0-148">**String**</span></span> <br/> |<span data-ttu-id="286f0-149">Вес на B-spline.</span><span class="sxs-lookup"><span data-stu-id="286f0-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="286f0-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="286f0-150">Remarks</span></span>

<span data-ttu-id="286f0-151">Для каждого  *аргумента x*  должен быть аргумент  *y;*  в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="286f0-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="286f0-152">Необходимо указать по крайней мере один  *аргумент x*, *y*, *argument и*  *weight;*  в противном случае Visio возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="286f0-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

