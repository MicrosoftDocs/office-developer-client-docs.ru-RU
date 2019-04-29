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
description: Определяет, перемещается ли конечная точка одноМерной фигуры в горизонтальную или вертикальную точку подключения на фигуре, к которой она связана, с помощью динамической ссылки, когда фигура перемещается в неоднозначное положение. По умолчанию обе конечные точки фигуры 1 – D перемещаются на горизонтальные точки подключения.
ms.openlocfilehash: 05f7ded3f7336dc2f8598e8d1e9edc501b511546
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408609"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="afa91-104">WalkPreference Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="afa91-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="afa91-105">Определяет, перемещается ли конечная точка одноМерной фигуры в горизонтальную или вертикальную точку подключения на фигуре, к которой она связана, с помощью динамической ссылки, когда фигура перемещается в неоднозначное положение.</span><span class="sxs-lookup"><span data-stu-id="afa91-105">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position.</span></span> <span data-ttu-id="afa91-106">По умолчанию обе конечные точки фигуры 1 – D перемещаются на горизонтальные точки подключения.</span><span class="sxs-lookup"><span data-stu-id="afa91-106">By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="afa91-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="afa91-107">**Value**</span></span>|<span data-ttu-id="afa91-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="afa91-108">**Description**</span></span>|<span data-ttu-id="afa91-109">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="afa91-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="afa91-110">1,1</span><span class="sxs-lookup"><span data-stu-id="afa91-110">1</span></span>  <br/> | <span data-ttu-id="afa91-111">Начальная точка одномерной фигуры перемещается на вертикальную точку подключения, а конечная точка перемещается в горизонтальную точку подключения (подключения с самым верхним или нижним и рядом).</span><span class="sxs-lookup"><span data-stu-id="afa91-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="afa91-112">**Висвалкпрефбегнс**</span><span class="sxs-lookup"><span data-stu-id="afa91-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="afa91-113">2</span><span class="sxs-lookup"><span data-stu-id="afa91-113">2</span></span>  <br/> | <span data-ttu-id="afa91-114">Начальная точка одномерной фигуры перемещается в горизонтальную точку подключения, а конечная точка перемещается в вертикальную точку подключения (сквозные и посторонние подключения).</span><span class="sxs-lookup"><span data-stu-id="afa91-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="afa91-115">**Висвалкпрефенднс**</span><span class="sxs-lookup"><span data-stu-id="afa91-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afa91-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="afa91-116">Remarks</span></span>

<span data-ttu-id="afa91-117">Эта ячейка не оказывает никакого действия для динамических соединителей.</span><span class="sxs-lookup"><span data-stu-id="afa91-117">This cell has no effect on dynamic connectors.</span></span> <span data-ttu-id="afa91-118">Поведение динамического соединителя определяется его стилем маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="afa91-118">A dynamic connector's behavior is determined by its routing style.</span></span> <span data-ttu-id="afa91-119">Просмотрите ячейку RouteStyle для стиля маршрутизации по умолчанию для динамических соединителей на странице или ShapeRouteStyle для стиля маршрутизации определенного динамического соединителя.</span><span class="sxs-lookup"><span data-stu-id="afa91-119">See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="afa91-120">Чтобы получить ссылку на ячейку WalkPreference по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="afa91-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="afa91-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="afa91-121">Cell name:</span></span>  <br/> | <span data-ttu-id="afa91-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="afa91-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="afa91-123">Чтобы получить ссылку на ячейку WalkPreference по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="afa91-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="afa91-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="afa91-124">Section index:</span></span>  <br/> |<span data-ttu-id="afa91-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="afa91-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="afa91-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="afa91-126">Row index:</span></span>  <br/> |<span data-ttu-id="afa91-127">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="afa91-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="afa91-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="afa91-128">Cell index:</span></span>  <br/> |<span data-ttu-id="afa91-129">**Висвалкпреф**</span><span class="sxs-lookup"><span data-stu-id="afa91-129">**visWalkPref**</span></span> <br/> |
   

