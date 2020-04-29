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
description: Определяет способ отображения фигуры группы и ее членов.
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413187"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="c3001-103">DisplayMode Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c3001-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="c3001-104">Определяет способ отображения фигуры группы и ее членов.</span><span class="sxs-lookup"><span data-stu-id="c3001-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="c3001-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c3001-105">**Value**</span></span>|<span data-ttu-id="c3001-106">**Режим отображения**</span><span class="sxs-lookup"><span data-stu-id="c3001-106">**Display Mode**</span></span>|<span data-ttu-id="c3001-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c3001-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3001-108">нуль</span><span class="sxs-lookup"><span data-stu-id="c3001-108">0</span></span>  <br/> |<span data-ttu-id="c3001-109">Скрывает фигуру группы и текст.</span><span class="sxs-lookup"><span data-stu-id="c3001-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="c3001-110">**висгрпдиспмоденоне**</span><span class="sxs-lookup"><span data-stu-id="c3001-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="c3001-111">1,1</span><span class="sxs-lookup"><span data-stu-id="c3001-111">1</span></span>  <br/> |<span data-ttu-id="c3001-112">Отображает фигуру группы позади фигур элементов.</span><span class="sxs-lookup"><span data-stu-id="c3001-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="c3001-113">**висгрпдиспмодебакк**</span><span class="sxs-lookup"><span data-stu-id="c3001-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="c3001-114">2</span><span class="sxs-lookup"><span data-stu-id="c3001-114">2</span></span>  <br/> |<span data-ttu-id="c3001-115">Отображает фигуру группы перед фигурами элементов.</span><span class="sxs-lookup"><span data-stu-id="c3001-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="c3001-116">**висгрпдиспмодефронт**</span><span class="sxs-lookup"><span data-stu-id="c3001-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3001-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3001-117">Remarks</span></span>

<span data-ttu-id="c3001-118">Это значение можно также задать, выбрав группу, щелкнув **поведение** в группе **Макет фигуры** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем выбрав режим отображения в списке **данные группы** .</span><span class="sxs-lookup"><span data-stu-id="c3001-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="c3001-119">Чтобы получить ссылку на ячейку DisplayMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c3001-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3001-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c3001-120">Cell name:</span></span>  <br/> |<span data-ttu-id="c3001-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="c3001-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="c3001-122">Чтобы получить ссылку на ячейку DisplayMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c3001-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3001-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c3001-123">Section index:</span></span>  <br/> |<span data-ttu-id="c3001-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c3001-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c3001-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c3001-125">Row index:</span></span>  <br/> |<span data-ttu-id="c3001-126">**висровграуп**</span><span class="sxs-lookup"><span data-stu-id="c3001-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="c3001-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c3001-127">Cell index:</span></span>  <br/> |<span data-ttu-id="c3001-128">**висграупдисплаймоде**</span><span class="sxs-lookup"><span data-stu-id="c3001-128">**visGroupDisplayMode**</span></span> <br/> |
   

