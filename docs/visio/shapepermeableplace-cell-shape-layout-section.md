---
title: ShapePermeablePlace Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Определяет, можно ли размещать размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout page и выберите "Дополнительные параметры макета").
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427222"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="b3e93-103">ShapePermeablePlace Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b3e93-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="b3e93-104">Определяет, можно ли размещать размещаемые фигуры поверх фигуры при  размещении фигур в  диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" и выберите "Дополнительные параметры  макета"). </span><span class="sxs-lookup"><span data-stu-id="b3e93-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="b3e93-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b3e93-105">**Value**</span></span>|<span data-ttu-id="b3e93-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3e93-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3e93-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b3e93-107">TRUE</span></span>  <br/> |<span data-ttu-id="b3e93-108">Позволяет размещать фигуры поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3e93-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="b3e93-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b3e93-109">FALSE</span></span>  <br/> |<span data-ttu-id="b3e93-110">Не следует размещать фигуры поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="b3e93-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3e93-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3e93-111">Remarks</span></span>

<span data-ttu-id="b3e93-112">Вы также можете установить значение этой  ячейки  на вкладке "Размещение" в диалоговом окне  "Поведение" (с выбранной фигурой, на вкладке "Разработчик", в группе "Проектирование фигуры" щелкните "Поведение" и выберите вкладку **"Размещение").** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="b3e93-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="b3e93-113">В версиях, более ранних, чем Visio 2000, такое поведение задано с помощью ячейки ObjInteract в разделе "Прочие".</span><span class="sxs-lookup"><span data-stu-id="b3e93-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="b3e93-114">Чтобы получить ссылку на ячейку ShapePermeablePlace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b3e93-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3e93-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3e93-115">Cell name:</span></span>  <br/> |<span data-ttu-id="b3e93-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="b3e93-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="b3e93-117">Чтобы получить ссылку на ячейку ShapePermeablePlace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b3e93-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3e93-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3e93-118">Section index:</span></span>  <br/> |<span data-ttu-id="b3e93-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3e93-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b3e93-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3e93-120">Row index:</span></span>  <br/> |<span data-ttu-id="b3e93-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="b3e93-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="b3e93-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3e93-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b3e93-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="b3e93-123">**visSLOPermeablePlace**</span></span> <br/> |
   

