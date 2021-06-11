---
title: ShapePlaceFlip Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Определяет, как фигура переворачивается, вращается или как на странице, когда вы закладываете фигуры, используя диалоговое окно Configure Layout (на вкладке Дизайн, в группе Макет, щелкните Re-Layout Страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429280"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="f1deb-103">ShapePlaceFlip Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="f1deb-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f1deb-104">Определяет, как фигура переворачивается, вращается или как на странице, когда вы закладываете фигуры, используя  диалоговое окно **Configure** **Layout**(на вкладке Design, в группе **Макет,** щелкните страницу повторного макета **и** нажмите кнопку Дополнительные параметры макета).</span><span class="sxs-lookup"><span data-stu-id="f1deb-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="f1deb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f1deb-105">**Value**</span></span>|<span data-ttu-id="f1deb-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1deb-106">**Description**</span></span>|<span data-ttu-id="f1deb-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f1deb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1deb-108">0</span><span class="sxs-lookup"><span data-stu-id="f1deb-108">0</span></span>  <br/> |<span data-ttu-id="f1deb-109">Использование по умолчанию страницы.</span><span class="sxs-lookup"><span data-stu-id="f1deb-109">Use page default.</span></span>  <br/> |<span data-ttu-id="f1deb-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="f1deb-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="f1deb-111">1</span><span class="sxs-lookup"><span data-stu-id="f1deb-111">1</span></span>  <br/> |<span data-ttu-id="f1deb-112">Переверните горизонтально.</span><span class="sxs-lookup"><span data-stu-id="f1deb-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="f1deb-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="f1deb-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="f1deb-114">2</span><span class="sxs-lookup"><span data-stu-id="f1deb-114">2</span></span>  <br/> |<span data-ttu-id="f1deb-115">Переверните вертикаль.</span><span class="sxs-lookup"><span data-stu-id="f1deb-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="f1deb-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="f1deb-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="f1deb-117">4 </span><span class="sxs-lookup"><span data-stu-id="f1deb-117">4</span></span>  <br/> |<span data-ttu-id="f1deb-118">Переверните 90-градусные приращения между 0 и 270.</span><span class="sxs-lookup"><span data-stu-id="f1deb-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="f1deb-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="f1deb-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="f1deb-120">8 </span><span class="sxs-lookup"><span data-stu-id="f1deb-120">8</span></span>  <br/> |<span data-ttu-id="f1deb-121">Не переворачивать.</span><span class="sxs-lookup"><span data-stu-id="f1deb-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="f1deb-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="f1deb-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1deb-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1deb-123">Remarks</span></span>

<span data-ttu-id="f1deb-124">Значение в ячейке ShapePlaceFlip помогает сориентировать фигуру на следующую, к ней подключенную.</span><span class="sxs-lookup"><span data-stu-id="f1deb-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="f1deb-125">Чтобы установить это поведение для  *всех*  фигур на странице рисования, используйте ячейку PlaceFlip в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="f1deb-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="f1deb-126">Чтобы получить ссылку на ячейку ShapePlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f1deb-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1deb-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f1deb-127">Cell name:</span></span>  <br/> |<span data-ttu-id="f1deb-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="f1deb-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="f1deb-129">Чтобы получить ссылку на ячейку ShapePlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f1deb-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1deb-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f1deb-130">Section index:</span></span>  <br/> |<span data-ttu-id="f1deb-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f1deb-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f1deb-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f1deb-132">Row index:</span></span>  <br/> |<span data-ttu-id="f1deb-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="f1deb-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="f1deb-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f1deb-134">Cell index:</span></span>  <br/> |<span data-ttu-id="f1deb-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="f1deb-135">**visSLOPlaceFlip**</span></span> <br/> |
   

