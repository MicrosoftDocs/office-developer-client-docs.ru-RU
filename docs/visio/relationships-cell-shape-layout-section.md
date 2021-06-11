---
title: Relationships Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Сохраняет связи между контейнерами, списками, вызовами и фигурами.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406411"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="cf90e-103">Relationships Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="cf90e-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="cf90e-104">Сохраняет связи между контейнерами, списками, вызовами и фигурами.</span><span class="sxs-lookup"><span data-stu-id="cf90e-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf90e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf90e-105">Remarks</span></span>

 <span data-ttu-id="cf90e-106">Microsoft Visio использует ячейку Relationships для хранения связей, которые связаны с этой фигурой.</span><span class="sxs-lookup"><span data-stu-id="cf90e-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="cf90e-107">Для представления отношений с этой фигурой используется серия функций DEPENDSON с показанными параметрами, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cf90e-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="cf90e-108">**Первый параметр**</span><span class="sxs-lookup"><span data-stu-id="cf90e-108">**First parameter**</span></span>|<span data-ttu-id="cf90e-109">**Дополнительные параметры**</span><span class="sxs-lookup"><span data-stu-id="cf90e-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf90e-110">1</span><span class="sxs-lookup"><span data-stu-id="cf90e-110">1</span></span>  <br/> |<span data-ttu-id="cf90e-111">Фигуры, которые являются членами этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="cf90e-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="cf90e-112">2</span><span class="sxs-lookup"><span data-stu-id="cf90e-112">2</span></span>  <br/> |<span data-ttu-id="cf90e-113">Фигуры, которые являются участниками этого списка.</span><span class="sxs-lookup"><span data-stu-id="cf90e-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="cf90e-114">3</span><span class="sxs-lookup"><span data-stu-id="cf90e-114">3</span></span>  <br/> |<span data-ttu-id="cf90e-115">Вызовы, связанные с этой фигурой.</span><span class="sxs-lookup"><span data-stu-id="cf90e-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="cf90e-116">4 </span><span class="sxs-lookup"><span data-stu-id="cf90e-116">4</span></span>  <br/> |<span data-ttu-id="cf90e-117">Контейнеры, в которые входит эта фигура.</span><span class="sxs-lookup"><span data-stu-id="cf90e-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="cf90e-118">5 </span><span class="sxs-lookup"><span data-stu-id="cf90e-118">5</span></span>  <br/> |<span data-ttu-id="cf90e-119">Список, в который входит этот элемент списка.</span><span class="sxs-lookup"><span data-stu-id="cf90e-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="cf90e-120">6 </span><span class="sxs-lookup"><span data-stu-id="cf90e-120">6</span></span>  <br/> |<span data-ttu-id="cf90e-121">Форма, связанная с этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="cf90e-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="cf90e-122">7 </span><span class="sxs-lookup"><span data-stu-id="cf90e-122">7</span></span>  <br/> |<span data-ttu-id="cf90e-123">Контейнер на левом краю границы, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="cf90e-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="cf90e-124">8 </span><span class="sxs-lookup"><span data-stu-id="cf90e-124">8</span></span>  <br/> |<span data-ttu-id="cf90e-125">Контейнер на правом пограничном краю, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="cf90e-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="cf90e-126">9 </span><span class="sxs-lookup"><span data-stu-id="cf90e-126">9</span></span>  <br/> |<span data-ttu-id="cf90e-127">Контейнер на верхнем краю границы, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="cf90e-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="cf90e-128">10 </span><span class="sxs-lookup"><span data-stu-id="cf90e-128">10</span></span>  <br/> |<span data-ttu-id="cf90e-129">Контейнер на нижнем краю границы, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="cf90e-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="cf90e-130">11</span><span class="sxs-lookup"><span data-stu-id="cf90e-130">11</span></span>  <br/> |<span data-ttu-id="cf90e-131">Перечислить, что этот список перекрывается.</span><span class="sxs-lookup"><span data-stu-id="cf90e-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="cf90e-132">Чтобы получить ссылку на ячейку Relationships по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="cf90e-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf90e-133">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cf90e-133">Cell name:</span></span>  <br/> |<span data-ttu-id="cf90e-134">Связи</span><span class="sxs-lookup"><span data-stu-id="cf90e-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="cf90e-135">Чтобы получить ссылку на ячейку Relationships по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cf90e-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf90e-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cf90e-136">Section index:</span></span>  <br/> |<span data-ttu-id="cf90e-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf90e-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cf90e-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cf90e-138">Row index:</span></span>  <br/> |<span data-ttu-id="cf90e-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="cf90e-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="cf90e-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cf90e-140">Cell index:</span></span>  <br/> |<span data-ttu-id="cf90e-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="cf90e-141">**visSLORelationships**</span></span> <br/> |
   

