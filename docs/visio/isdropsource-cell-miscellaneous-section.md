---
title: IsDropSource Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: Определяет, можно ли добавить фигуру в группу, перетащив ее в группу.
ms.openlocfilehash: e8cb02a66f745530f12c7c8be56b9bdd771121b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360174"
---
# <a name="isdropsource-cell-miscellaneous-section"></a><span data-ttu-id="fd6da-103">IsDropSource Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="fd6da-103">IsDropSource Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fd6da-104">Определяет, можно ли добавить фигуру в группу, перетащив ее в группу.</span><span class="sxs-lookup"><span data-stu-id="fd6da-104">Determines whether the shape can be added to a group by dropping it onto the group.</span></span>
  
|<span data-ttu-id="fd6da-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="fd6da-105">**Value**</span></span>|<span data-ttu-id="fd6da-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fd6da-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd6da-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fd6da-107">TRUE</span></span>  <br/> |<span data-ttu-id="fd6da-108">Можно добавить фигуру в группу, перетащив ее в группу.</span><span class="sxs-lookup"><span data-stu-id="fd6da-108">Can add the shape to a group by dropping it onto the group.</span></span>  <br/> |
|<span data-ttu-id="fd6da-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd6da-109">FALSE</span></span>  <br/> |<span data-ttu-id="fd6da-110">Не удается добавить фигуру в группу.</span><span class="sxs-lookup"><span data-stu-id="fd6da-110">Cannot add the shape to a group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd6da-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd6da-111">Remarks</span></span>

<span data-ttu-id="fd6da-112">Вы также можете задать это значение, выбрав фигуру, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установив флажок **Добавить фигуру в группы при удалении** .</span><span class="sxs-lookup"><span data-stu-id="fd6da-112">You can also set this value by selecting the shape, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Add shape to groups on drop** check box.</span></span> 
  
<span data-ttu-id="fd6da-113">Кроме того, чтобы включить такое поведение для фигуры, необходимо также включить для группы возможность принимать фигуры, перетаскиваемые в нее.</span><span class="sxs-lookup"><span data-stu-id="fd6da-113">In addition to enabling this behavior for a shape, you must also enable a group to accept shapes that are dragged into it.</span></span> <span data-ttu-id="fd6da-114">Для этого выберите группу, нажмите кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установите флажок **принять пропущенные фигуры** .</span><span class="sxs-lookup"><span data-stu-id="fd6da-114">To do so, select the group, click **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then select the **Accept dropped shapes** check box.</span></span> <span data-ttu-id="fd6da-115">Это значение хранится в ячейке IsDropTarget в разделе Свойства группы.</span><span class="sxs-lookup"><span data-stu-id="fd6da-115">This value is stored in the IsDropTarget cell in the Group Properties section.</span></span> 
  
<span data-ttu-id="fd6da-116">Чтобы получить ссылку на ячейку IsDropSource по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fd6da-116">To get a reference to the IsDropSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd6da-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd6da-117">Cell name:</span></span>  <br/> |<span data-ttu-id="fd6da-118">IsDropSource</span><span class="sxs-lookup"><span data-stu-id="fd6da-118">IsDropSource</span></span>  <br/> |
   
<span data-ttu-id="fd6da-119">Чтобы получить ссылку на ячейку IsDropSource по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fd6da-119">To get a reference to the IsDropSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd6da-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fd6da-120">Section index:</span></span>  <br/> |<span data-ttu-id="fd6da-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd6da-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fd6da-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fd6da-122">Row index:</span></span>  <br/> |<span data-ttu-id="fd6da-123">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="fd6da-123">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="fd6da-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd6da-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fd6da-125">**Висдропсаурце**</span><span class="sxs-lookup"><span data-stu-id="fd6da-125">**visDropSource**</span></span> <br/> |
   

