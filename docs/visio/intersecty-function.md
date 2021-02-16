---
title: Функция INTERSECTY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Возвращает координату y (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426102"
---
# <a name="intersecty-function"></a><span data-ttu-id="e1f45-103">Функция INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="e1f45-103">INTERSECTY Function</span></span>

<span data-ttu-id="e1f45-104">Возвращает  *координату y*  (в локальной системе координат) точки, в которой пересекаются две линии.</span><span class="sxs-lookup"><span data-stu-id="e1f45-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1f45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1f45-105">Syntax</span></span>

<span data-ttu-id="e1f45-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e1f45-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1f45-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1f45-107">Parameters</span></span>

|<span data-ttu-id="e1f45-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e1f45-108">**Name**</span></span>|<span data-ttu-id="e1f45-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e1f45-109">**Required/Optional**</span></span>|<span data-ttu-id="e1f45-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e1f45-110">**Data Type**</span></span>|<span data-ttu-id="e1f45-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1f45-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1f45-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="e1f45-112">_x1_</span></span> <br/> |<span data-ttu-id="e1f45-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-113">Required</span></span>  <br/> |<span data-ttu-id="e1f45-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-114">**Number**</span></span> <br/> |<span data-ttu-id="e1f45-115">X-координата точки в первой строке. </span><span class="sxs-lookup"><span data-stu-id="e1f45-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="e1f45-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="e1f45-116">_y1_</span></span> <br/> |<span data-ttu-id="e1f45-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-117">Required</span></span>  <br/> |<span data-ttu-id="e1f45-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-118">**Number**</span></span> <br/> |<span data-ttu-id="e1f45-119">Y-координата точки в первой строке. </span><span class="sxs-lookup"><span data-stu-id="e1f45-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="e1f45-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="e1f45-120">_angle1_</span></span> <br/> |<span data-ttu-id="e1f45-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-121">Required</span></span>  <br/> |<span data-ttu-id="e1f45-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-122">**Number**</span></span> <br/> | <span data-ttu-id="e1f45-123">Значение ячейки Angle для первой строки.</span><span class="sxs-lookup"><span data-stu-id="e1f45-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="e1f45-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="e1f45-124">_x2_</span></span> <br/> |<span data-ttu-id="e1f45-125">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-125">Required</span></span>  <br/> |<span data-ttu-id="e1f45-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-126">**Number**</span></span> <br/> |<span data-ttu-id="e1f45-127">X-координата точки во второй строке. </span><span class="sxs-lookup"><span data-stu-id="e1f45-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="e1f45-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="e1f45-128">_y2_</span></span> <br/> |<span data-ttu-id="e1f45-129">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-129">Required</span></span>  <br/> |<span data-ttu-id="e1f45-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-130">**Number**</span></span> <br/> |<span data-ttu-id="e1f45-131">Y-координата точки во второй строке. </span><span class="sxs-lookup"><span data-stu-id="e1f45-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="e1f45-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="e1f45-132">_angle2_</span></span> <br/> |<span data-ttu-id="e1f45-133">Обязательна</span><span class="sxs-lookup"><span data-stu-id="e1f45-133">Required</span></span>  <br/> |<span data-ttu-id="e1f45-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1f45-134">**Number**</span></span> <br/> |<span data-ttu-id="e1f45-135">Значение ячейки Angle для второй строки.</span><span class="sxs-lookup"><span data-stu-id="e1f45-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e1f45-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1f45-136">Return value</span></span>

<span data-ttu-id="e1f45-137">Числовой</span><span class="sxs-lookup"><span data-stu-id="e1f45-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1f45-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1f45-138">Remarks</span></span>

<span data-ttu-id="e1f45-139">Каждая строка определяется как точка *(x,y)* и угол.</span><span class="sxs-lookup"><span data-stu-id="e1f45-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="e1f45-140">Microsoft Visio использует эту функцию в ячейке PinY фигуры, привязаемой к повернутой направляющей.</span><span class="sxs-lookup"><span data-stu-id="e1f45-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="e1f45-141">Если линии не пересекаются, функция возвращает ошибку деления на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая последнее известное значение точки.</span><span class="sxs-lookup"><span data-stu-id="e1f45-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1f45-142">Пример</span><span class="sxs-lookup"><span data-stu-id="e1f45-142">Example</span></span>

<span data-ttu-id="e1f45-143">INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Angle)</span><span class="sxs-lookup"><span data-stu-id="e1f45-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="e1f45-144">Возвращает  *координату y точки*  пересечения VertGuide и HorzGuide в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="e1f45-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

