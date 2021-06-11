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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432648"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="98ed5-103">IsTextEditTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="98ed5-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="98ed5-104">Определяет назначение текста для группы.</span><span class="sxs-lookup"><span data-stu-id="98ed5-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="98ed5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="98ed5-105">**Value**</span></span>|<span data-ttu-id="98ed5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98ed5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98ed5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="98ed5-107">TRUE</span></span>  <br/> |<span data-ttu-id="98ed5-108">Текст добавляется в групповую форму.</span><span class="sxs-lookup"><span data-stu-id="98ed5-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="98ed5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="98ed5-109">FALSE</span></span>  <br/> |<span data-ttu-id="98ed5-110">Текст добавляется к фигуре в группе в верхней части порядка укладки.</span><span class="sxs-lookup"><span data-stu-id="98ed5-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98ed5-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="98ed5-111">Remarks</span></span>

<span data-ttu-id="98ed5-112">Вы также можете установить это значение, выбрав  группу, щелкнув "Поведение" на вкладке Разработчик, а затем выбрав текст редактирования **группового** контрольного окна. [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="98ed5-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="98ed5-113">Группы, созданные в версиях Visio 2000 года, имеют значение FALSE по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98ed5-113">Groups created in versions earlier than Visio 2000 have a default value of FALSE.</span></span> <span data-ttu-id="98ed5-114">Начиная с Visio версии 2000 по умолчанию значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="98ed5-114">Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="98ed5-115">Чтобы получить ссылку на ячейку IsTextEditTarget по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="98ed5-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98ed5-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="98ed5-116">Cell name:</span></span>  <br/> |<span data-ttu-id="98ed5-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="98ed5-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="98ed5-118">Чтобы получить ссылку на ячейку IsTextEditTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="98ed5-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98ed5-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="98ed5-119">Section index:</span></span>  <br/> |<span data-ttu-id="98ed5-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="98ed5-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="98ed5-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="98ed5-121">Row index:</span></span>  <br/> |<span data-ttu-id="98ed5-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="98ed5-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="98ed5-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="98ed5-123">Cell index:</span></span>  <br/> |<span data-ttu-id="98ed5-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="98ed5-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

