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
description: Определяет, как подкладываемая фигура пролистывает, поворачивается или и то, и другое на странице при выкладывке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета").
ms.openlocfilehash: 72ef1b67dd87d842e6a4372d1eb08d614f0eb2d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429280"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="18b87-103">ShapePlaceFlip Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="18b87-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="18b87-104">Определяет, как подкладываемая фигура пролистывает, поворачивается или и то,  и другое на странице  при выкладывке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" **и** выберите "Дополнительные параметры  макета"). </span><span class="sxs-lookup"><span data-stu-id="18b87-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="18b87-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="18b87-105">**Value**</span></span>|<span data-ttu-id="18b87-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18b87-106">**Description**</span></span>|<span data-ttu-id="18b87-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="18b87-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18b87-108">0</span><span class="sxs-lookup"><span data-stu-id="18b87-108">0</span></span>  <br/> |<span data-ttu-id="18b87-109">Используйте страницу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18b87-109">Use page default.</span></span>  <br/> |<span data-ttu-id="18b87-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="18b87-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="18b87-111">1 </span><span class="sxs-lookup"><span data-stu-id="18b87-111">1</span></span>  <br/> |<span data-ttu-id="18b87-112">Пролистывка по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="18b87-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="18b87-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="18b87-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="18b87-114">2 </span><span class="sxs-lookup"><span data-stu-id="18b87-114">2</span></span>  <br/> |<span data-ttu-id="18b87-115">Вертикальная пролистывка.</span><span class="sxs-lookup"><span data-stu-id="18b87-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="18b87-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="18b87-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="18b87-117">4 </span><span class="sxs-lookup"><span data-stu-id="18b87-117">4</span></span>  <br/> |<span data-ttu-id="18b87-118">Пролистывка на 90 градусов приращением от 0 до 270.</span><span class="sxs-lookup"><span data-stu-id="18b87-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="18b87-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="18b87-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="18b87-120">8 </span><span class="sxs-lookup"><span data-stu-id="18b87-120">8</span></span>  <br/> |<span data-ttu-id="18b87-121">Не пролистыый.</span><span class="sxs-lookup"><span data-stu-id="18b87-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="18b87-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="18b87-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18b87-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="18b87-123">Remarks</span></span>

<span data-ttu-id="18b87-124">Значение в ячейке ShapePlaceFlip помогает сориентировать подместимую фигуру на следующую фигуру, к ней подключено.</span><span class="sxs-lookup"><span data-stu-id="18b87-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="18b87-125">Чтобы настроить это поведение для  *всех*  фигур на странице рисования, используйте ячейку PlaceFlip в разделе "Макет страницы".</span><span class="sxs-lookup"><span data-stu-id="18b87-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="18b87-126">Чтобы получить ссылку на ячейку ShapePlaceFlip по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="18b87-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18b87-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="18b87-127">Cell name:</span></span>  <br/> |<span data-ttu-id="18b87-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="18b87-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="18b87-129">Чтобы получить ссылку на ячейку ShapePlaceFlip по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="18b87-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18b87-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="18b87-130">Section index:</span></span>  <br/> |<span data-ttu-id="18b87-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18b87-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="18b87-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="18b87-132">Row index:</span></span>  <br/> |<span data-ttu-id="18b87-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="18b87-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="18b87-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="18b87-134">Cell index:</span></span>  <br/> |<span data-ttu-id="18b87-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="18b87-135">**visSLOPlaceFlip**</span></span> <br/> |
   

