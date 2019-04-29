---
title: DynFeedback Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Изменяет тип визуальной обратной связи, предоставляемой пользователям при перетаскивании соединителя. При отпускании кнопки мыши этот параметр не влияет на получившуюся фигуру соединителя. Этот параметр не применяется к соединителям маршрутизации.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404801"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="ebf9d-105">DynFeedback Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="ebf9d-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ebf9d-106">Изменяет тип визуальной обратной связи, предоставляемой пользователям при перетаскивании соединителя.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-106">Changes the type of visual feedback provided to users when they drag a connector.</span></span> <span data-ttu-id="ebf9d-107">При отпускании кнопки мыши этот параметр не влияет на получившуюся фигуру соединителя.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-107">When the mouse button is released, the resulting connector shape is not affected by this setting.</span></span> <span data-ttu-id="ebf9d-108">Этот параметр не применяется к соединителям маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-108">This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="ebf9d-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-109">**Value**</span></span>|<span data-ttu-id="ebf9d-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-110">**Description**</span></span>|<span data-ttu-id="ebf9d-111">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ebf9d-112">нуль</span><span class="sxs-lookup"><span data-stu-id="ebf9d-112">0</span></span>  <br/> | <span data-ttu-id="ebf9d-113">Остается без отрезков.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="ebf9d-114">**Висдинфбдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="ebf9d-115">1,1</span><span class="sxs-lookup"><span data-stu-id="ebf9d-115">1</span></span>  <br/> | <span data-ttu-id="ebf9d-116">Показывает три отрезков при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="ebf9d-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="ebf9d-118">2</span><span class="sxs-lookup"><span data-stu-id="ebf9d-118">2</span></span>  <br/> | <span data-ttu-id="ebf9d-119">Показывает пять конечностей при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="ebf9d-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebf9d-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebf9d-121">Remarks</span></span>

<span data-ttu-id="ebf9d-122">Чтобы получить ссылку на ячейку DynFeedback по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebf9d-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-123">Cell name:</span></span>  <br/> | <span data-ttu-id="ebf9d-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="ebf9d-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="ebf9d-125">Чтобы получить ссылку на ячейку DynFeedback по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebf9d-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-126">Section index:</span></span>  <br/> |<span data-ttu-id="ebf9d-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ebf9d-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-128">Row index:</span></span>  <br/> |<span data-ttu-id="ebf9d-129">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ebf9d-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ebf9d-131">**Висдинфидбакк**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-131">**visDynFeedback**</span></span> <br/> |
   

