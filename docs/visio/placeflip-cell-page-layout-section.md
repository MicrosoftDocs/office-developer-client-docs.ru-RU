---
title: PlaceFlip Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253251
localization_priority: Normal
ms.assetid: df014b98-cfd5-b6d3-4b8a-b0acb3b94412
description: Определяет, как можно пролистыть и/или повернуть фигуры на странице при использовании диалогового окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout страницу, а затем щелкните "Дополнительные параметры макета").
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434300"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="93f72-103">PlaceFlip Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="93f72-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="93f72-104">Определяет, как меняющиеся фигуры меняются и/или поворачиваться на странице  при использовании диалогового окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" и выберите "Дополнительные параметры   макета"). </span><span class="sxs-lookup"><span data-stu-id="93f72-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="93f72-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="93f72-105">**Value**</span></span>|<span data-ttu-id="93f72-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93f72-106">**Description**</span></span>|<span data-ttu-id="93f72-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="93f72-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="93f72-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="93f72-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="93f72-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93f72-109">Default.</span></span> <span data-ttu-id="93f72-110">Не пролистыый.</span><span class="sxs-lookup"><span data-stu-id="93f72-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="93f72-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="93f72-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="93f72-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="93f72-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="93f72-113">Пролистывка по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="93f72-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="93f72-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="93f72-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="93f72-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="93f72-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="93f72-116">Вертикальная пролистывка.</span><span class="sxs-lookup"><span data-stu-id="93f72-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="93f72-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="93f72-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="93f72-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="93f72-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="93f72-119">Пролистывка с 90 градусами.</span><span class="sxs-lookup"><span data-stu-id="93f72-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="93f72-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="93f72-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="93f72-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="93f72-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="93f72-122">Не пролистыый.</span><span class="sxs-lookup"><span data-stu-id="93f72-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="93f72-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="93f72-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93f72-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="93f72-124">Remarks</span></span>

<span data-ttu-id="93f72-125">Значение в ячейке PlaceFlip помогает сориентировать поднимаемую фигуру на следующую фигуру, к ней подключено.</span><span class="sxs-lookup"><span data-stu-id="93f72-125">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span> <span data-ttu-id="93f72-126">Как правило, он используется при размыщении рисунков с использованием статического приклейки.</span><span class="sxs-lookup"><span data-stu-id="93f72-126">It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="93f72-127">Чтобы настроить это поведение для определенной фигуры, используйте ячейку ShapePlaceFlip в разделе "Макет фигуры".</span><span class="sxs-lookup"><span data-stu-id="93f72-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="93f72-128">Чтобы получить ссылку на ячейку PlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="93f72-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93f72-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="93f72-129">Cell name:</span></span>  <br/> |<span data-ttu-id="93f72-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="93f72-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="93f72-131">Чтобы получить ссылку на ячейку PlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="93f72-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93f72-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93f72-132">Section index:</span></span>  <br/> |<span data-ttu-id="93f72-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93f72-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="93f72-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93f72-134">Row index:</span></span>  <br/> |<span data-ttu-id="93f72-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="93f72-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="93f72-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93f72-136">Cell index:</span></span>  <br/> |<span data-ttu-id="93f72-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="93f72-137">**visPLOPlaceFlip**</span></span> <br/> |
   

