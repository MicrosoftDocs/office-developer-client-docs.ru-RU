---
title: IsSnapTarget Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Определяет, привязана ли к группе или к фигурам в группе.
ms.openlocfilehash: cae3eab64be3a91c48ae9f7fb49aa2a321087f43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421447"
---
# <a name="issnaptarget-cell-group-properties-section"></a><span data-ttu-id="55c8a-103">IsSnapTarget Cell (Group Properties Section)</span><span class="sxs-lookup"><span data-stu-id="55c8a-103">IsSnapTarget Cell (Group Properties Section)</span></span>

<span data-ttu-id="55c8a-104">Определяет, привязана ли к группе или к фигурам в группе.</span><span class="sxs-lookup"><span data-stu-id="55c8a-104">Determines whether you snap to a group or to shapes within the group.</span></span>
  
|<span data-ttu-id="55c8a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="55c8a-105">**Value**</span></span>|<span data-ttu-id="55c8a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55c8a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55c8a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="55c8a-107">TRUE</span></span>  <br/> |<span data-ttu-id="55c8a-108">РазРешите привязку к фигурам в группе.</span><span class="sxs-lookup"><span data-stu-id="55c8a-108">Enable snapping to shapes within a group.</span></span>  <br/> |
|<span data-ttu-id="55c8a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="55c8a-109">FALSE</span></span>  <br/> |<span data-ttu-id="55c8a-110">ПриКрепление только к группе.</span><span class="sxs-lookup"><span data-stu-id="55c8a-110">Snap only to the group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c8a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="55c8a-111">Remarks</span></span>

<span data-ttu-id="55c8a-112">Вы также можете задать это значение, выбрав группу, нажав кнопку **поведение** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем установив флажок **привязать к фигурам участника** .</span><span class="sxs-lookup"><span data-stu-id="55c8a-112">You can also set this value by selecting the group, clicking **Behavior** on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting the **Snap to member shapes** check box.</span></span> 
  
<span data-ttu-id="55c8a-113">Чтобы получить ссылку на ячейку IsSnapTarget по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="55c8a-113">To get a reference to the IsSnapTarget cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55c8a-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="55c8a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="55c8a-115">IsSnapTarget</span><span class="sxs-lookup"><span data-stu-id="55c8a-115">IsSnapTarget</span></span>  <br/> |
   
<span data-ttu-id="55c8a-116">Чтобы получить ссылку на ячейку IsSnapTarget по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="55c8a-116">To get a reference to the IsSnapTarget cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55c8a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="55c8a-117">Section index:</span></span>  <br/> |<span data-ttu-id="55c8a-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="55c8a-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="55c8a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="55c8a-119">Row index:</span></span>  <br/> |<span data-ttu-id="55c8a-120">**Висровграуп**</span><span class="sxs-lookup"><span data-stu-id="55c8a-120">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="55c8a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="55c8a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="55c8a-122">**Висграуписснаптаржет**</span><span class="sxs-lookup"><span data-stu-id="55c8a-122">**visGroupIsSnapTarget**</span></span> <br/> |
   

