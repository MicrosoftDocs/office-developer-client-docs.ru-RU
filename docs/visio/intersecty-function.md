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
description: Возвращает y-координата (в локальной системе координат) точки пересечения двух линий.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813968"
---
# <a name="intersecty-function"></a><span data-ttu-id="01cc3-103">Функция INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="01cc3-103">INTERSECTY Function</span></span>

<span data-ttu-id="01cc3-104">Возвращает *y* -координата (в локальной системе координат) точки пересечения двух линий.</span><span class="sxs-lookup"><span data-stu-id="01cc3-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="01cc3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01cc3-105">Syntax</span></span>

<span data-ttu-id="01cc3-106">INTERSECTX (** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *года 2* **, ** *angle2* **)</span><span class="sxs-lookup"><span data-stu-id="01cc3-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01cc3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01cc3-107">Parameters</span></span>

|<span data-ttu-id="01cc3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="01cc3-108">**Name**</span></span>|<span data-ttu-id="01cc3-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="01cc3-109">**Required/Optional**</span></span>|<span data-ttu-id="01cc3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="01cc3-110">**Data Type**</span></span>|<span data-ttu-id="01cc3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01cc3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01cc3-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="01cc3-112">_x1_</span></span> <br/> |<span data-ttu-id="01cc3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-113">Required</span></span>  <br/> |<span data-ttu-id="01cc3-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-114">**Number**</span></span> <br/> |<span data-ttu-id="01cc3-115">_X_-координаты точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="01cc3-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="01cc3-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="01cc3-116">_y1_</span></span> <br/> |<span data-ttu-id="01cc3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-117">Required</span></span>  <br/> |<span data-ttu-id="01cc3-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-118">**Number**</span></span> <br/> |<span data-ttu-id="01cc3-119">_Y_-координаты точки в первой строке.</span><span class="sxs-lookup"><span data-stu-id="01cc3-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="01cc3-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="01cc3-120">_angle1_</span></span> <br/> |<span data-ttu-id="01cc3-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-121">Required</span></span>  <br/> |<span data-ttu-id="01cc3-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-122">**Number**</span></span> <br/> | <span data-ttu-id="01cc3-123">Значение ячейки угол для первой строки.</span><span class="sxs-lookup"><span data-stu-id="01cc3-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="01cc3-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="01cc3-124">_x2_</span></span> <br/> |<span data-ttu-id="01cc3-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-125">Required</span></span>  <br/> |<span data-ttu-id="01cc3-126">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-126">**Number**</span></span> <br/> |<span data-ttu-id="01cc3-127">_X_-координаты точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="01cc3-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="01cc3-128">_года 2_</span><span class="sxs-lookup"><span data-stu-id="01cc3-128">_y2_</span></span> <br/> |<span data-ttu-id="01cc3-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-129">Required</span></span>  <br/> |<span data-ttu-id="01cc3-130">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-130">**Number**</span></span> <br/> |<span data-ttu-id="01cc3-131">_Y_-координаты точки во второй строке.</span><span class="sxs-lookup"><span data-stu-id="01cc3-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="01cc3-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="01cc3-132">_angle2_</span></span> <br/> |<span data-ttu-id="01cc3-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01cc3-133">Required</span></span>  <br/> |<span data-ttu-id="01cc3-134">**Число**</span><span class="sxs-lookup"><span data-stu-id="01cc3-134">**Number**</span></span> <br/> |<span data-ttu-id="01cc3-135">Значение ячейки угол для второй строке.</span><span class="sxs-lookup"><span data-stu-id="01cc3-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="01cc3-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="01cc3-136">Return value</span></span>

<span data-ttu-id="01cc3-137">Number</span><span class="sxs-lookup"><span data-stu-id="01cc3-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01cc3-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="01cc3-138">Remarks</span></span>

<span data-ttu-id="01cc3-139">Каждой строки определяется как точка (*x, y*) и угол.</span><span class="sxs-lookup"><span data-stu-id="01cc3-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="01cc3-140">Microsoft Visio использует эту функцию в ячейке PinY связан вращение руководство фигуры.</span><span class="sxs-lookup"><span data-stu-id="01cc3-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="01cc3-141">Если строки не пересекаются, функция возвращает ошибку деление на ноль (#DIV/0!), игнорирует Visio, последний неизвестное значение точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="01cc3-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="01cc3-142">Пример</span><span class="sxs-lookup"><span data-stu-id="01cc3-142">Example</span></span>

<span data-ttu-id="01cc3-143">INTERSECTY (VertGuide! PinX VertGuide! PinY, VertGuide! Угол HorzGuide! PinX HorzGuide! PinY, HorzGuide! Угол)</span><span class="sxs-lookup"><span data-stu-id="01cc3-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="01cc3-144">Возвращает *y* -координата пересечения точки VertGuide и HorzGuide в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="01cc3-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

