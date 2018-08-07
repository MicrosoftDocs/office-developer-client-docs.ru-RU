---
title: Ячейка SelectMode (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Определяет способ выбора групповой фигуры и ее компонентов.
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814740"
---
# <a name="selectmode-cell-group-properties-section"></a><span data-ttu-id="e6ec5-103">Ячейка SelectMode (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="e6ec5-103">SelectMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="e6ec5-104">Определяет способ выбора групповой фигуры и ее компонентов.</span><span class="sxs-lookup"><span data-stu-id="e6ec5-104">Determines how you select a group shape and its members.</span></span>
  
|<span data-ttu-id="e6ec5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-105">**Value**</span></span>|<span data-ttu-id="e6ec5-106">**Выбор режима**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-106">**Selection mode**</span></span>|<span data-ttu-id="e6ec5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6ec5-108">0</span><span class="sxs-lookup"><span data-stu-id="e6ec5-108">0</span></span>  <br/> |<span data-ttu-id="e6ec5-109">Выберите только групповой фигуры.</span><span class="sxs-lookup"><span data-stu-id="e6ec5-109">Select the group shape only.</span></span>  <br/> |<span data-ttu-id="e6ec5-110">**visGrpSelModeGroupOnly**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-110">**visGrpSelModeGroupOnly**</span></span> <br/> |
|<span data-ttu-id="e6ec5-111">1</span><span class="sxs-lookup"><span data-stu-id="e6ec5-111">1</span></span>  <br/> |<span data-ttu-id="e6ec5-112">Сначала выберите групповой фигуры.</span><span class="sxs-lookup"><span data-stu-id="e6ec5-112">Select the group shape first.</span></span>  <br/> |<span data-ttu-id="e6ec5-113">**visGrpSelModeGroup1st**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-113">**visGrpSelModeGroup1st**</span></span> <br/> |
|<span data-ttu-id="e6ec5-114">2</span><span class="sxs-lookup"><span data-stu-id="e6ec5-114">2</span></span>  <br/> |<span data-ttu-id="e6ec5-115">Выберите членов группы.</span><span class="sxs-lookup"><span data-stu-id="e6ec5-115">Select the members of the group first.</span></span>  <br/> |<span data-ttu-id="e6ec5-116">**visGrpSelModeMembers1st**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-116">**visGrpSelModeMembers1st**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6ec5-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6ec5-117">Remarks</span></span>

<span data-ttu-id="e6ec5-118">В диалоговом окне " **поведение** " можно задать это значение (с групповой фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** щелкните **поведение**и нажмите кнопку режим в **списке в разделе **группы Поведение**** ).</span><span class="sxs-lookup"><span data-stu-id="e6ec5-118">You can also set this value in the **Behavior** dialog box (with the group shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click a mode in the **Selection** list under **Group Behavior** ).</span></span> 
  
<span data-ttu-id="e6ec5-119">Чтобы получить ссылку на ячейку SelectMode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e6ec5-119">To get a reference to the SelectMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6ec5-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e6ec5-120">Cell name:</span></span>  <br/> |<span data-ttu-id="e6ec5-121">SelectMode</span><span class="sxs-lookup"><span data-stu-id="e6ec5-121">SelectMode</span></span>  <br/> |
   
<span data-ttu-id="e6ec5-122">Для получения ссылки на ячейки SelectMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e6ec5-122">To get a reference to the SelectMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6ec5-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e6ec5-123">Section index:</span></span>  <br/> |<span data-ttu-id="e6ec5-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e6ec5-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e6ec5-125">Row index:</span></span>  <br/> |<span data-ttu-id="e6ec5-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="e6ec5-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e6ec5-127">Cell index:</span></span>  <br/> |<span data-ttu-id="e6ec5-128">**visGroupSelectMode**</span><span class="sxs-lookup"><span data-stu-id="e6ec5-128">**visGroupSelectMode**</span></span> <br/> |
   

