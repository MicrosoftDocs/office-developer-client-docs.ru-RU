---
title: DisplayMode Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Определяет, как отображаются фигура группы и ее участники.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413187"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="ce8e4-103">DisplayMode Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ce8e4-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="ce8e4-104">Определяет, как отображаются фигура группы и ее участники.</span><span class="sxs-lookup"><span data-stu-id="ce8e4-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="ce8e4-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-105">**Value**</span></span>|<span data-ttu-id="ce8e4-106">**Режим отображения**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-106">**Display Mode**</span></span>|<span data-ttu-id="ce8e4-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce8e4-108">0</span><span class="sxs-lookup"><span data-stu-id="ce8e4-108">0</span></span>  <br/> |<span data-ttu-id="ce8e4-109">Скрывает фигуру группы и текст.</span><span class="sxs-lookup"><span data-stu-id="ce8e4-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="ce8e4-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="ce8e4-111">1</span><span class="sxs-lookup"><span data-stu-id="ce8e4-111">1</span></span>  <br/> |<span data-ttu-id="ce8e4-112">Отображает форму группы за фигурами членов.</span><span class="sxs-lookup"><span data-stu-id="ce8e4-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="ce8e4-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="ce8e4-114">2</span><span class="sxs-lookup"><span data-stu-id="ce8e4-114">2</span></span>  <br/> |<span data-ttu-id="ce8e4-115">Отображает форму группы перед фигурами членов.</span><span class="sxs-lookup"><span data-stu-id="ce8e4-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="ce8e4-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce8e4-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce8e4-117">Remarks</span></span>

<span data-ttu-id="ce8e4-118">Вы также можете установить это значение, выбрав  группу, щелкнув [](run-in-developer-mode-display-the-developer-tab.md) "Поведение" группы **Shape Design** на вкладке Разработчик, а затем выбрав режим отображения из списка данных **группы.**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="ce8e4-119">Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce8e4-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-120">Cell name:</span></span>  <br/> |<span data-ttu-id="ce8e4-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="ce8e4-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="ce8e4-122">Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce8e4-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-123">Section index:</span></span>  <br/> |<span data-ttu-id="ce8e4-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ce8e4-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-125">Row index:</span></span>  <br/> |<span data-ttu-id="ce8e4-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="ce8e4-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ce8e4-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ce8e4-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="ce8e4-128">**visGroupDisplayMode**</span></span> <br/> |
   

