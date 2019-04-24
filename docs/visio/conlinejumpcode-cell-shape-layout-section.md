---
title: ConLineJumpCode Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Определяет, когда соединитель переходит.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284090"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="c4cc6-103">ConLineJumpCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="c4cc6-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c4cc6-104">Определяет, когда соединитель переходит.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="c4cc6-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-105">**Value**</span></span>|<span data-ttu-id="c4cc6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-106">**Description**</span></span>|<span data-ttu-id="c4cc6-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4cc6-108">нуль</span><span class="sxs-lookup"><span data-stu-id="c4cc6-108">0</span></span>  <br/> |<span data-ttu-id="c4cc6-109">В качестве указания страницы; на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , а затем перейдите на вкладку **Макет и маршрутизация** , чтобы просмотреть спецификации страницы.</span><span class="sxs-lookup"><span data-stu-id="c4cc6-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="c4cc6-110">**Виссложумпдефаулт**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="c4cc6-111">1,1</span><span class="sxs-lookup"><span data-stu-id="c4cc6-111">1</span></span>  <br/> |<span data-ttu-id="c4cc6-112">Никогда</span><span class="sxs-lookup"><span data-stu-id="c4cc6-112">Never</span></span>  <br/> |<span data-ttu-id="c4cc6-113">**Виссложумпневер**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="c4cc6-114">2</span><span class="sxs-lookup"><span data-stu-id="c4cc6-114">2</span></span>  <br/> |<span data-ttu-id="c4cc6-115">Постоянно</span><span class="sxs-lookup"><span data-stu-id="c4cc6-115">Always</span></span>  <br/> |<span data-ttu-id="c4cc6-116">**Виссложумпалвайс**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="c4cc6-117">4</span><span class="sxs-lookup"><span data-stu-id="c4cc6-117">3</span></span>  <br/> |<span data-ttu-id="c4cc6-118">Другие переходы соединителей</span><span class="sxs-lookup"><span data-stu-id="c4cc6-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="c4cc6-119">**Виссложумпосер**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="c4cc6-120">SP4</span><span class="sxs-lookup"><span data-stu-id="c4cc6-120">4</span></span>  <br/> |<span data-ttu-id="c4cc6-121">Ни один из соединителей не переместится</span><span class="sxs-lookup"><span data-stu-id="c4cc6-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="c4cc6-122">**Виссложумпнеисер**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4cc6-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4cc6-123">Remarks</span></span>

<span data-ttu-id="c4cc6-124">Можно также задать значение этой ячейки, выбрав динамический соединитель, нажав кнопку **поведение** в группе **Макет фигуры** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем щелкнув вкладку **соединитель** .</span><span class="sxs-lookup"><span data-stu-id="c4cc6-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="c4cc6-125">Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4cc6-126">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-126">Cell name:</span></span>  <br/> |<span data-ttu-id="c4cc6-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="c4cc6-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="c4cc6-128">Чтобы получить ссылку на ячейку ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4cc6-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-129">Section index:</span></span>  <br/> |<span data-ttu-id="c4cc6-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c4cc6-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-131">Row index:</span></span>  <br/> |<span data-ttu-id="c4cc6-132">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c4cc6-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c4cc6-133">Cell index:</span></span>  <br/> |<span data-ttu-id="c4cc6-134">**Виссложумпкоде**</span><span class="sxs-lookup"><span data-stu-id="c4cc6-134">**visSLOJumpCode**</span></span> <br/> |
   

