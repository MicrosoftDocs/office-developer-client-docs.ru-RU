---
title: ShapePlowCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Определяет, отодвигается ли эта фигура при падении другой фигуры рядом с этой фигурой на странице рисования.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423897"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="68500-103">ShapePlowCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="68500-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="68500-104">Определяет, отодвигается ли эта фигура при падении другой фигуры рядом с этой фигурой на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="68500-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="68500-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68500-105">**Value**</span></span>|<span data-ttu-id="68500-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68500-106">**Description**</span></span>|<span data-ttu-id="68500-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="68500-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68500-108">0</span><span class="sxs-lookup"><span data-stu-id="68500-108">0</span></span>  <br/> |<span data-ttu-id="68500-109">Plow as page specifies.</span><span class="sxs-lookup"><span data-stu-id="68500-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="68500-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="68500-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="68500-111">1</span><span class="sxs-lookup"><span data-stu-id="68500-111">1</span></span>  <br/> |<span data-ttu-id="68500-112">Plow no shapes.</span><span class="sxs-lookup"><span data-stu-id="68500-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="68500-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="68500-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="68500-114">2</span><span class="sxs-lookup"><span data-stu-id="68500-114">2</span></span>  <br/> |<span data-ttu-id="68500-115">Plow every shape.</span><span class="sxs-lookup"><span data-stu-id="68500-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="68500-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="68500-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68500-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="68500-117">Remarks</span></span>

<span data-ttu-id="68500-118">Вы также можете установить значение этой ячейки для определенной  фигуры на вкладке Размещение в [](run-in-developer-mode-display-the-developer-tab.md) диалоговом окне Поведение (с выбранной фигурой, на вкладке Разработчик, в группе **Shape Design,** **щелкните** Поведение, а затем нажмите вкладку **Размещение).** </span><span class="sxs-lookup"><span data-stu-id="68500-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="68500-119">Чтобы установить такое поведение  *для всех*  фигур на странице рисования, используйте ячейку PlowCode в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="68500-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="68500-120">Чтобы получить ссылку на ячейку ShapePlowCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="68500-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68500-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="68500-121">Cell name:</span></span>  <br/> |<span data-ttu-id="68500-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="68500-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="68500-123">Чтобы получить ссылку на ячейку ShapePlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="68500-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68500-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="68500-124">Section index:</span></span>  <br/> |<span data-ttu-id="68500-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68500-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="68500-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="68500-126">Row index:</span></span>  <br/> |<span data-ttu-id="68500-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="68500-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="68500-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="68500-128">Cell index:</span></span>  <br/> |<span data-ttu-id="68500-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="68500-129">**visSLOPlowCode**</span></span> <br/> |
   

