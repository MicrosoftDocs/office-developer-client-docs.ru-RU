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
description: Определяет, будет ли перемещаться эта размещаемая фигура при перетаскивании другой размещенной фигуры возле этой фигуры на странице документа.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423897"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="b6439-103">ShapePlowCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b6439-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="b6439-104">Определяет, будет ли перемещаться эта размещаемая фигура при перетаскивании другой размещенной фигуры возле этой фигуры на странице документа.</span><span class="sxs-lookup"><span data-stu-id="b6439-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="b6439-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b6439-105">**Value**</span></span>|<span data-ttu-id="b6439-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6439-106">**Description**</span></span>|<span data-ttu-id="b6439-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="b6439-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6439-108">нуль</span><span class="sxs-lookup"><span data-stu-id="b6439-108">0</span></span>  <br/> |<span data-ttu-id="b6439-109">Плов в качестве указания страницы.</span><span class="sxs-lookup"><span data-stu-id="b6439-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="b6439-110">**Висслопловдефаулт**</span><span class="sxs-lookup"><span data-stu-id="b6439-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="b6439-111">1,1</span><span class="sxs-lookup"><span data-stu-id="b6439-111">1</span></span>  <br/> |<span data-ttu-id="b6439-112">Плов без фигур.</span><span class="sxs-lookup"><span data-stu-id="b6439-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="b6439-113">**Висслопловневер**</span><span class="sxs-lookup"><span data-stu-id="b6439-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="b6439-114">2</span><span class="sxs-lookup"><span data-stu-id="b6439-114">2</span></span>  <br/> |<span data-ttu-id="b6439-115">Плов каждая фигура.</span><span class="sxs-lookup"><span data-stu-id="b6439-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="b6439-116">**Висслопловалвайс**</span><span class="sxs-lookup"><span data-stu-id="b6439-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6439-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6439-117">Remarks</span></span>

<span data-ttu-id="b6439-118">Вы также можете задать значение этой ячейки для конкретной фигуры на вкладке " **Размещение** " диалогового окна **поведение** (с выбранной фигурой на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Макет фигуры** , щелкните **поведение**, а затем нажмите кнопку Вкладка " **Размещение** ").</span><span class="sxs-lookup"><span data-stu-id="b6439-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="b6439-119">Чтобы задать это поведение для *всех* фигур на странице документа, используйте ячейку PlowCode в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="b6439-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="b6439-120">Чтобы получить ссылку на ячейку ShapePlowCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b6439-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6439-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6439-121">Cell name:</span></span>  <br/> |<span data-ttu-id="b6439-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="b6439-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="b6439-123">Чтобы получить ссылку на ячейку ShapePlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b6439-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6439-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b6439-124">Section index:</span></span>  <br/> |<span data-ttu-id="b6439-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6439-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b6439-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b6439-126">Row index:</span></span>  <br/> |<span data-ttu-id="b6439-127">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="b6439-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="b6439-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b6439-128">Cell index:</span></span>  <br/> |<span data-ttu-id="b6439-129">**Висслопловкоде**</span><span class="sxs-lookup"><span data-stu-id="b6439-129">**visSLOPlowCode**</span></span> <br/> |
   

