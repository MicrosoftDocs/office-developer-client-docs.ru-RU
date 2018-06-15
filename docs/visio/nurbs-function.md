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
description: Возвращает неоднородной rational-сплайн (NURBS). Эта функция используется в ячейке E в строках геометрии NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814342"
---
# <a name="nurbs-function"></a><span data-ttu-id="ee385-104">Функция NURBS</span><span class="sxs-lookup"><span data-stu-id="ee385-104">NURBS Function</span></span>

<span data-ttu-id="ee385-105">Возвращает неоднородной rational-сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="ee385-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="ee385-106">Эта функция используется в ячейке E в строках геометрии NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="ee385-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ee385-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee385-107">Syntax</span></span>

<span data-ttu-id="ee385-108">NURBS (** *knotLast* **, ** *степень* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **,...)</span><span class="sxs-lookup"><span data-stu-id="ee385-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ee385-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee385-109">Parameters</span></span>

|<span data-ttu-id="ee385-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ee385-110">**Name**</span></span>|<span data-ttu-id="ee385-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="ee385-111">**Required/Optional**</span></span>|<span data-ttu-id="ee385-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ee385-112">**Data Type**</span></span>|<span data-ttu-id="ee385-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee385-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ee385-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="ee385-114">_knotLast_</span></span> <br/> |<span data-ttu-id="ee385-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-115">Required</span></span>  <br/> |<span data-ttu-id="ee385-116">**string**</span><span class="sxs-lookup"><span data-stu-id="ee385-116">**string**</span></span> <br/> | <span data-ttu-id="ee385-117">Последний число узлов.</span><span class="sxs-lookup"><span data-stu-id="ee385-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="ee385-118">_степень_</span><span class="sxs-lookup"><span data-stu-id="ee385-118">_degree_</span></span> <br/> |<span data-ttu-id="ee385-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-119">Required</span></span>  <br/> |<span data-ttu-id="ee385-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="ee385-120">**Numeric**</span></span> <br/> |<span data-ttu-id="ee385-121">Степень сплайна.</span><span class="sxs-lookup"><span data-stu-id="ee385-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="ee385-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="ee385-122">_xType_</span></span> <br/> |<span data-ttu-id="ee385-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-123">Required</span></span>  <br/> |<span data-ttu-id="ee385-124">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="ee385-124">**Numeric**</span></span> <br/> |<span data-ttu-id="ee385-125">Указывает способ представления входных данных _x_ .</span><span class="sxs-lookup"><span data-stu-id="ee385-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="ee385-126">Если _xType_ равно 0, все входные данные _x_ интерпретируется в процентах от ширины.</span><span class="sxs-lookup"><span data-stu-id="ee385-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="ee385-127">Если _xType_ принимает значение 1, все входные данные _x_ интерпретируется как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="ee385-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="ee385-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="ee385-128">_yType_</span></span> <br/> |<span data-ttu-id="ee385-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-129">Required</span></span>  <br/> |<span data-ttu-id="ee385-130">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="ee385-130">**Numeric**</span></span> <br/> |<span data-ttu-id="ee385-131">Указывает способ представления входных данных _y_ .</span><span class="sxs-lookup"><span data-stu-id="ee385-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="ee385-132">Если _yType_ равно 0, все входные данные _y_ интерпретируется в процентном соотношении от высоту.</span><span class="sxs-lookup"><span data-stu-id="ee385-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="ee385-133">Если _yType_ принимает значение 1, все входные данные _y_ интерпретируется как локальные координаты.</span><span class="sxs-lookup"><span data-stu-id="ee385-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="ee385-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="ee385-134">_x1_</span></span> <br/> |<span data-ttu-id="ee385-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-135">Required</span></span>  <br/> |<span data-ttu-id="ee385-136">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ee385-136">**String**</span></span> <br/> |<span data-ttu-id="ee385-137">X координата.</span><span class="sxs-lookup"><span data-stu-id="ee385-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="ee385-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="ee385-138">_y1_</span></span> <br/> |<span data-ttu-id="ee385-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-139">Required</span></span>  <br/> |<span data-ttu-id="ee385-140">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ee385-140">**String**</span></span> <br/> |<span data-ttu-id="ee385-141">Координата.</span><span class="sxs-lookup"><span data-stu-id="ee385-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="ee385-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="ee385-142">_knot1_</span></span> <br/> |<span data-ttu-id="ee385-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-143">Required</span></span>  <br/> |<span data-ttu-id="ee385-144">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ee385-144">**String**</span></span> <br/> |<span data-ttu-id="ee385-145">Узлов на сплайн.</span><span class="sxs-lookup"><span data-stu-id="ee385-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="ee385-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="ee385-146">_weight1_</span></span> <br/> |<span data-ttu-id="ee385-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee385-147">Required</span></span>  <br/> |<span data-ttu-id="ee385-148">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ee385-148">**String**</span></span> <br/> |<span data-ttu-id="ee385-149">Вес на сплайн.</span><span class="sxs-lookup"><span data-stu-id="ee385-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee385-150">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee385-150">Remarks</span></span>

<span data-ttu-id="ee385-151">Для каждого аргумента *x* значения *y* аргумент; в противном случае возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ee385-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="ee385-152">Необходимо указать по крайней мере один *x*, *y*, *число узлов* и *Вес* аргумент; в противном случае Visio возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ee385-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

