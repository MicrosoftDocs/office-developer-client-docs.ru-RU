---
title: Ячейка IsDropTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Определяет, позволяет ли группы для добавления фигуры, перетащите его в группе.
ms.openlocfilehash: 326ead15bcdc72797853daee797d8f08d459a638
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813988"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="ca5d0-103">Ячейка IsDropTarget (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="ca5d0-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="ca5d0-104">Определяет, позволяет ли группы для добавления фигуры, перетащите его в группе.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="ca5d0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ca5d0-105">**Value**</span></span>|<span data-ttu-id="ca5d0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca5d0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca5d0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca5d0-107">TRUE</span></span>  <br/> |<span data-ttu-id="ca5d0-108">Можно добавить фигуру в группу, перетащите его в группу.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="ca5d0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca5d0-109">FALSE</span></span>  <br/> |<span data-ttu-id="ca5d0-110">Не удалось удалить фигуру на группы.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca5d0-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca5d0-111">Remarks</span></span>

<span data-ttu-id="ca5d0-112">Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем выбрав флажок **Accept пропущенные фигур** .</span><span class="sxs-lookup"><span data-stu-id="ca5d0-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="ca5d0-113">Чтобы добавить фигуру в группу, перетащите его в группе, необходимо также включить схожи фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="ca5d0-114">Выделите фигуру, выберите **поведение** на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) и затем установите флажок **Добавить фигуру в группы при размещении** .</span><span class="sxs-lookup"><span data-stu-id="ca5d0-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="ca5d0-115">Это значение хранится в ячейке IsDropSource в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="ca5d0-116">Чтобы получить ссылку на ячейку IsDropTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca5d0-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca5d0-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ca5d0-117">Cell name:</span></span>  <br/> |<span data-ttu-id="ca5d0-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="ca5d0-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="ca5d0-119">Для получения ссылки на ячейки IsDropTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ca5d0-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca5d0-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ca5d0-120">Section index:</span></span>  <br/> |<span data-ttu-id="ca5d0-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca5d0-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ca5d0-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ca5d0-122">Row index:</span></span>  <br/> |<span data-ttu-id="ca5d0-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="ca5d0-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="ca5d0-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ca5d0-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ca5d0-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="ca5d0-125">**visGroupIsDropTarget**</span></span> <br/> |
   

