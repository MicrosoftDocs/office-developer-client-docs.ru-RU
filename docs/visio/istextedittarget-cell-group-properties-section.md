---
title: IsTextEditTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Определяет назначение текста для группы.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314919"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="9880d-103">IsTextEditTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9880d-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="9880d-104">Определяет назначение текста для группы.</span><span class="sxs-lookup"><span data-stu-id="9880d-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="9880d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9880d-105">**Value**</span></span>|<span data-ttu-id="9880d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9880d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9880d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9880d-107">TRUE</span></span>  <br/> |<span data-ttu-id="9880d-108">Текст добавляется в фигуру группы.</span><span class="sxs-lookup"><span data-stu-id="9880d-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="9880d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9880d-109">FALSE</span></span>  <br/> |<span data-ttu-id="9880d-110">Текст добавляется к фигуре в группе в верхней части порядка размещения.</span><span class="sxs-lookup"><span data-stu-id="9880d-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9880d-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="9880d-111">Remarks</span></span>

<span data-ttu-id="9880d-112">Вы также можете задать это значение, выбрав группу, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установив флажок **изменить текст группы** .</span><span class="sxs-lookup"><span data-stu-id="9880d-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="9880d-113">Группы, созданные в более ранних версиях, чем Visio 2000, имеют значение по умолчанию (FALSE).</span><span class="sxs-lookup"><span data-stu-id="9880d-113">Groups created in versions earlier than Visio 2000 have a default value of FALSE.</span></span> <span data-ttu-id="9880d-114">Начиная с Visio версии 2000, значение по умолчанию — TRUE.</span><span class="sxs-lookup"><span data-stu-id="9880d-114">Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="9880d-115">Чтобы получить ссылку на ячейку IsTextEditTarget по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="9880d-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9880d-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9880d-116">Cell name:</span></span>  <br/> |<span data-ttu-id="9880d-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="9880d-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="9880d-118">Чтобы получить ссылку на ячейку IsTextEditTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9880d-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9880d-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9880d-119">Section index:</span></span>  <br/> |<span data-ttu-id="9880d-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9880d-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9880d-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9880d-121">Row index:</span></span>  <br/> |<span data-ttu-id="9880d-122">**Висровграуп**</span><span class="sxs-lookup"><span data-stu-id="9880d-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="9880d-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9880d-123">Cell index:</span></span>  <br/> |<span data-ttu-id="9880d-124">**Висграупистекстедиттаржет**</span><span class="sxs-lookup"><span data-stu-id="9880d-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

