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
description: Возвращает координату x (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335310"
---
# <a name="intersectx-function"></a><span data-ttu-id="d9639-103">Функция INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="d9639-103">INTERSECTX Function</span></span>

<span data-ttu-id="d9639-104">Возвращает координату *x* (в локальной системе координат) точки, в которой пересекаются две линии.</span><span class="sxs-lookup"><span data-stu-id="d9639-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d9639-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9639-105">Syntax</span></span>

<span data-ttu-id="d9639-106">INTERSECTX (\* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *x2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d9639-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d9639-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9639-107">Parameters</span></span>

|<span data-ttu-id="d9639-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d9639-108">**Name**</span></span>|<span data-ttu-id="d9639-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d9639-109">**Required/Optional**</span></span>|<span data-ttu-id="d9639-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d9639-110">**Data Type**</span></span>|<span data-ttu-id="d9639-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9639-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d9639-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="d9639-112">_x1_</span></span> <br/> |<span data-ttu-id="d9639-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-113">Required</span></span>  <br/> |<span data-ttu-id="d9639-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-114">**Number**</span></span> <br/> |<span data-ttu-id="d9639-115">Координата _x_точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="d9639-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="d9639-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="d9639-116">_y1_</span></span> <br/> |<span data-ttu-id="d9639-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-117">Required</span></span>  <br/> |<span data-ttu-id="d9639-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-118">**Number**</span></span> <br/> |<span data-ttu-id="d9639-119">Координата _y_точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="d9639-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="d9639-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="d9639-120">_angle1_</span></span> <br/> |<span data-ttu-id="d9639-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-121">Required</span></span>  <br/> |<span data-ttu-id="d9639-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-122">**Number**</span></span> <br/> | <span data-ttu-id="d9639-123">Значение ячейки угла для первой строки.</span><span class="sxs-lookup"><span data-stu-id="d9639-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="d9639-124">_2_</span><span class="sxs-lookup"><span data-stu-id="d9639-124">_x2_</span></span> <br/> |<span data-ttu-id="d9639-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-125">Required</span></span>  <br/> |<span data-ttu-id="d9639-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-126">**Number**</span></span> <br/> |<span data-ttu-id="d9639-127">Координата _x_точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="d9639-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="d9639-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="d9639-128">_y2_</span></span> <br/> |<span data-ttu-id="d9639-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-129">Required</span></span>  <br/> |<span data-ttu-id="d9639-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-130">**Number**</span></span> <br/> |<span data-ttu-id="d9639-131">Координата _y_точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="d9639-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="d9639-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="d9639-132">_angle2_</span></span> <br/> |<span data-ttu-id="d9639-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d9639-133">Required</span></span>  <br/> |<span data-ttu-id="d9639-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9639-134">**Number**</span></span> <br/> |<span data-ttu-id="d9639-135">Значение ячейки угла для второй строки.</span><span class="sxs-lookup"><span data-stu-id="d9639-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d9639-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9639-136">Return value</span></span>

<span data-ttu-id="d9639-137">Номер</span><span class="sxs-lookup"><span data-stu-id="d9639-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9639-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9639-138">Remarks</span></span>

<span data-ttu-id="d9639-139">Каждая строка определяется как точка (*x, y*) и угол.</span><span class="sxs-lookup"><span data-stu-id="d9639-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="d9639-140">В Microsoft Visio Эта функция используется в ячейке PinX фигуры, связанной с повернутой направляющей.</span><span class="sxs-lookup"><span data-stu-id="d9639-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="d9639-141">Если строки не пересекаются, функция возвращает ошибку деления на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая Последнее известное значение точки.</span><span class="sxs-lookup"><span data-stu-id="d9639-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d9639-142">Пример</span><span class="sxs-lookup"><span data-stu-id="d9639-142">Example</span></span>

<span data-ttu-id="d9639-143">INTERSECTX (Вертгуиде! PinX, Вертгуиде! PinY, Вертгуиде! Угол, Хорзгуиде! PinX, Хорзгуиде! PinY, Хорзгуиде! Градусов</span><span class="sxs-lookup"><span data-stu-id="d9639-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="d9639-144">Возвращает координату *x* точки пересечения Вертгуиде и хорзгуиде в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="d9639-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

