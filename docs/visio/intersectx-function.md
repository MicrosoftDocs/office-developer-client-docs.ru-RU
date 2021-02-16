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
description: Возвращает x-координату (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418276"
---
# <a name="intersectx-function"></a><span data-ttu-id="5ded3-103">Функция INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="5ded3-103">INTERSECTX Function</span></span>

<span data-ttu-id="5ded3-104">Возвращает  *x-координату*  (в локальной системе координат) точки, в которой пересекаются две линии.</span><span class="sxs-lookup"><span data-stu-id="5ded3-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ded3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ded3-105">Syntax</span></span>

<span data-ttu-id="5ded3-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5ded3-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ded3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ded3-107">Parameters</span></span>

|<span data-ttu-id="5ded3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5ded3-108">**Name**</span></span>|<span data-ttu-id="5ded3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5ded3-109">**Required/Optional**</span></span>|<span data-ttu-id="5ded3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5ded3-110">**Data Type**</span></span>|<span data-ttu-id="5ded3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ded3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ded3-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="5ded3-112">_x1_</span></span> <br/> |<span data-ttu-id="5ded3-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-113">Required</span></span>  <br/> |<span data-ttu-id="5ded3-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-114">**Number**</span></span> <br/> |<span data-ttu-id="5ded3-115">X-координата точки в первой строке. </span><span class="sxs-lookup"><span data-stu-id="5ded3-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="5ded3-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="5ded3-116">_y1_</span></span> <br/> |<span data-ttu-id="5ded3-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-117">Required</span></span>  <br/> |<span data-ttu-id="5ded3-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-118">**Number**</span></span> <br/> |<span data-ttu-id="5ded3-119">Y-координата точки в первой строке. </span><span class="sxs-lookup"><span data-stu-id="5ded3-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="5ded3-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="5ded3-120">_angle1_</span></span> <br/> |<span data-ttu-id="5ded3-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-121">Required</span></span>  <br/> |<span data-ttu-id="5ded3-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-122">**Number**</span></span> <br/> | <span data-ttu-id="5ded3-123">Значение ячейки Angle для первой строки.</span><span class="sxs-lookup"><span data-stu-id="5ded3-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="5ded3-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="5ded3-124">_x2_</span></span> <br/> |<span data-ttu-id="5ded3-125">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-125">Required</span></span>  <br/> |<span data-ttu-id="5ded3-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-126">**Number**</span></span> <br/> |<span data-ttu-id="5ded3-127">X-координата точки во второй строке. </span><span class="sxs-lookup"><span data-stu-id="5ded3-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="5ded3-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="5ded3-128">_y2_</span></span> <br/> |<span data-ttu-id="5ded3-129">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-129">Required</span></span>  <br/> |<span data-ttu-id="5ded3-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-130">**Number**</span></span> <br/> |<span data-ttu-id="5ded3-131">Y-координата точки во второй строке. </span><span class="sxs-lookup"><span data-stu-id="5ded3-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="5ded3-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="5ded3-132">_angle2_</span></span> <br/> |<span data-ttu-id="5ded3-133">Обязательна</span><span class="sxs-lookup"><span data-stu-id="5ded3-133">Required</span></span>  <br/> |<span data-ttu-id="5ded3-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="5ded3-134">**Number**</span></span> <br/> |<span data-ttu-id="5ded3-135">Значение ячейки Angle для второй строки.</span><span class="sxs-lookup"><span data-stu-id="5ded3-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ded3-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ded3-136">Return value</span></span>

<span data-ttu-id="5ded3-137">Числовой</span><span class="sxs-lookup"><span data-stu-id="5ded3-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ded3-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ded3-138">Remarks</span></span>

<span data-ttu-id="5ded3-139">Каждая строка определяется как точка *(x,y)* и угол.</span><span class="sxs-lookup"><span data-stu-id="5ded3-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="5ded3-140">Microsoft Visio использует эту функцию в ячейке PinX фигуры, привязаемой к повернутой направляющей.</span><span class="sxs-lookup"><span data-stu-id="5ded3-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="5ded3-141">Если линии не пересекаются, функция возвращает ошибку деления на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая последнее известное значение точки.</span><span class="sxs-lookup"><span data-stu-id="5ded3-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ded3-142">Пример</span><span class="sxs-lookup"><span data-stu-id="5ded3-142">Example</span></span>

<span data-ttu-id="5ded3-143">INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Angle)</span><span class="sxs-lookup"><span data-stu-id="5ded3-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="5ded3-144">Возвращает  *x-координату*  точки пересечения VertGuide и HorzGuide в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="5ded3-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

