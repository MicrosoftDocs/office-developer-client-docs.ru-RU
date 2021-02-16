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
description: Определяет, когда соединители переходов.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421622"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="30548-103">ConLineJumpCode Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="30548-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="30548-104">Определяет, когда соединители переходов.</span><span class="sxs-lookup"><span data-stu-id="30548-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="30548-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="30548-105">**Value**</span></span>|<span data-ttu-id="30548-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="30548-106">**Description**</span></span>|<span data-ttu-id="30548-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="30548-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30548-108">0</span><span class="sxs-lookup"><span data-stu-id="30548-108">0</span></span>  <br/> |<span data-ttu-id="30548-109">Как указывает страница; На **вкладке "Конструктор"** щелкните стрелку в группе "Настройка страницы", а затем щелкните вкладку  **"Макет** и маршрут", чтобы увидеть спецификации страницы</span><span class="sxs-lookup"><span data-stu-id="30548-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="30548-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="30548-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="30548-111">1 </span><span class="sxs-lookup"><span data-stu-id="30548-111">1</span></span>  <br/> |<span data-ttu-id="30548-112">Никогда</span><span class="sxs-lookup"><span data-stu-id="30548-112">Never</span></span>  <br/> |<span data-ttu-id="30548-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="30548-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="30548-114">2 </span><span class="sxs-lookup"><span data-stu-id="30548-114">2</span></span>  <br/> |<span data-ttu-id="30548-115">Постоянно</span><span class="sxs-lookup"><span data-stu-id="30548-115">Always</span></span>  <br/> |<span data-ttu-id="30548-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="30548-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="30548-117">3 </span><span class="sxs-lookup"><span data-stu-id="30548-117">3</span></span>  <br/> |<span data-ttu-id="30548-118">Другие переходы соединители</span><span class="sxs-lookup"><span data-stu-id="30548-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="30548-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="30548-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="30548-120">4 </span><span class="sxs-lookup"><span data-stu-id="30548-120">4</span></span>  <br/> |<span data-ttu-id="30548-121">Ни один из соединители не переходов</span><span class="sxs-lookup"><span data-stu-id="30548-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="30548-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="30548-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30548-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="30548-123">Remarks</span></span>

<span data-ttu-id="30548-124">Вы также можете установить значение этой ячейки, выбрав динамический  соединитель, щелкнув "Поведение" в группе "Конструктор фигур" на вкладке "Разработчик", а затем выбрав вкладку **"Соединитель".**  [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="30548-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="30548-125">Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="30548-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30548-126">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="30548-126">Cell name:</span></span>  <br/> |<span data-ttu-id="30548-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="30548-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="30548-128">Чтобы получить ссылку на ячейку ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="30548-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30548-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="30548-129">Section index:</span></span>  <br/> |<span data-ttu-id="30548-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30548-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="30548-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="30548-131">Row index:</span></span>  <br/> |<span data-ttu-id="30548-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="30548-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="30548-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="30548-133">Cell index:</span></span>  <br/> |<span data-ttu-id="30548-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="30548-134">**visSLOJumpCode**</span></span> <br/> |
   

