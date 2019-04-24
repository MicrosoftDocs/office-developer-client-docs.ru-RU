---
title: ResizeMode Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Показывает текущий параметр поведения изменения размера для фигуры.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326882"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="54b14-103">ResizeMode Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="54b14-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="54b14-104">Показывает текущий параметр поведения изменения размера для фигуры.</span><span class="sxs-lookup"><span data-stu-id="54b14-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="54b14-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="54b14-105">**Value**</span></span>|<span data-ttu-id="54b14-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="54b14-106">**Description**</span></span>|<span data-ttu-id="54b14-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="54b14-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54b14-108">нуль</span><span class="sxs-lookup"><span data-stu-id="54b14-108">0</span></span>  <br/> |<span data-ttu-id="54b14-109">Используйте параметр группы.</span><span class="sxs-lookup"><span data-stu-id="54b14-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="54b14-110">**Висксформресизедонткаре**</span><span class="sxs-lookup"><span data-stu-id="54b14-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="54b14-111">1,1</span><span class="sxs-lookup"><span data-stu-id="54b14-111">1</span></span>  <br/> |<span data-ttu-id="54b14-112">Только перестановка.</span><span class="sxs-lookup"><span data-stu-id="54b14-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="54b14-113">**Висксформресизеспреад**</span><span class="sxs-lookup"><span data-stu-id="54b14-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="54b14-114">2</span><span class="sxs-lookup"><span data-stu-id="54b14-114">2</span></span>  <br/> |<span data-ttu-id="54b14-115">Масштабирование с помощью Group.</span><span class="sxs-lookup"><span data-stu-id="54b14-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="54b14-116">**Висксформресизескале**</span><span class="sxs-lookup"><span data-stu-id="54b14-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54b14-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="54b14-117">Remarks</span></span>

<span data-ttu-id="54b14-118">Вы также можете задать это значение на вкладке **поведение** в диалоговом окне **поведение** (на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md)в группе **Макет фигуры** щелкните **поведение**).</span><span class="sxs-lookup"><span data-stu-id="54b14-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="54b14-119">Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="54b14-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54b14-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="54b14-120">Cell name:</span></span>  <br/> |<span data-ttu-id="54b14-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="54b14-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="54b14-122">Чтобы получить ссылку на ячейку ResizeMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="54b14-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54b14-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="54b14-123">Section index:</span></span>  <br/> |<span data-ttu-id="54b14-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54b14-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="54b14-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="54b14-125">Row index:</span></span>  <br/> |<span data-ttu-id="54b14-126">**Висровксформаут**</span><span class="sxs-lookup"><span data-stu-id="54b14-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="54b14-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="54b14-127">Cell index:</span></span>  <br/> |<span data-ttu-id="54b14-128">**Висксформресиземоде**</span><span class="sxs-lookup"><span data-stu-id="54b14-128">**visXFormResizeMode**</span></span> <br/> |
   

