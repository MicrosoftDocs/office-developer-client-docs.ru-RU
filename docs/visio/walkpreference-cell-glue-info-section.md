---
title: Ячейка WalkPreference (раздел "Сведения о приклеивании")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Определяет ли конечная точка одномерной фигуры перемещение точки подключения горизонтальный или вертикальный на фигуры, которые он является привязку, с помощью динамических связывающих при перемещении фигуры в неоднозначные позицию. По умолчанию обе конечные точки одномерной фигуры перемещение горизонтальным точкам соединения.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815158"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="531a3-104">Ячейка WalkPreference (раздел "Сведения о приклеивании")</span><span class="sxs-lookup"><span data-stu-id="531a3-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="531a3-105">Определяет ли конечная точка одномерной фигуры перемещение точки подключения горизонтальный или вертикальный на фигуры, которые он является привязку, с помощью динамических связывающих при перемещении фигуры в неоднозначные позицию.</span><span class="sxs-lookup"><span data-stu-id="531a3-105">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position.</span></span> <span data-ttu-id="531a3-106">По умолчанию обе конечные точки одномерной фигуры перемещение горизонтальным точкам соединения.</span><span class="sxs-lookup"><span data-stu-id="531a3-106">By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="531a3-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="531a3-107">**Value**</span></span>|<span data-ttu-id="531a3-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="531a3-108">**Description**</span></span>|<span data-ttu-id="531a3-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="531a3-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="531a3-110">1</span><span class="sxs-lookup"><span data-stu-id="531a3-110">1</span></span>  <br/> | <span data-ttu-id="531a3-111">Начальную точку одномерной фигуры перемещает вертикальной подключений и перемещений конечной точки для горизонтальной подключения выберите команду (в начало стороне или снизу подключений).</span><span class="sxs-lookup"><span data-stu-id="531a3-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="531a3-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="531a3-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="531a3-113">2</span><span class="sxs-lookup"><span data-stu-id="531a3-113">2</span></span>  <br/> | <span data-ttu-id="531a3-114">Начальную точку одномерной фигуры перемещает точку подключения горизонтальной и перемещений конечной точки для вертикальной подключения выберите пункт (подключения со стороны вверх или вниз со стороны).</span><span class="sxs-lookup"><span data-stu-id="531a3-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="531a3-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="531a3-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="531a3-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="531a3-116">Remarks</span></span>

<span data-ttu-id="531a3-117">В этой ячейке не оказывает влияния на динамический соединители.</span><span class="sxs-lookup"><span data-stu-id="531a3-117">This cell has no effect on dynamic connectors.</span></span> <span data-ttu-id="531a3-118">Динамические соединителя поведение определяется его стиль маршрута.</span><span class="sxs-lookup"><span data-stu-id="531a3-118">A dynamic connector's behavior is determined by its routing style.</span></span> <span data-ttu-id="531a3-119">Видеть ячейку RouteStyle для стиля маршрутизации по умолчанию для динамического соединителей на странице или ShapeRouteStyle для маршрутизации стиля определенного динамических соединителя.</span><span class="sxs-lookup"><span data-stu-id="531a3-119">See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="531a3-120">Чтобы получить ссылку на ячейку WalkPreference по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="531a3-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="531a3-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="531a3-121">Cell name:</span></span>  <br/> | <span data-ttu-id="531a3-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="531a3-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="531a3-123">Для получения ссылки на ячейки WalkPreference по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="531a3-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="531a3-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="531a3-124">Section index:</span></span>  <br/> |<span data-ttu-id="531a3-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="531a3-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="531a3-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="531a3-126">Row index:</span></span>  <br/> |<span data-ttu-id="531a3-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="531a3-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="531a3-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="531a3-128">Cell index:</span></span>  <br/> |<span data-ttu-id="531a3-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="531a3-129">**visWalkPref**</span></span> <br/> |
   

