---
title: ShapePermeableY Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Определяет, может ли соединитель проходить по вертикали через фигуру.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417520"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="9aed0-103">ShapePermeableY Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="9aed0-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9aed0-104">Определяет, может ли соединитель проходить по вертикали через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9aed0-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="9aed0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9aed0-105">**Value**</span></span>|<span data-ttu-id="9aed0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9aed0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9aed0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9aed0-107">TRUE</span></span>  <br/> |<span data-ttu-id="9aed0-108">Позволяет соединителям проходить по вертикали через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9aed0-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="9aed0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9aed0-109">FALSE</span></span>  <br/> |<span data-ttu-id="9aed0-110">Не позволяйте соединителям проходить по вертикали через фигуру.</span><span class="sxs-lookup"><span data-stu-id="9aed0-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9aed0-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="9aed0-111">Remarks</span></span>

<span data-ttu-id="9aed0-112">Вы также можете установить значение этой  ячейки  на вкладке "Размещение" в диалоговом окне  "Поведение" (с выбранной фигурой, на вкладке "Разработчик", в группе "Проектирование фигуры" щелкните "Поведение" и выберите вкладку **"Размещение").** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="9aed0-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="9aed0-113">В версиях, более ранних, чем Visio 2000, такое поведение задано с помощью ячейки ObjInteract в разделе "Прочие".</span><span class="sxs-lookup"><span data-stu-id="9aed0-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="9aed0-114">Чтобы получить ссылку на ячейку ShapePermeableY по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="9aed0-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9aed0-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9aed0-115">Cell name:</span></span>  <br/> |<span data-ttu-id="9aed0-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="9aed0-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="9aed0-117">Чтобы получить ссылку на ячейку ShapePermeableY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9aed0-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9aed0-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9aed0-118">Section index:</span></span>  <br/> |<span data-ttu-id="9aed0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9aed0-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9aed0-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9aed0-120">Row index:</span></span>  <br/> |<span data-ttu-id="9aed0-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9aed0-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9aed0-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9aed0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9aed0-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="9aed0-123">**visSLOPermY**</span></span> <br/> |
   

