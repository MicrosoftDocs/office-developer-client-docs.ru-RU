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
description: Возвращает y-coordinate (в локальной системе координат) точки, в которой пересекаются две линии.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426102"
---
# <a name="intersecty-function"></a><span data-ttu-id="e1cbc-103">Функция INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="e1cbc-103">INTERSECTY Function</span></span>

<span data-ttu-id="e1cbc-104">Возвращает  *y-coordinate*  (в локальной системе координат) точки, в которой пересекаются две линии.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1cbc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1cbc-105">Syntax</span></span>

<span data-ttu-id="e1cbc-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e1cbc-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1cbc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1cbc-107">Parameters</span></span>

|<span data-ttu-id="e1cbc-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-108">**Name**</span></span>|<span data-ttu-id="e1cbc-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-109">**Required/Optional**</span></span>|<span data-ttu-id="e1cbc-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-110">**Data Type**</span></span>|<span data-ttu-id="e1cbc-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1cbc-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-112">_x1_</span></span> <br/> |<span data-ttu-id="e1cbc-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-113">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-114">**Number**</span></span> <br/> |<span data-ttu-id="e1cbc-115">X-координата точки на первой строке. </span><span class="sxs-lookup"><span data-stu-id="e1cbc-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="e1cbc-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-116">_y1_</span></span> <br/> |<span data-ttu-id="e1cbc-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-117">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-118">**Number**</span></span> <br/> |<span data-ttu-id="e1cbc-119">Y-координата точки на первой строке. </span><span class="sxs-lookup"><span data-stu-id="e1cbc-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="e1cbc-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-120">_angle1_</span></span> <br/> |<span data-ttu-id="e1cbc-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-121">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-122">**Number**</span></span> <br/> | <span data-ttu-id="e1cbc-123">Значение ячейки Angle для первой строки.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="e1cbc-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-124">_x2_</span></span> <br/> |<span data-ttu-id="e1cbc-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-125">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-126">**Number**</span></span> <br/> |<span data-ttu-id="e1cbc-127">X-координата точки на второй строке. </span><span class="sxs-lookup"><span data-stu-id="e1cbc-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="e1cbc-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-128">_y2_</span></span> <br/> |<span data-ttu-id="e1cbc-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-129">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-130">**Number**</span></span> <br/> |<span data-ttu-id="e1cbc-131">Y-координата точки на второй строке. </span><span class="sxs-lookup"><span data-stu-id="e1cbc-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="e1cbc-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="e1cbc-132">_angle2_</span></span> <br/> |<span data-ttu-id="e1cbc-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1cbc-133">Required</span></span>  <br/> |<span data-ttu-id="e1cbc-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="e1cbc-134">**Number**</span></span> <br/> |<span data-ttu-id="e1cbc-135">Значение ячейки Angle для второй строки.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e1cbc-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1cbc-136">Return value</span></span>

<span data-ttu-id="e1cbc-137">Номер</span><span class="sxs-lookup"><span data-stu-id="e1cbc-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1cbc-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1cbc-138">Remarks</span></span>

<span data-ttu-id="e1cbc-139">Каждая строка определяется как точка *(x,y) и* угол.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="e1cbc-140">Microsoft Visio использует эту функцию в ячейке PinY фигуры, приклеенной к вращаемой направляющей.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="e1cbc-141">Если линии не пересекаются, функция возвращает ошибку разделять на ноль (#DIV/0!), которую Visio игнорирует, восстанавливая последнее известное значение для точки.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1cbc-142">Пример</span><span class="sxs-lookup"><span data-stu-id="e1cbc-142">Example</span></span>

<span data-ttu-id="e1cbc-143">INTERSECTY(VertGuide! PinX,VertGuide! Piny,VertGuide! Угол, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Угол)</span><span class="sxs-lookup"><span data-stu-id="e1cbc-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="e1cbc-144">Возвращает  *y-координату*  точки пересечения VertGuide и HorzGuide в единицах страниц.</span><span class="sxs-lookup"><span data-stu-id="e1cbc-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

