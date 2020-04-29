---
title: SelectMode Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Определяет способ выбора групповой фигуры и ее членов.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435364"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="ad888-103">SelectMode Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ad888-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="ad888-104">Определяет способ выбора групповой фигуры и ее членов.</span><span class="sxs-lookup"><span data-stu-id="ad888-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="ad888-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ad888-105">**Value**</span></span>|<span data-ttu-id="ad888-106">**Режим выбора**</span><span class="sxs-lookup"><span data-stu-id="ad888-106">**Selection mode**</span></span>|<span data-ttu-id="ad888-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ad888-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad888-108">нуль</span><span class="sxs-lookup"><span data-stu-id="ad888-108">0</span></span>  <br/> |<span data-ttu-id="ad888-109">Выберите только фигуру группы.</span><span class="sxs-lookup"><span data-stu-id="ad888-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="ad888-110">**висгрпселмодеграупонли**</span><span class="sxs-lookup"><span data-stu-id="ad888-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="ad888-111">1,1</span><span class="sxs-lookup"><span data-stu-id="ad888-111">1</span></span>  <br/> |<span data-ttu-id="ad888-112">Сначала выберите фигуру Group (группа).</span><span class="sxs-lookup"><span data-stu-id="ad888-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="ad888-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="ad888-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="ad888-114">2</span><span class="sxs-lookup"><span data-stu-id="ad888-114">2</span></span>  <br/> |<span data-ttu-id="ad888-115">Сначала выберите участников группы.</span><span class="sxs-lookup"><span data-stu-id="ad888-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="ad888-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="ad888-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad888-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad888-117">Remarks</span></span>

<span data-ttu-id="ad888-118">Вы также можете задать это значение в диалоговом окне **поведение** (если выбрана фигура группы, на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , в группе **Макет фигуры** щелкните **поведение**, а затем выберите режим в списке **Выбор** раздела **поведение группы** ).</span><span class="sxs-lookup"><span data-stu-id="ad888-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="ad888-119">Чтобы получить ссылку на ячейку SelectMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ad888-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad888-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ad888-120">Cell name:</span></span>  <br/> |<span data-ttu-id="ad888-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="ad888-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="ad888-122">Чтобы получить ссылку на ячейку SelectMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ad888-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad888-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ad888-123">Section index:</span></span>  <br/> |<span data-ttu-id="ad888-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad888-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ad888-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ad888-125">Row index:</span></span>  <br/> |<span data-ttu-id="ad888-126">**висровграуп**</span><span class="sxs-lookup"><span data-stu-id="ad888-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="ad888-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ad888-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ad888-128">**висграупселектмоде**</span><span class="sxs-lookup"><span data-stu-id="ad888-128">**visGroupSelectMode**</span></span> <br/> |
   

