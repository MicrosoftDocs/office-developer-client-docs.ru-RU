---
title: LineJumpCode Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Определяет соединители, к которым нужно добавить переходы.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416253"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="84e42-103">LineJumpCode Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="84e42-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="84e42-104">Определяет соединители, к которым нужно добавить переходы.</span><span class="sxs-lookup"><span data-stu-id="84e42-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="84e42-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="84e42-105">**Value**</span></span>|<span data-ttu-id="84e42-106">**Соединители, к которым нужно добавить переходы**</span><span class="sxs-lookup"><span data-stu-id="84e42-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="84e42-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="84e42-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84e42-108">0</span><span class="sxs-lookup"><span data-stu-id="84e42-108">0</span></span>  <br/> |<span data-ttu-id="84e42-109">Нет</span><span class="sxs-lookup"><span data-stu-id="84e42-109">None</span></span>  <br/> |<span data-ttu-id="84e42-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="84e42-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="84e42-111">1 </span><span class="sxs-lookup"><span data-stu-id="84e42-111">1</span></span>  <br/> |<span data-ttu-id="84e42-112">Горизонтальные линии</span><span class="sxs-lookup"><span data-stu-id="84e42-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="84e42-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="84e42-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="84e42-114">2 </span><span class="sxs-lookup"><span data-stu-id="84e42-114">2</span></span>  <br/> |<span data-ttu-id="84e42-115">Вертикальные линии</span><span class="sxs-lookup"><span data-stu-id="84e42-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="84e42-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="84e42-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="84e42-117">3 </span><span class="sxs-lookup"><span data-stu-id="84e42-117">3</span></span>  <br/> |<span data-ttu-id="84e42-118">Последняя маршрутивная линия</span><span class="sxs-lookup"><span data-stu-id="84e42-118">Last routed line</span></span>  <br/> |<span data-ttu-id="84e42-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="84e42-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="84e42-120">4 </span><span class="sxs-lookup"><span data-stu-id="84e42-120">4</span></span>  <br/> |<span data-ttu-id="84e42-121">Последняя отображаемая линия  (верхняя фигура в z-порядке)</span><span class="sxs-lookup"><span data-stu-id="84e42-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="84e42-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="84e42-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="84e42-123">5 </span><span class="sxs-lookup"><span data-stu-id="84e42-123">5</span></span>  <br/> |<span data-ttu-id="84e42-124">Первая отображаемая строка (фигура в нижней части *Z-порядка)*</span><span class="sxs-lookup"><span data-stu-id="84e42-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="84e42-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="84e42-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84e42-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="84e42-126">Remarks</span></span>

<span data-ttu-id="84e42-127">Вы также можете установить значение этой  ячейки на вкладке "Макет и маршрут"  в диалоговом окне "Настройка страницы" (на вкладке "Конструктор", щелкните стрелку "Настройка страницы", а затем щелкните "Макет и **маршрут").**  </span><span class="sxs-lookup"><span data-stu-id="84e42-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="84e42-128">Чтобы получить ссылку на ячейку LineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="84e42-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84e42-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="84e42-129">Cell name:</span></span>  <br/> |<span data-ttu-id="84e42-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="84e42-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="84e42-131">Чтобы получить ссылку на ячейку LineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="84e42-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84e42-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="84e42-132">Section index:</span></span>  <br/> |<span data-ttu-id="84e42-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84e42-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="84e42-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="84e42-134">Row index:</span></span>  <br/> |<span data-ttu-id="84e42-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="84e42-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="84e42-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="84e42-136">Cell index:</span></span>  <br/> |<span data-ttu-id="84e42-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="84e42-137">**visPLOJumpCode**</span></span> <br/> |
   

