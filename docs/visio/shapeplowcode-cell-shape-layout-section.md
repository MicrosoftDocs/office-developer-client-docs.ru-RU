---
title: Ячейка ShapePlowCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Определяет, будет ли этот размещаемой фигуры перемещает нет на месте при перетаскивании другой фигуры к ним рядом с этой фигуры на странице документа.
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814792"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="72925-103">Ячейка ShapePlowCode (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="72925-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="72925-104">Определяет, будет ли этот размещаемой фигуры перемещает нет на месте при перетаскивании другой фигуры к ним рядом с этой фигуры на странице документа.</span><span class="sxs-lookup"><span data-stu-id="72925-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="72925-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="72925-105">**Value**</span></span>|<span data-ttu-id="72925-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72925-106">**Description**</span></span>|<span data-ttu-id="72925-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="72925-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72925-108">0</span><span class="sxs-lookup"><span data-stu-id="72925-108">0</span></span>  <br/> |<span data-ttu-id="72925-109">Сдвигать, как указано для страницы.</span><span class="sxs-lookup"><span data-stu-id="72925-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="72925-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="72925-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="72925-111">1</span><span class="sxs-lookup"><span data-stu-id="72925-111">1</span></span>  <br/> |<span data-ttu-id="72925-112">Не сдвигать фигуры.</span><span class="sxs-lookup"><span data-stu-id="72925-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="72925-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="72925-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="72925-114">2</span><span class="sxs-lookup"><span data-stu-id="72925-114">2</span></span>  <br/> |<span data-ttu-id="72925-115">Сдвигать все фигуры.</span><span class="sxs-lookup"><span data-stu-id="72925-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="72925-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="72925-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72925-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="72925-117">Remarks</span></span>

<span data-ttu-id="72925-118">Также можно настроить значение ячейки для определенного фигуры на вкладку **Размещение** в диалоговом окне **поведение** (с фигурой выбрано, на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Разработки фигуры** выберите **поведение**и нажмите кнопку Вкладка **Размещение** ).</span><span class="sxs-lookup"><span data-stu-id="72925-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="72925-119">Чтобы задать это поведение для *всех* фигур на странице документа, используйте ячейку PlowCode в разделе макет страницы.</span><span class="sxs-lookup"><span data-stu-id="72925-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="72925-120">Чтобы получить ссылку на ячейку ShapePlowCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="72925-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72925-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="72925-121">Cell name:</span></span>  <br/> |<span data-ttu-id="72925-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="72925-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="72925-123">Для получения ссылки на ячейки ShapePlowCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="72925-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72925-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="72925-124">Section index:</span></span>  <br/> |<span data-ttu-id="72925-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72925-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="72925-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="72925-126">Row index:</span></span>  <br/> |<span data-ttu-id="72925-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="72925-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="72925-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="72925-128">Cell index:</span></span>  <br/> |<span data-ttu-id="72925-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="72925-129">**visSLOPlowCode**</span></span> <br/> |
   

