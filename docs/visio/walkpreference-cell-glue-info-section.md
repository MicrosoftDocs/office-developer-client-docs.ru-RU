---
title: WalkPreference Cell (Glue Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Определяет, перемещается ли конечная точка 1-D-фигуры в горизонтальную или вертикальную точку подключения к фигуре, к какой фигуре она приглушена, с помощью динамического приклейки, когда фигура перемещается в неоднозначное положение. По умолчанию обе конечные точки размерной фигуры перемещаются в горизонтальные точки подключения.
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408609"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="2d52f-104">WalkPreference Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="2d52f-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="2d52f-105">Определяет, перемещается ли конечная точка 1-D-фигуры в горизонтальную или вертикальную точку подключения к фигуре, к какой фигуре она приглушена, с помощью динамического приклейки, когда фигура перемещается в неоднозначное положение.</span><span class="sxs-lookup"><span data-stu-id="2d52f-105">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position.</span></span> <span data-ttu-id="2d52f-106">По умолчанию обе конечные точки размерной фигуры перемещаются в горизонтальные точки подключения.</span><span class="sxs-lookup"><span data-stu-id="2d52f-106">By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="2d52f-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2d52f-107">**Value**</span></span>|<span data-ttu-id="2d52f-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2d52f-108">**Description**</span></span>|<span data-ttu-id="2d52f-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="2d52f-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2d52f-110">1 </span><span class="sxs-lookup"><span data-stu-id="2d52f-110">1</span></span>  <br/> | <span data-ttu-id="2d52f-111">Начальская точка фигуры размером 1 D перемещается в вертикальную точку подключения, а конечная точка перемещается в горизонтальную точку подключения (сверху к боковой или снизу к боковой).</span><span class="sxs-lookup"><span data-stu-id="2d52f-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="2d52f-112">**visPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="2d52f-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="2d52f-113">2 </span><span class="sxs-lookup"><span data-stu-id="2d52f-113">2</span></span>  <br/> | <span data-ttu-id="2d52f-114">Начальская точка фигуры размером 1 D перемещается в горизонтальную точку подключения, а конечная точка перемещается в вертикальную точку подключения (соединения "сверху вниз" или "сверху вниз").</span><span class="sxs-lookup"><span data-stu-id="2d52f-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="2d52f-115">**visPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="2d52f-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d52f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d52f-116">Remarks</span></span>

<span data-ttu-id="2d52f-117">Эта ячейка не влияет на динамические соединители.</span><span class="sxs-lookup"><span data-stu-id="2d52f-117">This cell has no effect on dynamic connectors.</span></span> <span data-ttu-id="2d52f-118">Поведение динамического соединитела определяется его стилем маршрутки.</span><span class="sxs-lookup"><span data-stu-id="2d52f-118">A dynamic connector's behavior is determined by its routing style.</span></span> <span data-ttu-id="2d52f-119">В ячейке RouteStyle для стиля маршрутки по умолчанию для динамических соединителей на странице или в shapeRouteStyle для стиля маршрутки определенного динамического соединителя.</span><span class="sxs-lookup"><span data-stu-id="2d52f-119">See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="2d52f-120">Чтобы получить ссылку на ячейку WalkPreference по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2d52f-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d52f-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d52f-121">Cell name:</span></span>  <br/> | <span data-ttu-id="2d52f-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="2d52f-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="2d52f-123">Чтобы получить ссылку на ячейку WalkPreference по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2d52f-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d52f-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2d52f-124">Section index:</span></span>  <br/> |<span data-ttu-id="2d52f-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d52f-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d52f-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2d52f-126">Row index:</span></span>  <br/> |<span data-ttu-id="2d52f-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2d52f-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="2d52f-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d52f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="2d52f-129">**visPref**</span><span class="sxs-lookup"><span data-stu-id="2d52f-129">**visWalkPref**</span></span> <br/> |
   

