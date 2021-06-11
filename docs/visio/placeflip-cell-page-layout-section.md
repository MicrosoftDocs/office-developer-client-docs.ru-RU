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
description: Определяет, как фигуры переворачиваются и/или вращаются на странице при использовании диалогового окна Настройка макета (на вкладке Дизайн, в группе Макет, щелкните Re-Layout страницу, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434300"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="4675c-103">PlaceFlip Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="4675c-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="4675c-104">Определяет, как фигуры переворачиваются и/или вращаются на странице при использовании диалогового окна **Configure Layout** (на вкладке Design, в группе **Макет,** щелкните Страницу повторного макета **и** нажмите кнопку Дополнительные параметры  макета). </span><span class="sxs-lookup"><span data-stu-id="4675c-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="4675c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4675c-105">**Value**</span></span>|<span data-ttu-id="4675c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4675c-106">**Description**</span></span>|<span data-ttu-id="4675c-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="4675c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4675c-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="4675c-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="4675c-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4675c-109">Default.</span></span> <span data-ttu-id="4675c-110">Не переворачивать.</span><span class="sxs-lookup"><span data-stu-id="4675c-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="4675c-111">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="4675c-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="4675c-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="4675c-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="4675c-113">Переверните горизонтально.</span><span class="sxs-lookup"><span data-stu-id="4675c-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="4675c-114">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="4675c-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="4675c-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="4675c-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="4675c-116">Переверните вертикаль.</span><span class="sxs-lookup"><span data-stu-id="4675c-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="4675c-117">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="4675c-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="4675c-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="4675c-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="4675c-119">Flip in 90 degree increments.</span><span class="sxs-lookup"><span data-stu-id="4675c-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="4675c-120">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="4675c-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="4675c-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="4675c-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="4675c-122">Не переворачивать.</span><span class="sxs-lookup"><span data-stu-id="4675c-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="4675c-123">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="4675c-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4675c-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="4675c-124">Remarks</span></span>

<span data-ttu-id="4675c-125">Значение в ячейке PlaceFlip помогает сориентировать фигуру на следующую, к ней подключенную.</span><span class="sxs-lookup"><span data-stu-id="4675c-125">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span> <span data-ttu-id="4675c-126">Обычно используется при разработке рисунков с использованием статического клея.</span><span class="sxs-lookup"><span data-stu-id="4675c-126">It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="4675c-127">Чтобы настроить такое поведение для определенной формы, используйте ячейку ShapePlaceFlip в разделе Макет фигуры.</span><span class="sxs-lookup"><span data-stu-id="4675c-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="4675c-128">Чтобы получить ссылку на ячейку PlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4675c-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4675c-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4675c-129">Cell name:</span></span>  <br/> |<span data-ttu-id="4675c-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="4675c-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="4675c-131">Чтобы получить ссылку на ячейку PlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4675c-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4675c-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4675c-132">Section index:</span></span>  <br/> |<span data-ttu-id="4675c-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4675c-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4675c-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4675c-134">Row index:</span></span>  <br/> |<span data-ttu-id="4675c-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4675c-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="4675c-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4675c-136">Cell index:</span></span>  <br/> |<span data-ttu-id="4675c-137">**visPLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="4675c-137">**visPLOPlaceFlip**</span></span> <br/> |
   

