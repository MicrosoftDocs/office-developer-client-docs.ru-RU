---
title: Ячейка PlaceFlip (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Определяет, как размещаемые фигуры отразить и/или поворот на странице при использовании диалоговое окно "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: fb16849c7a496a4277133c68453d94d6fd2e67f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814368"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="6651d-103">Ячейка PlaceFlip (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="6651d-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="6651d-104">Определяет, как размещаемые фигуры отразить и/или поворот на странице при использовании диалоговое окно " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="6651d-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="6651d-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6651d-105">**Value**</span></span>|<span data-ttu-id="6651d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6651d-106">**Description**</span></span>|<span data-ttu-id="6651d-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="6651d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6651d-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="6651d-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="6651d-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6651d-109">Default.</span></span> <span data-ttu-id="6651d-110">Не отражение.</span><span class="sxs-lookup"><span data-stu-id="6651d-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="6651d-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="6651d-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="6651d-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="6651d-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="6651d-113">Слева направо.</span><span class="sxs-lookup"><span data-stu-id="6651d-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="6651d-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="6651d-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="6651d-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="6651d-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="6651d-116">Отразить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="6651d-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="6651d-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="6651d-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="6651d-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="6651d-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="6651d-119">Отразить на 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="6651d-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="6651d-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="6651d-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="6651d-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="6651d-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="6651d-122">Не отражение.</span><span class="sxs-lookup"><span data-stu-id="6651d-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="6651d-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="6651d-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6651d-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="6651d-124">Remarks</span></span>

<span data-ttu-id="6651d-125">Значение в ячейке PlaceFlip поможет сориентироваться размещаемой фигуры к следующей размещаемой фигуры, которым подключаются к.</span><span class="sxs-lookup"><span data-stu-id="6651d-125">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span> <span data-ttu-id="6651d-126">Обычно используется при создании макетов документы, которые используют статические связывающих.</span><span class="sxs-lookup"><span data-stu-id="6651d-126">It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="6651d-127">Чтобы задать это поведение для определенного фигуры, используйте ShapePlaceFlip ячейки в разделе Макет фигуры.</span><span class="sxs-lookup"><span data-stu-id="6651d-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="6651d-128">Чтобы получить ссылку на ячейку PlaceFlip по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="6651d-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6651d-129">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6651d-129">Cell name:</span></span>  <br/> |<span data-ttu-id="6651d-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="6651d-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="6651d-131">Для получения ссылки на ячейки PlaceFlip по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6651d-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6651d-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6651d-132">Section index:</span></span>  <br/> |<span data-ttu-id="6651d-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6651d-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6651d-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6651d-134">Row index:</span></span>  <br/> |<span data-ttu-id="6651d-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6651d-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6651d-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6651d-136">Cell index:</span></span>  <br/> |<span data-ttu-id="6651d-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="6651d-137">**visPLOPlaceFlip**</span></span> <br/> |
   

