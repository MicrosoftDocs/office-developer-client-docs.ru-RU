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
description: Хранит связи между контейнерами, списками, вызовами и фигурами.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406411"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="8ed03-103">Relationships Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="8ed03-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="8ed03-104">Хранит связи между контейнерами, списками, вызовами и фигурами.</span><span class="sxs-lookup"><span data-stu-id="8ed03-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8ed03-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed03-105">Remarks</span></span>

 <span data-ttu-id="8ed03-106">Microsoft Visio использует ячейку Relationships для хранения связей, которые связаны с этой фигурой.</span><span class="sxs-lookup"><span data-stu-id="8ed03-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="8ed03-107">Ряд функций DEPENDSON с показанными параметрами используется для представления связей с этой фигурой, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ed03-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="8ed03-108">**Первый параметр**</span><span class="sxs-lookup"><span data-stu-id="8ed03-108">**First parameter**</span></span>|<span data-ttu-id="8ed03-109">**Дополнительные параметры**</span><span class="sxs-lookup"><span data-stu-id="8ed03-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ed03-110">1 </span><span class="sxs-lookup"><span data-stu-id="8ed03-110">1</span></span>  <br/> |<span data-ttu-id="8ed03-111">Фигуры, которые являются членами этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8ed03-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="8ed03-112">2 </span><span class="sxs-lookup"><span data-stu-id="8ed03-112">2</span></span>  <br/> |<span data-ttu-id="8ed03-113">Фигуры, которые являются членами этого списка.</span><span class="sxs-lookup"><span data-stu-id="8ed03-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="8ed03-114">3 </span><span class="sxs-lookup"><span data-stu-id="8ed03-114">3</span></span>  <br/> |<span data-ttu-id="8ed03-115">Вызовы, связанные с этой фигурой.</span><span class="sxs-lookup"><span data-stu-id="8ed03-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="8ed03-116">4 </span><span class="sxs-lookup"><span data-stu-id="8ed03-116">4</span></span>  <br/> |<span data-ttu-id="8ed03-117">Контейнеры, в которые входит эта фигура.</span><span class="sxs-lookup"><span data-stu-id="8ed03-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="8ed03-118">5 </span><span class="sxs-lookup"><span data-stu-id="8ed03-118">5</span></span>  <br/> |<span data-ttu-id="8ed03-119">Список элементов списка.</span><span class="sxs-lookup"><span data-stu-id="8ed03-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="8ed03-120">6 </span><span class="sxs-lookup"><span data-stu-id="8ed03-120">6</span></span>  <br/> |<span data-ttu-id="8ed03-121">Фигура, связанная с этой вызовите.</span><span class="sxs-lookup"><span data-stu-id="8ed03-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="8ed03-122">7 </span><span class="sxs-lookup"><span data-stu-id="8ed03-122">7</span></span>  <br/> |<span data-ttu-id="8ed03-123">Контейнер, на левом границе которого находится фигура.</span><span class="sxs-lookup"><span data-stu-id="8ed03-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="8ed03-124">8 </span><span class="sxs-lookup"><span data-stu-id="8ed03-124">8</span></span>  <br/> |<span data-ttu-id="8ed03-125">Контейнер на правом пограничном границе, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="8ed03-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="8ed03-126">9 </span><span class="sxs-lookup"><span data-stu-id="8ed03-126">9</span></span>  <br/> |<span data-ttu-id="8ed03-127">Контейнер на верхней границе края, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="8ed03-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="8ed03-128">10 </span><span class="sxs-lookup"><span data-stu-id="8ed03-128">10</span></span>  <br/> |<span data-ttu-id="8ed03-129">Контейнер на нижнем краю границы, на котором расположена эта фигура.</span><span class="sxs-lookup"><span data-stu-id="8ed03-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="8ed03-130">11</span><span class="sxs-lookup"><span data-stu-id="8ed03-130">11</span></span>  <br/> |<span data-ttu-id="8ed03-131">Список перекрывающихся списков.</span><span class="sxs-lookup"><span data-stu-id="8ed03-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="8ed03-132">Чтобы получить ссылку на ячейку Relationships по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8ed03-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed03-133">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ed03-133">Cell name:</span></span>  <br/> |<span data-ttu-id="8ed03-134">Связи</span><span class="sxs-lookup"><span data-stu-id="8ed03-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="8ed03-135">Чтобы получить ссылку на ячейку Relationships по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8ed03-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ed03-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8ed03-136">Section index:</span></span>  <br/> |<span data-ttu-id="8ed03-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8ed03-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8ed03-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8ed03-138">Row index:</span></span>  <br/> |<span data-ttu-id="8ed03-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="8ed03-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="8ed03-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ed03-140">Cell index:</span></span>  <br/> |<span data-ttu-id="8ed03-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="8ed03-141">**visSLORelationships**</span></span> <br/> |
   

