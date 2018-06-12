---
title: Отношения между ячейки (раздел макет фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Сохранение отношения между контейнеров, списков, выноски и фигур.
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814561"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="19799-103">Отношения между ячейки (раздел макет фигуры)</span><span class="sxs-lookup"><span data-stu-id="19799-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="19799-104">Сохранение отношения между контейнеров, списков, выноски и фигур.</span><span class="sxs-lookup"><span data-stu-id="19799-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19799-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="19799-105">Remarks</span></span>

 <span data-ttu-id="19799-106">Microsoft Visio использует ячейки связей для хранения отношений с участием этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="19799-107">Ряд функций DEPENDSON, с параметрами, используются для представления отношения с этой фигуры, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="19799-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="19799-108">**Первым параметром**</span><span class="sxs-lookup"><span data-stu-id="19799-108">**First parameter**</span></span>|<span data-ttu-id="19799-109">**Дополнительные параметры**</span><span class="sxs-lookup"><span data-stu-id="19799-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19799-110">1</span><span class="sxs-lookup"><span data-stu-id="19799-110">1</span></span>  <br/> |<span data-ttu-id="19799-111">Фигуры, которые являются членами этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="19799-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="19799-112">2</span><span class="sxs-lookup"><span data-stu-id="19799-112">2</span></span>  <br/> |<span data-ttu-id="19799-113">Фигуры, которые являются членами этого списка.</span><span class="sxs-lookup"><span data-stu-id="19799-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="19799-114">3</span><span class="sxs-lookup"><span data-stu-id="19799-114">3</span></span>  <br/> |<span data-ttu-id="19799-115">Выноски, связанных с этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="19799-116">4</span><span class="sxs-lookup"><span data-stu-id="19799-116">4</span></span>  <br/> |<span data-ttu-id="19799-117">Контейнеры, которые принадлежит этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="19799-118">5</span><span class="sxs-lookup"><span data-stu-id="19799-118">5</span></span>  <br/> |<span data-ttu-id="19799-119">Список, принадлежит этот элемент списка.</span><span class="sxs-lookup"><span data-stu-id="19799-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="19799-120">6</span><span class="sxs-lookup"><span data-stu-id="19799-120">6</span></span>  <br/> |<span data-ttu-id="19799-121">Фигура, связанный с этой выноски.</span><span class="sxs-lookup"><span data-stu-id="19799-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="19799-122">7</span><span class="sxs-lookup"><span data-stu-id="19799-122">7</span></span>  <br/> |<span data-ttu-id="19799-123">Контейнер на левой границе, из которых стоит этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="19799-124">8</span><span class="sxs-lookup"><span data-stu-id="19799-124">8</span></span>  <br/> |<span data-ttu-id="19799-125">Контейнер на правой границе, из которых стоит этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="19799-126">9</span><span class="sxs-lookup"><span data-stu-id="19799-126">9</span></span>  <br/> |<span data-ttu-id="19799-127">Контейнер на верхней границе, из которых стоит этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="19799-128">10</span><span class="sxs-lookup"><span data-stu-id="19799-128">10</span></span>  <br/> |<span data-ttu-id="19799-129">Контейнер на нижней границе которого располагается этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="19799-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="19799-130">11</span><span class="sxs-lookup"><span data-stu-id="19799-130">11</span></span>  <br/> |<span data-ttu-id="19799-131">Список, перекрывается этого списка.</span><span class="sxs-lookup"><span data-stu-id="19799-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="19799-132">Для получения ссылки на ячейку связи по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="19799-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19799-133">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="19799-133">Cell name:</span></span>  <br/> |<span data-ttu-id="19799-134">Связи</span><span class="sxs-lookup"><span data-stu-id="19799-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="19799-135">Для получения ссылки на ячейки связи по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="19799-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19799-136">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="19799-136">Section index:</span></span>  <br/> |<span data-ttu-id="19799-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19799-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="19799-138">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="19799-138">Row index:</span></span>  <br/> |<span data-ttu-id="19799-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="19799-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="19799-140">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="19799-140">Cell index:</span></span>  <br/> |<span data-ttu-id="19799-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="19799-141">**visSLORelationships**</span></span> <br/> |
   

