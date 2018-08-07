---
title: Ячейка ShapePlaceFlip (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Определяет, как зеркальное отражение размещаемой фигуры, поворот, или оба на странице при размещении фигур с помощью диалоговое окно Настройка макета (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814779"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a><span data-ttu-id="5bd84-103">Ячейка ShapePlaceFlip (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="5bd84-103">ShapePlaceFlip Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5bd84-104">Определяет, как зеркальное отражение размещаемой фигуры, поворот, или оба на странице при размещении фигур с помощью диалоговое окно **Настройка макета** (на вкладке **Конструктор** в группе **Макет** выберите пункт **Изменить расположение**и нажмите кнопку **более Параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="5bd84-104">Determines how a placeable shape flips, rotates, or both on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="5bd84-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5bd84-105">**Value**</span></span>|<span data-ttu-id="5bd84-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5bd84-106">**Description**</span></span>|<span data-ttu-id="5bd84-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="5bd84-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bd84-108">0</span><span class="sxs-lookup"><span data-stu-id="5bd84-108">0</span></span>  <br/> |<span data-ttu-id="5bd84-109">Использование страницы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5bd84-109">Use page default.</span></span>  <br/> |<span data-ttu-id="5bd84-110">**visLOFlipDefault**</span><span class="sxs-lookup"><span data-stu-id="5bd84-110">**visLOFlipDefault**</span></span> <br/> |
|<span data-ttu-id="5bd84-111">1</span><span class="sxs-lookup"><span data-stu-id="5bd84-111">1</span></span>  <br/> |<span data-ttu-id="5bd84-112">Слева направо.</span><span class="sxs-lookup"><span data-stu-id="5bd84-112">Flip horizontal.</span></span>  <br/> |<span data-ttu-id="5bd84-113">**visLOFlipX**</span><span class="sxs-lookup"><span data-stu-id="5bd84-113">**visLOFlipX**</span></span> <br/> |
|<span data-ttu-id="5bd84-114">2</span><span class="sxs-lookup"><span data-stu-id="5bd84-114">2</span></span>  <br/> |<span data-ttu-id="5bd84-115">Отразить сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="5bd84-115">Flip vertical.</span></span>  <br/> |<span data-ttu-id="5bd84-116">**visLOFlipY**</span><span class="sxs-lookup"><span data-stu-id="5bd84-116">**visLOFlipY**</span></span> <br/> |
|<span data-ttu-id="5bd84-117">4</span><span class="sxs-lookup"><span data-stu-id="5bd84-117">4</span></span>  <br/> |<span data-ttu-id="5bd84-118">Отразить на 90 градусов между 0 и на 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="5bd84-118">Flip in 90 degree increments between 0 and 270.</span></span>  <br/> |<span data-ttu-id="5bd84-119">**visLOFlipRotate**</span><span class="sxs-lookup"><span data-stu-id="5bd84-119">**visLOFlipRotate**</span></span> <br/> |
|<span data-ttu-id="5bd84-120">8</span><span class="sxs-lookup"><span data-stu-id="5bd84-120">8</span></span>  <br/> |<span data-ttu-id="5bd84-121">Не отражение.</span><span class="sxs-lookup"><span data-stu-id="5bd84-121">Do not flip.</span></span>  <br/> |<span data-ttu-id="5bd84-122">**visLOFlipNone**</span><span class="sxs-lookup"><span data-stu-id="5bd84-122">**visLOFlipNone**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bd84-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bd84-123">Remarks</span></span>

<span data-ttu-id="5bd84-124">Значение в ячейке ShapePlaceFlip поможет сориентироваться размещаемой фигуры к следующей размещаемой фигуры, которым подключаются к.</span><span class="sxs-lookup"><span data-stu-id="5bd84-124">The value in the ShapePlaceFlip cell helps orient a placeable shape toward the next placeable shape it is connected to.</span></span>
  
<span data-ttu-id="5bd84-125">Чтобы задать это поведение для *всех* фигур на странице документа, используйте ячейку PlaceFlip в разделе макет страницы.</span><span class="sxs-lookup"><span data-stu-id="5bd84-125">To set this behavior for  *all*  the shapes on the drawing page, use the PlaceFlip cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="5bd84-126">Чтобы получить ссылку на ячейку ShapePlaceFlip по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5bd84-126">To get a reference to the ShapePlaceFlip cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bd84-127">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5bd84-127">Cell name:</span></span>  <br/> |<span data-ttu-id="5bd84-128">ShapePlaceFlip</span><span class="sxs-lookup"><span data-stu-id="5bd84-128">ShapePlaceFlip</span></span>  <br/> |
   
<span data-ttu-id="5bd84-129">Для получения ссылки на ячейки ShapePlaceFlip по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5bd84-129">To get a reference to the ShapePlaceFlip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bd84-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5bd84-130">Section index:</span></span>  <br/> |<span data-ttu-id="5bd84-131">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5bd84-131">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5bd84-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5bd84-132">Row index:</span></span>  <br/> |<span data-ttu-id="5bd84-133">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="5bd84-133">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="5bd84-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5bd84-134">Cell index:</span></span>  <br/> |<span data-ttu-id="5bd84-135">**visSLOPlaceFlip**</span><span class="sxs-lookup"><span data-stu-id="5bd84-135">**visSLOPlaceFlip**</span></span> <br/> |
   

