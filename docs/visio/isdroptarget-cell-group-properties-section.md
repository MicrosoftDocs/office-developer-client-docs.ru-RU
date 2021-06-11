---
title: IsDropTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm495
localization_priority: Normal
ms.assetid: 8140fc7b-b99c-54bb-7af3-7de6fcdae7d3
description: Определяет, позволяет ли группа добавлять фигуру в нее, сбрасывая ее в группу.
ms.openlocfilehash: 50f545b3cbd4f7e1541a7f5e8ca32c34d0429c5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410793"
---
# <a name="isdroptarget-cell-group-properties-section"></a><span data-ttu-id="ca072-103">IsDropTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="ca072-103">IsDropTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="ca072-104">Определяет, позволяет ли группа добавлять фигуру в нее, сбрасывая ее в группу.</span><span class="sxs-lookup"><span data-stu-id="ca072-104">Determines whether the group allows you to add a shape to it by dropping it on the group.</span></span>
  
|<span data-ttu-id="ca072-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ca072-105">**Value**</span></span>|<span data-ttu-id="ca072-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca072-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca072-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca072-107">TRUE</span></span>  <br/> |<span data-ttu-id="ca072-108">Можно добавить фигуру в группу, сбросив ее в группу.</span><span class="sxs-lookup"><span data-stu-id="ca072-108">Can add a shape to the group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="ca072-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca072-109">FALSE</span></span>  <br/> |<span data-ttu-id="ca072-110">Не удается выбросить фигуру на группу.</span><span class="sxs-lookup"><span data-stu-id="ca072-110">Cannot drop shape onto the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca072-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca072-111">Remarks</span></span>

<span data-ttu-id="ca072-112">Вы также можете установить это значение, выбрав  группу, щелкнув "Поведение" на вкладке "Разработчик", а затем выбрав поле "Принять выброшенные [](run-in-developer-mode-display-the-developer-tab.md) **фигуры".**</span><span class="sxs-lookup"><span data-stu-id="ca072-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Accept dropped shapes** check box.</span></span> 
  
<span data-ttu-id="ca072-113">Чтобы добавить фигуру в группу, сбросив ее в группу, необходимо также включить аналогичное поведение фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca072-113">To add a shape to a group by dropping it on the group, you must also enable similar shape behavior.</span></span> <span data-ttu-id="ca072-114">Необходимо выбрать фигуру, щелкнуть **"Поведение"** на вкладке ["Разработчик",](run-in-developer-mode-display-the-developer-tab.md) а затем выбрать фигуру Добавить в группы на **табло** "Падение".</span><span class="sxs-lookup"><span data-stu-id="ca072-114">You must select the shape, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Add shape to groups on drop** check box.</span></span> <span data-ttu-id="ca072-115">Это значение хранится в ячейке IsDropSource в разделе Разное.</span><span class="sxs-lookup"><span data-stu-id="ca072-115">This value is stored in the IsDropSource cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="ca072-116">Чтобы получить ссылку на ячейку IsDropTarget по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ca072-116">To get a reference to the IsDropTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca072-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ca072-117">Cell name:</span></span>  <br/> |<span data-ttu-id="ca072-118">IsDropTarget</span><span class="sxs-lookup"><span data-stu-id="ca072-118">IsDropTarget</span></span>  <br/> |
   
<span data-ttu-id="ca072-119">Чтобы получить ссылку на ячейку IsDropTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ca072-119">To get a reference to the IsDropTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca072-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ca072-120">Section index:</span></span>  <br/> |<span data-ttu-id="ca072-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca072-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ca072-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ca072-122">Row index:</span></span>  <br/> |<span data-ttu-id="ca072-123">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="ca072-123">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="ca072-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ca072-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ca072-125">**visGroupIsDropTarget**</span><span class="sxs-lookup"><span data-stu-id="ca072-125">**visGroupIsDropTarget**</span></span> <br/> |
   

