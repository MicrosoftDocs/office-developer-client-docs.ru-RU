---
title: ShapePermeableX Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Определяет, может ли соединителю маршрутить по горизонтали через фигуру.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409477"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="e4386-103">ShapePermeableX Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e4386-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="e4386-104">Определяет, может ли соединителю маршрутить по горизонтали через фигуру.</span><span class="sxs-lookup"><span data-stu-id="e4386-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="e4386-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e4386-105">**Value**</span></span>|<span data-ttu-id="e4386-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e4386-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4386-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e4386-107">TRUE</span></span>  <br/> |<span data-ttu-id="e4386-108">Включить соединители для горизонтального маршрута через фигуру.</span><span class="sxs-lookup"><span data-stu-id="e4386-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="e4386-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e4386-109">FALSE</span></span>  <br/> |<span data-ttu-id="e4386-110">Не позволяйте соединителю проходить горизонтально через фигуру.</span><span class="sxs-lookup"><span data-stu-id="e4386-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4386-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4386-111">Remarks</span></span>

<span data-ttu-id="e4386-112">Вы также можете установить значение этой  ячейки  на вкладке Размещение в диалоговом [](run-in-developer-mode-display-the-developer-tab.md) окне Поведение (с выбранной фигурой на вкладке Разработчик, в группе **Shape Design** нажмите кнопку **Поведение,** а затем щелкните вкладку **Размещение).**</span><span class="sxs-lookup"><span data-stu-id="e4386-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="e4386-113">В версиях, ранее Visio 2000 г., вы установите это поведение с помощью ячейки ObjInteract в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="e4386-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="e4386-114">Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e4386-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4386-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e4386-115">Cell name:</span></span>  <br/> |<span data-ttu-id="e4386-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="e4386-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="e4386-117">Чтобы получить ссылку на ячейку ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e4386-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4386-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e4386-118">Section index:</span></span>  <br/> |<span data-ttu-id="e4386-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e4386-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e4386-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e4386-120">Row index:</span></span>  <br/> |<span data-ttu-id="e4386-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="e4386-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="e4386-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e4386-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e4386-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="e4386-123">**visSLOPermX**</span></span> <br/> |
   

