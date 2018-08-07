---
title: Ячейка DisplayLevel (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Определяет диапазон уровня отображения (относительное диапазон из Z-порядка группировки) для фигуры.
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813590"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="05dbe-103">Ячейка DisplayLevel (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="05dbe-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="05dbe-104">Определяет диапазон уровня отображения (относительное диапазон из Z-порядка группировки) для фигуры.</span><span class="sxs-lookup"><span data-stu-id="05dbe-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05dbe-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="05dbe-105">Remarks</span></span>

<span data-ttu-id="05dbe-106">Z-порядка является порядок отображения для фигур на странице документа.</span><span class="sxs-lookup"><span data-stu-id="05dbe-106">Z-order is the display order for shapes on the drawing page.</span></span> <span data-ttu-id="05dbe-107">Фигура, находящегося выше в Z-порядке отображается перед фигуры нижнего уровня в Z-порядке, когда один из другой перекрытий фигур.</span><span class="sxs-lookup"><span data-stu-id="05dbe-107">A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="05dbe-108">Разделяет уровня отображения с фигурами в группы или полосами.</span><span class="sxs-lookup"><span data-stu-id="05dbe-108">The display level divides shapes into groupings, or bands.</span></span> <span data-ttu-id="05dbe-109">Все фигуры в полосе заданного иметь выше Z-порядка чем фигур в нижней панели.</span><span class="sxs-lookup"><span data-stu-id="05dbe-109">All shapes in a given band have a higher Z-order than the shapes in a lower band.</span></span> <span data-ttu-id="05dbe-110">По умолчанию большинство фигур имеют уровень отображения нуль (0).</span><span class="sxs-lookup"><span data-stu-id="05dbe-110">By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="05dbe-111">Диапазон отображаемых уровней — от-32,767 +32,767.</span><span class="sxs-lookup"><span data-stu-id="05dbe-111">The range of display levels is from -32,767 to +32,767.</span></span> <span data-ttu-id="05dbe-112">Фигуры, которые имеют тот же уровень отображения объединяются в одном регулирования, в котором они также ранжируются относительно друг с другом по оси z.</span><span class="sxs-lookup"><span data-stu-id="05dbe-112">Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="05dbe-113">Z-порядка фигур в полосе можно изменить с помощью команды **Переместить вперед**, **Переместить назад**, **на передний план**и **на задний план**.</span><span class="sxs-lookup"><span data-stu-id="05dbe-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="05dbe-114">Если эти команды Переместить фигуру из заданного расположения, Microsoft Visio значение зарезервировано -32768 в ячейке DisplayLevel фигуры, если не защищены ячейки.</span><span class="sxs-lookup"><span data-stu-id="05dbe-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="05dbe-115">В этом случае фигуры не могут перемещаться в другом и Visio отображается предупреждение «защиты и/или уровень со свойствами не удается завершить выполнение этой команды».</span><span class="sxs-lookup"><span data-stu-id="05dbe-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="05dbe-116">Для получения ссылки на ячейку DisplayLevel по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующее.</span><span class="sxs-lookup"><span data-stu-id="05dbe-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05dbe-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="05dbe-117">Cell name:</span></span>  <br/> |<span data-ttu-id="05dbe-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="05dbe-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="05dbe-119">Для получения ссылки на ячейки DisplayLevel по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="05dbe-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05dbe-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="05dbe-120">Section index:</span></span>  <br/> |<span data-ttu-id="05dbe-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05dbe-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="05dbe-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="05dbe-122">Row index:</span></span>  <br/> |<span data-ttu-id="05dbe-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="05dbe-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="05dbe-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="05dbe-124">Cell index:</span></span>  <br/> |<span data-ttu-id="05dbe-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="05dbe-125">**visSLODisplayLevel**</span></span> <br/> |
   

