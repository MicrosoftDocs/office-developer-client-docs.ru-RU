---
title: DisplayLevel Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Определяет диапазон уровня отображения (относительный диапазон группировки Z-order) для формы.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408147"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="cbbfb-103">DisplayLevel Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="cbbfb-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="cbbfb-104">Определяет диапазон уровня отображения (относительный диапазон группировки Z-order) для формы.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cbbfb-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbbfb-105">Remarks</span></span>

<span data-ttu-id="cbbfb-106">Z-order — это порядок отображения фигур на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-106">Z-order is the display order for shapes on the drawing page.</span></span> <span data-ttu-id="cbbfb-107">Фигура, более высокая в Z-порядке, появляется перед фигурой, которая ниже в Z-порядке, когда одна из фигур наложения на другую.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-107">A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="cbbfb-108">Уровень отображения делит фигуры на группы или полосы.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-108">The display level divides shapes into groupings, or bands.</span></span> <span data-ttu-id="cbbfb-109">Все фигуры в данной группе имеют более высокий Z-порядок, чем фигуры в нижней полосе.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-109">All shapes in a given band have a higher Z-order than the shapes in a lower band.</span></span> <span data-ttu-id="cbbfb-110">По умолчанию большинство фигур имеют уровень отображения 0 (0).</span><span class="sxs-lookup"><span data-stu-id="cbbfb-110">By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="cbbfb-111">Диапазон уровней отображения от -32 767 до +32 767.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-111">The range of display levels is from -32,767 to +32,767.</span></span> <span data-ttu-id="cbbfb-112">Фигуры с одинаковым уровнем отображения объединяются в одну группу, в пределах которой они также ранжируются по отношению друг к другу по Z-порядку.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-112">Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="cbbfb-113">Вы можете изменить Z-порядок фигур в группе с помощью команд **Bring Forward,** **Send Backward,** **Bring to Front** и Send **to Back**.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="cbbfb-114">Если эти команды перемещают фигуру из данной полосы, microsoft Visio отображает зарезервированное значение -32768 в ячейке DisplayLevel фигуры, если ячейка не охраняется.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="cbbfb-115">В этом случае фигура не может быть перемещена в другую полосу, и Visio отображает предупреждение "Защита формы и/или свойства слоя препятствуют полному выполнению этой команды".</span><span class="sxs-lookup"><span data-stu-id="cbbfb-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="cbbfb-116">Чтобы получить ссылку на ячейку DisplayLevel по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте следующее.</span><span class="sxs-lookup"><span data-stu-id="cbbfb-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbbfb-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cbbfb-117">Cell name:</span></span>  <br/> |<span data-ttu-id="cbbfb-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="cbbfb-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="cbbfb-119">Чтобы получить ссылку на ячейку DisplayLevel по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cbbfb-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbbfb-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cbbfb-120">Section index:</span></span>  <br/> |<span data-ttu-id="cbbfb-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cbbfb-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cbbfb-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cbbfb-122">Row index:</span></span>  <br/> |<span data-ttu-id="cbbfb-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="cbbfb-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="cbbfb-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cbbfb-124">Cell index:</span></span>  <br/> |<span data-ttu-id="cbbfb-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="cbbfb-125">**visSLODisplayLevel**</span></span> <br/> |
   

