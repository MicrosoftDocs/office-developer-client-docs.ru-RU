---
title: Ячейка DisplayMode (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Определяет способ отображения групповой фигуры и ее компонентов.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813608"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="54d99-103">Ячейка DisplayMode (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="54d99-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="54d99-104">Определяет способ отображения групповой фигуры и ее компонентов.</span><span class="sxs-lookup"><span data-stu-id="54d99-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="54d99-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="54d99-105">**Value**</span></span>|<span data-ttu-id="54d99-106">**Режим отображения**</span><span class="sxs-lookup"><span data-stu-id="54d99-106">**Display Mode**</span></span>|<span data-ttu-id="54d99-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="54d99-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54d99-108">0</span><span class="sxs-lookup"><span data-stu-id="54d99-108">0</span></span>  <br/> |<span data-ttu-id="54d99-109">Скрывает групповой фигуры и текст.</span><span class="sxs-lookup"><span data-stu-id="54d99-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="54d99-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="54d99-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="54d99-111">1</span><span class="sxs-lookup"><span data-stu-id="54d99-111">1</span></span>  <br/> |<span data-ttu-id="54d99-112">Отображает групповой фигуры за фигурами.</span><span class="sxs-lookup"><span data-stu-id="54d99-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="54d99-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="54d99-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="54d99-114">2</span><span class="sxs-lookup"><span data-stu-id="54d99-114">2</span></span>  <br/> |<span data-ttu-id="54d99-115">Отображает групповой фигуры перед фигурами.</span><span class="sxs-lookup"><span data-stu-id="54d99-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="54d99-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="54d99-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54d99-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="54d99-117">Remarks</span></span>

<span data-ttu-id="54d99-118">Также задается это значение выбора группы, щелкнув **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) ", а затем выбрав режим отображения в списке **группы данных** .</span><span class="sxs-lookup"><span data-stu-id="54d99-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="54d99-119">Для получения ссылки на ячейки DisplayMode по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="54d99-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54d99-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="54d99-120">Cell name:</span></span>  <br/> |<span data-ttu-id="54d99-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="54d99-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="54d99-122">Для получения ссылки на ячейки DisplayMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="54d99-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54d99-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="54d99-123">Section index:</span></span>  <br/> |<span data-ttu-id="54d99-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54d99-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="54d99-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="54d99-125">Row index:</span></span>  <br/> |<span data-ttu-id="54d99-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="54d99-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="54d99-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="54d99-127">Cell index:</span></span>  <br/> |<span data-ttu-id="54d99-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="54d99-128">**visGroupDisplayMode**</span></span> <br/> |
   

