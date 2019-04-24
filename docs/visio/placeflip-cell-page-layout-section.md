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
description: Определяет, как размещаемые фигуры отворачиваются и/или поворачиваются на странице при использовании диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: d1c31654782012b3536d35f3a12a923c2cc7a8f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346874"
---
# <a name="placeflip-cell-page-layout-section"></a><span data-ttu-id="d822a-103">PlaceFlip Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d822a-103">PlaceFlip Cell (Page Layout Section)</span></span>

<span data-ttu-id="d822a-104">Определяет, как размещаемые фигуры отворачиваются и/или поворачиваются на странице при использовании диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем щелкните **Дополнительные параметры макета**).</span><span class="sxs-lookup"><span data-stu-id="d822a-104">Determines how placeable shapes flip and/or rotate on a page when you use the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="d822a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="d822a-105">**Value**</span></span>|<span data-ttu-id="d822a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d822a-106">**Description**</span></span>|<span data-ttu-id="d822a-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="d822a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d822a-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="d822a-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="d822a-109">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d822a-109">Default.</span></span> <span data-ttu-id="d822a-110">Не переворачиваются.</span><span class="sxs-lookup"><span data-stu-id="d822a-110">Do not flip.</span></span>  <br/> |<span data-ttu-id="d822a-111">**Вислофлипдефаулт**</span><span class="sxs-lookup"><span data-stu-id="d822a-111">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="d822a-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="d822a-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="d822a-113">ОтРазить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="d822a-113">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="d822a-114">**Вислофлипкс**</span><span class="sxs-lookup"><span data-stu-id="d822a-114">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="d822a-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="d822a-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="d822a-116">ОтРазить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="d822a-116">Flip vertical.</span></span>  <br/> |<span data-ttu-id="d822a-117">**Вислофлипи**</span><span class="sxs-lookup"><span data-stu-id="d822a-117">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="d822a-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="d822a-118">&amp;H4</span></span>  <br/> |<span data-ttu-id="d822a-119">ОтРазить при увеличении на 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="d822a-119">Flip in 90 degree increments.</span></span>  <br/> |<span data-ttu-id="d822a-120">**Вислофлипротате**</span><span class="sxs-lookup"><span data-stu-id="d822a-120">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="d822a-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="d822a-121">&amp;H8</span></span>  <br/> |<span data-ttu-id="d822a-122">Не переворачиваются.</span><span class="sxs-lookup"><span data-stu-id="d822a-122">Do not flip.</span></span>  <br/> |<span data-ttu-id="d822a-123">**Вислофлипноне**</span><span class="sxs-lookup"><span data-stu-id="d822a-123">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d822a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="d822a-124">Remarks</span></span>

<span data-ttu-id="d822a-125">Значение в ячейке PlaceFlip помогает расположить размещаемую фигуру в направлении следующей размещенной фигуры, к которой она подключена.</span><span class="sxs-lookup"><span data-stu-id="d822a-125">The value in the PlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span> <span data-ttu-id="d822a-126">Он обычно используется при разметке рисунков, использующих статическую привязывание.</span><span class="sxs-lookup"><span data-stu-id="d822a-126">It is typically used when laying out drawings that use static glue.</span></span>
  
<span data-ttu-id="d822a-127">Чтобы задать такое поведение для конкретной фигуры, используйте ячейку ShapePlaceFlip в разделе Макет фигуры.</span><span class="sxs-lookup"><span data-stu-id="d822a-127">To set this behavior for a particular shape, use the ShapePlaceFlip cell in the Shape Layout section.</span></span>
  
<span data-ttu-id="d822a-128">Чтобы получить ссылку на ячейку PlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="d822a-128">To get a reference to the PlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d822a-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d822a-129">Cell name:</span></span>  <br/> |<span data-ttu-id="d822a-130">PlaceFlip</span><span class="sxs-lookup"><span data-stu-id="d822a-130">PlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="d822a-131">Чтобы получить ссылку на ячейку PlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d822a-131">To get a reference to the PlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d822a-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d822a-132">Section index:</span></span>  <br/> |<span data-ttu-id="d822a-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d822a-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d822a-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d822a-134">Row index:</span></span>  <br/> |<span data-ttu-id="d822a-135">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="d822a-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d822a-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d822a-136">Cell index:</span></span>  <br/> |<span data-ttu-id="d822a-137">**Висплоплацефлип**</span><span class="sxs-lookup"><span data-stu-id="d822a-137">**visPLOPlaceFlip**</span></span> <br/> |
   

