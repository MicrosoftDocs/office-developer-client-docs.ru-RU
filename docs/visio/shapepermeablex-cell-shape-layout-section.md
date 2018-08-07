---
title: Ячейка ShapePermeableX (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Определяет, будет ли соединитель могут направляться по горизонтали размещаемой фигуры.
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814778"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="3a3c2-103">Ячейка ShapePermeableX (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="3a3c2-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="3a3c2-104">Определяет, будет ли соединитель могут направляться по горизонтали размещаемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="3a3c2-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="3a3c2-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3a3c2-105">**Value**</span></span>|<span data-ttu-id="3a3c2-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a3c2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a3c2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a3c2-107">TRUE</span></span>  <br/> |<span data-ttu-id="3a3c2-108">Включение соединителей для маршрутизации по горизонтали через размещаемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="3a3c2-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="3a3c2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a3c2-109">FALSE</span></span>  <br/> |<span data-ttu-id="3a3c2-110">Нельзя допускать маршрут соединители горизонтально через размещаемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="3a3c2-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a3c2-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a3c2-111">Remarks</span></span>

<span data-ttu-id="3a3c2-112">Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="3a3c2-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="3a3c2-113">В версии более ранней, чем Visio 2000 устанавливаются это поведение с помощью ObjInteract ячейки в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="3a3c2-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="3a3c2-114">Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3a3c2-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a3c2-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3a3c2-115">Cell name:</span></span>  <br/> |<span data-ttu-id="3a3c2-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="3a3c2-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="3a3c2-117">Для получения ссылки на ячейки ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3a3c2-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a3c2-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3a3c2-118">Section index:</span></span>  <br/> |<span data-ttu-id="3a3c2-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a3c2-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3a3c2-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3a3c2-120">Row index:</span></span>  <br/> |<span data-ttu-id="3a3c2-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="3a3c2-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="3a3c2-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3a3c2-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3a3c2-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="3a3c2-123">**visSLOPermX**</span></span> <br/> |
   

