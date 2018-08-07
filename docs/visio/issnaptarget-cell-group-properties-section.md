---
title: Ячейка IsSnapTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Определяет, выполняется ли привязка к группе или к фигурам в группе.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814003"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="51a7e-103">Ячейка IsSnapTarget (раздел "Свойства группы")</span><span class="sxs-lookup"><span data-stu-id="51a7e-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="51a7e-104">Определяет, выполняется ли привязка к группе или к фигурам в группе.</span><span class="sxs-lookup"><span data-stu-id="51a7e-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="51a7e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="51a7e-105">**Value**</span></span>|<span data-ttu-id="51a7e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51a7e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51a7e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="51a7e-107">TRUE</span></span>  <br/> |<span data-ttu-id="51a7e-108">Включение привязки к фигурам в группе.</span><span class="sxs-lookup"><span data-stu-id="51a7e-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="51a7e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="51a7e-109">FALSE</span></span>  <br/> |<span data-ttu-id="51a7e-110">Привязка только для группы.</span><span class="sxs-lookup"><span data-stu-id="51a7e-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51a7e-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="51a7e-111">Remarks</span></span>

<span data-ttu-id="51a7e-112">Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Привязка к фигурам** .</span><span class="sxs-lookup"><span data-stu-id="51a7e-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="51a7e-113">Чтобы получить ссылку на ячейку IsSnapTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="51a7e-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51a7e-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="51a7e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="51a7e-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="51a7e-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="51a7e-116">Для получения ссылки на ячейки IsSnapTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="51a7e-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51a7e-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="51a7e-117">Section index:</span></span>  <br/> |<span data-ttu-id="51a7e-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51a7e-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="51a7e-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="51a7e-119">Row index:</span></span>  <br/> |<span data-ttu-id="51a7e-120">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="51a7e-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="51a7e-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="51a7e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="51a7e-122">**visGroupIsSnapTarget**</span><span class="sxs-lookup"><span data-stu-id="51a7e-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

