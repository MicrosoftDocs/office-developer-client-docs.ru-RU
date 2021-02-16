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
description: Определяет полосу уровня отображения (относительный диапазон группировки Z-порядка) для фигуры.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408147"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="ccf65-103">DisplayLevel Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ccf65-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ccf65-104">Определяет полосу уровня отображения (относительный диапазон группировки Z-порядка) для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ccf65-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccf65-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ccf65-105">Remarks</span></span>

<span data-ttu-id="ccf65-106">Z-порядок — это порядок отображения фигур на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="ccf65-106">Z-order is the display order for shapes on the drawing page.</span></span> <span data-ttu-id="ccf65-107">Фигура, более высокая в Z-порядке, отображается перед фигурой, которая находится ниже в Z-порядке, когда одна из фигур наложения другого.</span><span class="sxs-lookup"><span data-stu-id="ccf65-107">A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="ccf65-108">Уровень отображения делит фигуры на группы или диапазоны.</span><span class="sxs-lookup"><span data-stu-id="ccf65-108">The display level divides shapes into groupings, or bands.</span></span> <span data-ttu-id="ccf65-109">Все фигуры в заданной полосе имеют более высокий Z-порядок, чем фигуры в нижней полосе.</span><span class="sxs-lookup"><span data-stu-id="ccf65-109">All shapes in a given band have a higher Z-order than the shapes in a lower band.</span></span> <span data-ttu-id="ccf65-110">По умолчанию большинство фигур имеют уровень отображения 0 (0).</span><span class="sxs-lookup"><span data-stu-id="ccf65-110">By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="ccf65-111">Диапазон уровней отображения — от -32 767 до +32 767.</span><span class="sxs-lookup"><span data-stu-id="ccf65-111">The range of display levels is from -32,767 to +32,767.</span></span> <span data-ttu-id="ccf65-112">Фигуры с одинаковым уровнем отображения объединяются в один диапазон, в котором они также ранжируются относительно друг друга по Z-порядку.</span><span class="sxs-lookup"><span data-stu-id="ccf65-112">Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="ccf65-113">Вы можете изменить Z-порядок фигур в пределах диапазона с помощью команд **"Переслать",**"Отправить назад", "На передний" и "Отправить **назад".**</span><span class="sxs-lookup"><span data-stu-id="ccf65-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="ccf65-114">Если эти команды перемещают фигуру из заданного диапазона, Microsoft Visio отображает зарезервированное значение -32768 в ячейке DisplayLevel фигуры, если ячейка не защищена.</span><span class="sxs-lookup"><span data-stu-id="ccf65-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="ccf65-115">В этом случае фигуру нельзя передвигать на другую полосу, и Visio отображает предупреждение "Защита фигуры и/или свойства слоя препятствуют полному выполнению этой команды".</span><span class="sxs-lookup"><span data-stu-id="ccf65-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="ccf65-116">Чтобы получить ссылку на ячейку DisplayLevel по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте следующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="ccf65-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccf65-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccf65-117">Cell name:</span></span>  <br/> |<span data-ttu-id="ccf65-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="ccf65-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="ccf65-119">Чтобы получить ссылку на ячейку DisplayLevel по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ccf65-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccf65-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ccf65-120">Section index:</span></span>  <br/> |<span data-ttu-id="ccf65-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ccf65-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ccf65-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ccf65-122">Row index:</span></span>  <br/> |<span data-ttu-id="ccf65-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ccf65-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="ccf65-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ccf65-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ccf65-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="ccf65-125">**visSLODisplayLevel**</span></span> <br/> |
   

