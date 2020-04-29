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
description: Определяет, может ли соединитель маршрутизироваться горизонтально через размещаемую фигуру.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409477"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="29135-103">ShapePermeableX Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="29135-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="29135-104">Определяет, может ли соединитель маршрутизироваться горизонтально через размещаемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="29135-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="29135-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="29135-105">**Value**</span></span>|<span data-ttu-id="29135-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29135-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29135-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="29135-107">TRUE</span></span>  <br/> |<span data-ttu-id="29135-108">Включить соединители для горизонтальной маршрутизации через размещаемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="29135-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="29135-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="29135-109">FALSE</span></span>  <br/> |<span data-ttu-id="29135-110">Не додавайте соединители маршрутизировать их горизонтально через размещаемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="29135-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29135-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="29135-111">Remarks</span></span>

<span data-ttu-id="29135-112">Вы также можете задать значение этой ячейки на вкладке **Размещение** в диалоговом окне **поведение** (с выбранной фигурой на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , в группе **Макет фигуры** щелкните **поведение**, а затем перейдите на вкладку **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="29135-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="29135-113">В версиях, предшествующих Visio 2000, это поведение задается с помощью ячейки Обжинтеракт в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="29135-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="29135-114">Чтобы получить ссылку на ячейку ShapePermeableX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="29135-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29135-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="29135-115">Cell name:</span></span>  <br/> |<span data-ttu-id="29135-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="29135-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="29135-117">Чтобы получить ссылку на ячейку ShapePermeableX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="29135-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29135-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="29135-118">Section index:</span></span>  <br/> |<span data-ttu-id="29135-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29135-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="29135-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="29135-120">Row index:</span></span>  <br/> |<span data-ttu-id="29135-121">**висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="29135-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="29135-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="29135-122">Cell index:</span></span>  <br/> |<span data-ttu-id="29135-123">**висслопермкс**</span><span class="sxs-lookup"><span data-stu-id="29135-123">**visSLOPermX**</span></span> <br/> |
   

