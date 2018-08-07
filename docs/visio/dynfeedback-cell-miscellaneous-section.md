---
title: Ячейка DynFeedback (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Изменяет тип визуальной обратной связи, предоставляемых пользователям при перетаскивании соединительной линии. При отпускании кнопки мыши, этот параметр не повлияет получившуюся форму соединительной линии. Этот параметр не применяется к маршрутизируемые соединители.
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813675"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="81e3a-105">Ячейка DynFeedback (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="81e3a-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="81e3a-106">Изменяет тип визуальной обратной связи, предоставляемых пользователям при перетаскивании соединительной линии.</span><span class="sxs-lookup"><span data-stu-id="81e3a-106">Changes the type of visual feedback provided to users when they drag a connector.</span></span> <span data-ttu-id="81e3a-107">При отпускании кнопки мыши, этот параметр не повлияет получившуюся форму соединительной линии.</span><span class="sxs-lookup"><span data-stu-id="81e3a-107">When the mouse button is released, the resulting connector shape is not affected by this setting.</span></span> <span data-ttu-id="81e3a-108">Этот параметр не применяется к маршрутизируемые соединители.</span><span class="sxs-lookup"><span data-stu-id="81e3a-108">This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="81e3a-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="81e3a-109">**Value**</span></span>|<span data-ttu-id="81e3a-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81e3a-110">**Description**</span></span>|<span data-ttu-id="81e3a-111">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="81e3a-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="81e3a-112">0</span><span class="sxs-lookup"><span data-stu-id="81e3a-112">0</span></span>  <br/> | <span data-ttu-id="81e3a-113">Остается с текущими настройками прямых (не конечностей).</span><span class="sxs-lookup"><span data-stu-id="81e3a-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="81e3a-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="81e3a-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="81e3a-115">1</span><span class="sxs-lookup"><span data-stu-id="81e3a-115">1</span></span>  <br/> | <span data-ttu-id="81e3a-116">Отображает три конечностей при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="81e3a-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="81e3a-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="81e3a-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="81e3a-118">2</span><span class="sxs-lookup"><span data-stu-id="81e3a-118">2</span></span>  <br/> | <span data-ttu-id="81e3a-119">Показывает пять конечностей при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="81e3a-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="81e3a-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="81e3a-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81e3a-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="81e3a-121">Remarks</span></span>

<span data-ttu-id="81e3a-122">Чтобы получить ссылку на ячейку DynFeedback по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="81e3a-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81e3a-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="81e3a-123">Cell name:</span></span>  <br/> | <span data-ttu-id="81e3a-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="81e3a-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="81e3a-125">Для получения ссылки на ячейки DynFeedback по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="81e3a-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81e3a-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81e3a-126">Section index:</span></span>  <br/> |<span data-ttu-id="81e3a-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81e3a-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81e3a-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81e3a-128">Row index:</span></span>  <br/> |<span data-ttu-id="81e3a-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="81e3a-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="81e3a-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81e3a-130">Cell index:</span></span>  <br/> |<span data-ttu-id="81e3a-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="81e3a-131">**visDynFeedback**</span></span> <br/> |
   

