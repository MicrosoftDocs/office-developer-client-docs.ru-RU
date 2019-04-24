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
description: Возвращает неоднородного рациональный B-сплайн (NURBS). Эта функция используется в ячейке E в строках геометрии NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340126"
---
# <a name="nurbs-function"></a><span data-ttu-id="df7a1-104">Функция NURBS</span><span class="sxs-lookup"><span data-stu-id="df7a1-104">NURBS Function</span></span>

<span data-ttu-id="df7a1-105">Возвращает неоднородного рациональный B-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="df7a1-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="df7a1-106">Эта функция используется в ячейке E в строках геометрии NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="df7a1-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="df7a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df7a1-107">Syntax</span></span>

<span data-ttu-id="df7a1-108">NURBS (\* \* *кнотласт* \* \*, \* \* *градусы* \* \*, \* \* *кстипе* \* \*, \* \* *итипе* \* \*, \* \*\* \*, \* \* \* \* \*\* \* \* \* \*, \* \* *knot1* \* \*, \* \* *weight1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="df7a1-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df7a1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df7a1-109">Parameters</span></span>

|<span data-ttu-id="df7a1-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="df7a1-110">**Name**</span></span>|<span data-ttu-id="df7a1-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="df7a1-111">**Required/Optional**</span></span>|<span data-ttu-id="df7a1-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="df7a1-112">**Data Type**</span></span>|<span data-ttu-id="df7a1-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df7a1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df7a1-114">_Кнотласт_</span><span class="sxs-lookup"><span data-stu-id="df7a1-114">_knotLast_</span></span> <br/> |<span data-ttu-id="df7a1-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-115">Required</span></span>  <br/> |<span data-ttu-id="df7a1-116">**строка**</span><span class="sxs-lookup"><span data-stu-id="df7a1-116">**string**</span></span> <br/> | <span data-ttu-id="df7a1-117">Последнее кнот.</span><span class="sxs-lookup"><span data-stu-id="df7a1-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="df7a1-118">_угол_</span><span class="sxs-lookup"><span data-stu-id="df7a1-118">_degree_</span></span> <br/> |<span data-ttu-id="df7a1-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-119">Required</span></span>  <br/> |<span data-ttu-id="df7a1-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="df7a1-120">**Numeric**</span></span> <br/> |<span data-ttu-id="df7a1-121">Степень сплайна.</span><span class="sxs-lookup"><span data-stu-id="df7a1-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="df7a1-122">_Кстипе_</span><span class="sxs-lookup"><span data-stu-id="df7a1-122">_xType_</span></span> <br/> |<span data-ttu-id="df7a1-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-123">Required</span></span>  <br/> |<span data-ttu-id="df7a1-124">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="df7a1-124">**Numeric**</span></span> <br/> |<span data-ttu-id="df7a1-125">Указывает способ интерпретации входных данных _x_ .</span><span class="sxs-lookup"><span data-stu-id="df7a1-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="df7a1-126">Если _кстипе_ имеет значение 0, все входные данные _x_ интерпретируются как процент ширины.</span><span class="sxs-lookup"><span data-stu-id="df7a1-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="df7a1-127">Если _кстипе_ имеет значение 1, все входные данные _x_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="df7a1-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="df7a1-128">_Итипе_</span><span class="sxs-lookup"><span data-stu-id="df7a1-128">_yType_</span></span> <br/> |<span data-ttu-id="df7a1-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-129">Required</span></span>  <br/> |<span data-ttu-id="df7a1-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="df7a1-130">**Numeric**</span></span> <br/> |<span data-ttu-id="df7a1-131">Указывает способ интерпретации входных данных _y_ .</span><span class="sxs-lookup"><span data-stu-id="df7a1-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="df7a1-132">Если _итипе_ имеет значение 0, все входные данные _y_ интерпретируются как процент от высоты.</span><span class="sxs-lookup"><span data-stu-id="df7a1-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="df7a1-133">Если _итипе_ имеет значение 1, все входные данные _y_ интерпретируются как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="df7a1-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="df7a1-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="df7a1-134">_x1_</span></span> <br/> |<span data-ttu-id="df7a1-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-135">Required</span></span>  <br/> |<span data-ttu-id="df7a1-136">**String**</span><span class="sxs-lookup"><span data-stu-id="df7a1-136">**String**</span></span> <br/> |<span data-ttu-id="df7a1-137">Координата x.</span><span class="sxs-lookup"><span data-stu-id="df7a1-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="df7a1-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="df7a1-138">_y1_</span></span> <br/> |<span data-ttu-id="df7a1-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-139">Required</span></span>  <br/> |<span data-ttu-id="df7a1-140">**String**</span><span class="sxs-lookup"><span data-stu-id="df7a1-140">**String**</span></span> <br/> |<span data-ttu-id="df7a1-141">Координата y.</span><span class="sxs-lookup"><span data-stu-id="df7a1-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="df7a1-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="df7a1-142">_knot1_</span></span> <br/> |<span data-ttu-id="df7a1-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-143">Required</span></span>  <br/> |<span data-ttu-id="df7a1-144">**String**</span><span class="sxs-lookup"><span data-stu-id="df7a1-144">**String**</span></span> <br/> |<span data-ttu-id="df7a1-145">Объект кнот на B — сплайн.</span><span class="sxs-lookup"><span data-stu-id="df7a1-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="df7a1-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="df7a1-146">_weight1_</span></span> <br/> |<span data-ttu-id="df7a1-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df7a1-147">Required</span></span>  <br/> |<span data-ttu-id="df7a1-148">**String**</span><span class="sxs-lookup"><span data-stu-id="df7a1-148">**String**</span></span> <br/> |<span data-ttu-id="df7a1-149">Вес для сбалансированного сплайна.</span><span class="sxs-lookup"><span data-stu-id="df7a1-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df7a1-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df7a1-150">Remarks</span></span>

<span data-ttu-id="df7a1-151">Для каждого аргумента *x* должен быть аргумент *y* ; в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="df7a1-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="df7a1-152">Необходимо указать по крайней мере один аргумент *x*, *y*, *кнот* и *Weight* ; в противном случае Visio возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="df7a1-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

