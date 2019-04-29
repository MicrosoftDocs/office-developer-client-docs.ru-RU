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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421622"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="febd9-103">ConLineJumpCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="febd9-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="febd9-104">Определяет, когда соединитель переходит.</span><span class="sxs-lookup"><span data-stu-id="febd9-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="febd9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="febd9-105">**Value**</span></span>|<span data-ttu-id="febd9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="febd9-106">**Description**</span></span>|<span data-ttu-id="febd9-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="febd9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="febd9-108">нуль</span><span class="sxs-lookup"><span data-stu-id="febd9-108">0</span></span>  <br/> |<span data-ttu-id="febd9-109">В качестве указания страницы; на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , а затем перейдите на вкладку **Макет и маршрутизация** , чтобы просмотреть спецификации страницы.</span><span class="sxs-lookup"><span data-stu-id="febd9-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="febd9-110">**Виссложумпдефаулт**</span><span class="sxs-lookup"><span data-stu-id="febd9-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="febd9-111">1,1</span><span class="sxs-lookup"><span data-stu-id="febd9-111">1</span></span>  <br/> |<span data-ttu-id="febd9-112">Никогда</span><span class="sxs-lookup"><span data-stu-id="febd9-112">Never</span></span>  <br/> |<span data-ttu-id="febd9-113">**Виссложумпневер**</span><span class="sxs-lookup"><span data-stu-id="febd9-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="febd9-114">2</span><span class="sxs-lookup"><span data-stu-id="febd9-114">2</span></span>  <br/> |<span data-ttu-id="febd9-115">Постоянно</span><span class="sxs-lookup"><span data-stu-id="febd9-115">Always</span></span>  <br/> |<span data-ttu-id="febd9-116">**Виссложумпалвайс**</span><span class="sxs-lookup"><span data-stu-id="febd9-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="febd9-117">4</span><span class="sxs-lookup"><span data-stu-id="febd9-117">3</span></span>  <br/> |<span data-ttu-id="febd9-118">Другие переходы соединителей</span><span class="sxs-lookup"><span data-stu-id="febd9-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="febd9-119">**Виссложумпосер**</span><span class="sxs-lookup"><span data-stu-id="febd9-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="febd9-120">SP4</span><span class="sxs-lookup"><span data-stu-id="febd9-120">4</span></span>  <br/> |<span data-ttu-id="febd9-121">Ни один из соединителей не переместится</span><span class="sxs-lookup"><span data-stu-id="febd9-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="febd9-122">**Виссложумпнеисер**</span><span class="sxs-lookup"><span data-stu-id="febd9-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="febd9-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="febd9-123">Remarks</span></span>

<span data-ttu-id="febd9-124">Можно также задать значение этой ячейки, выбрав динамический соединитель, нажав кнопку **поведение** в группе **Макет фигуры** на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) , а затем щелкнув вкладку **соединитель** .</span><span class="sxs-lookup"><span data-stu-id="febd9-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="febd9-125">Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="febd9-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="febd9-126">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="febd9-126">Cell name:</span></span>  <br/> |<span data-ttu-id="febd9-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="febd9-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="febd9-128">Чтобы получить ссылку на ячейку ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="febd9-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="febd9-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="febd9-129">Section index:</span></span>  <br/> |<span data-ttu-id="febd9-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="febd9-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="febd9-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="febd9-131">Row index:</span></span>  <br/> |<span data-ttu-id="febd9-132">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="febd9-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="febd9-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="febd9-133">Cell index:</span></span>  <br/> |<span data-ttu-id="febd9-134">**Виссложумпкоде**</span><span class="sxs-lookup"><span data-stu-id="febd9-134">**visSLOJumpCode**</span></span> <br/> |
   

