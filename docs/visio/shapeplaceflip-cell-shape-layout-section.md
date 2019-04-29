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
description: Определяет способ отражения размещаемой фигуры, поворота или обеих страниц на странице при размещении фигур с помощью диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429280"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="81db0-103">ShapePlaceFlip Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="81db0-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="81db0-104">Определяет способ отражения и поворота размещаемой фигуры на странице при размещении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем нажмите кнопку Дополнительно). \*\* Параметры макета\*\*).</span><span class="sxs-lookup"><span data-stu-id="81db0-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="81db0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="81db0-105">**Value**</span></span>|<span data-ttu-id="81db0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81db0-106">**Description**</span></span>|<span data-ttu-id="81db0-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="81db0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81db0-108">нуль</span><span class="sxs-lookup"><span data-stu-id="81db0-108">0</span></span>  <br/> |<span data-ttu-id="81db0-109">Используйте страницу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="81db0-109">Use page default.</span></span>  <br/> |<span data-ttu-id="81db0-110">**Вислофлипдефаулт**</span><span class="sxs-lookup"><span data-stu-id="81db0-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="81db0-111">1,1</span><span class="sxs-lookup"><span data-stu-id="81db0-111">1</span></span>  <br/> |<span data-ttu-id="81db0-112">ОтРазить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="81db0-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="81db0-113">**Вислофлипкс**</span><span class="sxs-lookup"><span data-stu-id="81db0-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="81db0-114">2</span><span class="sxs-lookup"><span data-stu-id="81db0-114">2</span></span>  <br/> |<span data-ttu-id="81db0-115">ОтРазить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="81db0-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="81db0-116">**Вислофлипи**</span><span class="sxs-lookup"><span data-stu-id="81db0-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="81db0-117">SP4</span><span class="sxs-lookup"><span data-stu-id="81db0-117">4</span></span>  <br/> |<span data-ttu-id="81db0-118">ОтРазится на 90 градусов с шагом от 0 до 270.</span><span class="sxs-lookup"><span data-stu-id="81db0-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="81db0-119">**Вислофлипротате**</span><span class="sxs-lookup"><span data-stu-id="81db0-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="81db0-120">8,5</span><span class="sxs-lookup"><span data-stu-id="81db0-120">8</span></span>  <br/> |<span data-ttu-id="81db0-121">Не переворачиваются.</span><span class="sxs-lookup"><span data-stu-id="81db0-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="81db0-122">**Вислофлипноне**</span><span class="sxs-lookup"><span data-stu-id="81db0-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81db0-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="81db0-123">Remarks</span></span>

<span data-ttu-id="81db0-124">Значение в ячейке ShapePlaceFlip помогает расположить размещаемую фигуру в направлении следующей размещенной фигуры, к которой она подключена.</span><span class="sxs-lookup"><span data-stu-id="81db0-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="81db0-125">Чтобы задать это поведение для *всех* фигур на странице документа, используйте ячейку PlaceFlip в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="81db0-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="81db0-126">Чтобы получить ссылку на ячейку ShapePlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="81db0-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81db0-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="81db0-127">Cell name:</span></span>  <br/> |<span data-ttu-id="81db0-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="81db0-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="81db0-129">Чтобы получить ссылку на ячейку ShapePlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="81db0-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81db0-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81db0-130">Section index:</span></span>  <br/> |<span data-ttu-id="81db0-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81db0-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="81db0-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81db0-132">Row index:</span></span>  <br/> |<span data-ttu-id="81db0-133">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="81db0-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="81db0-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81db0-134">Cell index:</span></span>  <br/> |<span data-ttu-id="81db0-135">**Висслоплацефлип**</span><span class="sxs-lookup"><span data-stu-id="81db0-135">**visSLOPlaceFlip**</span></span> <br/> |
   

