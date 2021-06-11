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
description: Определяет, перемещается ли конечная точка фигуры 1-D в точку горизонтального или вертикального подключения к фигуре, к ней приклеивается динамический клей, когда фигура перемещается в неоднозначное положение. По умолчанию обе конечные точки формы 1-D перемещаются в горизонтальные точки подключения.
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408609"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="e8994-104">WalkPreference Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="e8994-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="e8994-105">Определяет, перемещается ли конечная точка фигуры 1-D в точку горизонтального или вертикального подключения к фигуре, к ней приклеивается динамический клей, когда фигура перемещается в неоднозначное положение.</span><span class="sxs-lookup"><span data-stu-id="e8994-105">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position.</span></span> <span data-ttu-id="e8994-106">По умолчанию обе конечные точки формы 1-D перемещаются в горизонтальные точки подключения.</span><span class="sxs-lookup"><span data-stu-id="e8994-106">By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="e8994-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e8994-107">**Value**</span></span>|<span data-ttu-id="e8994-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8994-108">**Description**</span></span>|<span data-ttu-id="e8994-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e8994-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e8994-110">1</span><span class="sxs-lookup"><span data-stu-id="e8994-110">1</span></span>  <br/> | <span data-ttu-id="e8994-111">Начальская точка фигуры 1-D перемещается в точку вертикального подключения, а конечная — к горизонтальной точке подключения (верхней или нижней части).</span><span class="sxs-lookup"><span data-stu-id="e8994-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="e8994-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="e8994-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="e8994-113">2</span><span class="sxs-lookup"><span data-stu-id="e8994-113">2</span></span>  <br/> | <span data-ttu-id="e8994-114">Началная точка фигуры 1-D перемещается в горизонтальную точку подключения, а конечная точка перемещается в вертикальную точку подключения (боковое или нижнее подключения).</span><span class="sxs-lookup"><span data-stu-id="e8994-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="e8994-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="e8994-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8994-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8994-116">Remarks</span></span>

<span data-ttu-id="e8994-117">Эта ячейка не влияет на динамические соединители.</span><span class="sxs-lookup"><span data-stu-id="e8994-117">This cell has no effect on dynamic connectors.</span></span> <span data-ttu-id="e8994-118">Поведение динамического соединиттеля определяется стилем маршрутики.</span><span class="sxs-lookup"><span data-stu-id="e8994-118">A dynamic connector's behavior is determined by its routing style.</span></span> <span data-ttu-id="e8994-119">См. элемент RouteStyle для стиля маршрутивки по умолчанию для динамических соединителей на странице или ShapeRouteStyle для стиля маршрутивки определенного динамического соединиттеля.</span><span class="sxs-lookup"><span data-stu-id="e8994-119">See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="e8994-120">Чтобы получить ссылку на ячейку WalkPreference по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e8994-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8994-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8994-121">Cell name:</span></span>  <br/> | <span data-ttu-id="e8994-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="e8994-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="e8994-123">Чтобы получить ссылку на ячейку WalkPreference по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e8994-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8994-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e8994-124">Section index:</span></span>  <br/> |<span data-ttu-id="e8994-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8994-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8994-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e8994-126">Row index:</span></span>  <br/> |<span data-ttu-id="e8994-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="e8994-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="e8994-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8994-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e8994-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="e8994-129">**visWalkPref**</span></span> <br/> |
   

