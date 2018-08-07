---
title: Ячейка IsTextEditTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Определяет назначение текста для группы.
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814016"
---
# <a name="istextedittarget-cell-group-properties-section"></a><span data-ttu-id="cf5a1-103">Ячейка IsTextEditTarget (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="cf5a1-103">IsTextEditTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="cf5a1-104">Определяет назначение текста для группы.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-104">Determines text assignment for a group.</span></span>
  
|<span data-ttu-id="cf5a1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-105">**Value**</span></span>|<span data-ttu-id="cf5a1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf5a1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf5a1-107">TRUE</span></span>  <br/> |<span data-ttu-id="cf5a1-108">Текст добавляется в группы фигур.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-108">Text is added to the group shape.</span></span>  <br/> |
|<span data-ttu-id="cf5a1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf5a1-109">FALSE</span></span>  <br/> |<span data-ttu-id="cf5a1-110">Текст добавляется фигура в группе в верхней части порядок размещения.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-110">Text is added to the shape in the group at the top of the stacking order.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf5a1-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf5a1-111">Remarks</span></span>

<span data-ttu-id="cf5a1-112">Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Изменить текст группы** .</span><span class="sxs-lookup"><span data-stu-id="cf5a1-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Edit text of group** check box.</span></span> 
  
<span data-ttu-id="cf5a1-113">Группы, созданные в версиях, более ранних чем Visio 2000 имеют значение по умолчанию FALSE.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-113">Groups created in versions earlier than Visio 2000 have a default value of FALSE.</span></span> <span data-ttu-id="cf5a1-114">Приступая к работе с Visio версии 2000, значение по умолчанию — TRUE.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-114">Beginning with Visio version 2000, the default value is TRUE.</span></span> 
  
<span data-ttu-id="cf5a1-115">Чтобы получить ссылку на ячейку IsTextEditTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-115">To get a reference to the IsTextEditTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf5a1-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cf5a1-116">Cell name:</span></span>  <br/> |<span data-ttu-id="cf5a1-117">IsTextEditTarget</span><span class="sxs-lookup"><span data-stu-id="cf5a1-117">IsTextEditTarget</span></span>  <br/> |
   
<span data-ttu-id="cf5a1-118">Для получения ссылки на ячейки IsTextEditTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-118">To get a reference to the IsTextEditTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf5a1-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-119">Section index:</span></span>  <br/> |<span data-ttu-id="cf5a1-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cf5a1-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-121">Row index:</span></span>  <br/> |<span data-ttu-id="cf5a1-122">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-122">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="cf5a1-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cf5a1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="cf5a1-124">**visGroupIsTextEditTarget**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-124">**visGroupIsTextEditTarget**</span></span> <br/> |
   

