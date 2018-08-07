---
title: Функция INTERSECTX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Возвращает x-координата (в локальной системе координат) точки пересечения двух линий.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813965"
---
# <a name="intersectx-function"></a><span data-ttu-id="55d60-103">Функция INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="55d60-103">INTERSECTX Function</span></span>

<span data-ttu-id="55d60-104">Возвращает *x* -координата (в локальной системе координат) точки пересечения двух линий.</span><span class="sxs-lookup"><span data-stu-id="55d60-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="55d60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55d60-105">Syntax</span></span>

<span data-ttu-id="55d60-106">INTERSECTX (** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *года 2* **, ** *angle2* **)</span><span class="sxs-lookup"><span data-stu-id="55d60-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="55d60-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="55d60-107">Parameters</span></span>

|<span data-ttu-id="55d60-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="55d60-108">**Name**</span></span>|<span data-ttu-id="55d60-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="55d60-109">**Required/Optional**</span></span>|<span data-ttu-id="55d60-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="55d60-110">**Data Type**</span></span>|<span data-ttu-id="55d60-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55d60-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="55d60-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="55d60-112">_x1_</span></span> <br/> |<span data-ttu-id="55d60-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-113">Required</span></span>  <br/> |<span data-ttu-id="55d60-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-114">**Number**</span></span> <br/> |<span data-ttu-id="55d60-115">_X_-координаты точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="55d60-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="55d60-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="55d60-116">_y1_</span></span> <br/> |<span data-ttu-id="55d60-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-117">Required</span></span>  <br/> |<span data-ttu-id="55d60-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-118">**Number**</span></span> <br/> |<span data-ttu-id="55d60-119">_Y_-координаты точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="55d60-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="55d60-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="55d60-120">_angle1_</span></span> <br/> |<span data-ttu-id="55d60-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-121">Required</span></span>  <br/> |<span data-ttu-id="55d60-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-122">**Number**</span></span> <br/> | <span data-ttu-id="55d60-123">Значение ячейки угол для первой строки.</span><span class="sxs-lookup"><span data-stu-id="55d60-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="55d60-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="55d60-124">_x2_</span></span> <br/> |<span data-ttu-id="55d60-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-125">Required</span></span>  <br/> |<span data-ttu-id="55d60-126">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-126">**Number**</span></span> <br/> |<span data-ttu-id="55d60-127">_X_-координаты точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="55d60-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="55d60-128">_года 2_</span><span class="sxs-lookup"><span data-stu-id="55d60-128">_y2_</span></span> <br/> |<span data-ttu-id="55d60-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-129">Required</span></span>  <br/> |<span data-ttu-id="55d60-130">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-130">**Number**</span></span> <br/> |<span data-ttu-id="55d60-131">_Y_-координаты точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="55d60-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="55d60-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="55d60-132">_angle2_</span></span> <br/> |<span data-ttu-id="55d60-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="55d60-133">Required</span></span>  <br/> |<span data-ttu-id="55d60-134">**Число**</span><span class="sxs-lookup"><span data-stu-id="55d60-134">**Number**</span></span> <br/> |<span data-ttu-id="55d60-135">Значение ячейки угол для второй строке.</span><span class="sxs-lookup"><span data-stu-id="55d60-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="55d60-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="55d60-137">Number</span><span class="sxs-lookup"><span data-stu-id="55d60-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55d60-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="55d60-138">Remarks</span></span>

<span data-ttu-id="55d60-139">Каждой строки определяется как точка (*x, y*) и угол.</span><span class="sxs-lookup"><span data-stu-id="55d60-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="55d60-140">Microsoft Visio использует эту функцию в ячейке PinX связан вращение руководство фигуры.</span><span class="sxs-lookup"><span data-stu-id="55d60-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="55d60-141">Если строки не пересекаются, функция возвращает ошибку деление на ноль (#DIV/0!), игнорирует Visio, последний неизвестное значение точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="55d60-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="55d60-142">Пример</span><span class="sxs-lookup"><span data-stu-id="55d60-142">Example</span></span>

<span data-ttu-id="55d60-143">INTERSECTX (VertGuide! PinX VertGuide! PinY, VertGuide! Угол HorzGuide! PinX HorzGuide! PinY, HorzGuide! Угол)</span><span class="sxs-lookup"><span data-stu-id="55d60-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="55d60-144">Возвращает *x* -координата пересечения точки VertGuide и HorzGuide в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="55d60-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

