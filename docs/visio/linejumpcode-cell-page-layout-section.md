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
description: Определяет соединители, к которым вы хотите добавить переходы.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416253"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="9992c-103">LineJumpCode Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="9992c-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="9992c-104">Определяет соединители, к которым вы хотите добавить переходы.</span><span class="sxs-lookup"><span data-stu-id="9992c-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="9992c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9992c-105">**Value**</span></span>|<span data-ttu-id="9992c-106">**Соединители, к которым вы хотите добавить переходы**</span><span class="sxs-lookup"><span data-stu-id="9992c-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="9992c-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="9992c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9992c-108">нуль</span><span class="sxs-lookup"><span data-stu-id="9992c-108">0</span></span>  <br/> |<span data-ttu-id="9992c-109">Нет</span><span class="sxs-lookup"><span data-stu-id="9992c-109">None</span></span>  <br/> |<span data-ttu-id="9992c-110">**виспложумпноне**</span><span class="sxs-lookup"><span data-stu-id="9992c-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="9992c-111">1,1</span><span class="sxs-lookup"><span data-stu-id="9992c-111">1</span></span>  <br/> |<span data-ttu-id="9992c-112">Горизонтальные линии</span><span class="sxs-lookup"><span data-stu-id="9992c-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="9992c-113">**виспложумфоризонтал**</span><span class="sxs-lookup"><span data-stu-id="9992c-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="9992c-114">2</span><span class="sxs-lookup"><span data-stu-id="9992c-114">2</span></span>  <br/> |<span data-ttu-id="9992c-115">Вертикальные линии</span><span class="sxs-lookup"><span data-stu-id="9992c-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="9992c-116">**виспложумпвертикал**</span><span class="sxs-lookup"><span data-stu-id="9992c-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="9992c-117">4</span><span class="sxs-lookup"><span data-stu-id="9992c-117">3</span></span>  <br/> |<span data-ttu-id="9992c-118">Последняя строка маршрута</span><span class="sxs-lookup"><span data-stu-id="9992c-118">Last routed line</span></span>  <br/> |<span data-ttu-id="9992c-119">**виспложумпластраутед**</span><span class="sxs-lookup"><span data-stu-id="9992c-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="9992c-120">4 </span><span class="sxs-lookup"><span data-stu-id="9992c-120">4</span></span>  <br/> |<span data-ttu-id="9992c-121">Последняя отображаемая строка (верхняя фигура в *z* -порядке)</span><span class="sxs-lookup"><span data-stu-id="9992c-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="9992c-122">**виспложумпдисплайордер**</span><span class="sxs-lookup"><span data-stu-id="9992c-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="9992c-123">5 </span><span class="sxs-lookup"><span data-stu-id="9992c-123">5</span></span>  <br/> |<span data-ttu-id="9992c-124">Первая отображаемая строка (фигура в нижней части *z* -порядка)</span><span class="sxs-lookup"><span data-stu-id="9992c-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="9992c-125">**виспложумпреверседисплайордер**</span><span class="sxs-lookup"><span data-stu-id="9992c-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9992c-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="9992c-126">Remarks</span></span>

<span data-ttu-id="9992c-127">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).</span><span class="sxs-lookup"><span data-stu-id="9992c-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="9992c-128">Чтобы получить ссылку на ячейку LineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="9992c-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9992c-129">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9992c-129">Cell name:</span></span>  <br/> |<span data-ttu-id="9992c-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="9992c-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="9992c-131">Чтобы получить ссылку на ячейку LineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9992c-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9992c-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9992c-132">Section index:</span></span>  <br/> |<span data-ttu-id="9992c-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9992c-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9992c-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9992c-134">Row index:</span></span>  <br/> |<span data-ttu-id="9992c-135">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="9992c-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="9992c-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9992c-136">Cell index:</span></span>  <br/> |<span data-ttu-id="9992c-137">**виспложумпкоде**</span><span class="sxs-lookup"><span data-stu-id="9992c-137">**visPLOJumpCode**</span></span> <br/> |
   

