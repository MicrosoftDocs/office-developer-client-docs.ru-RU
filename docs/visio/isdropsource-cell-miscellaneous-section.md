---
title: Ячейка IsDropSource (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Определяет, будет ли фигуры можно добавить в группу, перетащите его в группу.
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813978"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="9dbe5-103">Ячейка IsDropSource (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="9dbe5-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9dbe5-104">Определяет, будет ли фигуры можно добавить в группу, перетащите его в группу.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="9dbe5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9dbe5-105">**Value**</span></span>|<span data-ttu-id="9dbe5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9dbe5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9dbe5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9dbe5-107">TRUE</span></span>  <br/> |<span data-ttu-id="9dbe5-108">Можно добавить фигуру в группу, перетащите его в группу.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="9dbe5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9dbe5-109">FALSE</span></span>  <br/> |<span data-ttu-id="9dbe5-110">Не удается добавить фигуру в группу.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9dbe5-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="9dbe5-111">Remarks</span></span>

<span data-ttu-id="9dbe5-112">Также можно задать это значение, выбрав фигуры, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Добавить фигуру в группы при размещении** .</span><span class="sxs-lookup"><span data-stu-id="9dbe5-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="9dbe5-113">Дополнение к разрешению это поведение для фигуры, необходимо также включить группу, чтобы принять фигур, перетащенных в нее.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="9dbe5-114">Для этого выберите группу, щелкните **поведение** на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) и установите флажок **Accept добавленной фигур** .</span><span class="sxs-lookup"><span data-stu-id="9dbe5-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="9dbe5-115">Это значение хранится в ячейке IsDropTarget в разделе Свойства группы.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="9dbe5-116">Чтобы получить ссылку на ячейку IsDropSource по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9dbe5-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9dbe5-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9dbe5-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9dbe5-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="9dbe5-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="9dbe5-119">Для получения ссылки на ячейки IsDropSource по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9dbe5-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9dbe5-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9dbe5-120">Section index:</span></span>  <br/> |<span data-ttu-id="9dbe5-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9dbe5-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9dbe5-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9dbe5-122">Row index:</span></span>  <br/> |<span data-ttu-id="9dbe5-123">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9dbe5-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="9dbe5-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9dbe5-124">Cell index:</span></span>  <br/> |<span data-ttu-id="9dbe5-125">**visDropSource**</span><span class="sxs-lookup"><span data-stu-id="9dbe5-125">**visDropSource**</span></span> <br/> |
   

