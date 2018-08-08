---
title: Ячейка ConLineJumpCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Определяет, когда соединительные линии.
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813466"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="9e35d-103">Ячейка ConLineJumpCode (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="9e35d-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9e35d-104">Определяет, когда соединительные линии.</span><span class="sxs-lookup"><span data-stu-id="9e35d-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="9e35d-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9e35d-105">**Value**</span></span>|<span data-ttu-id="9e35d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9e35d-106">**Description**</span></span>|<span data-ttu-id="9e35d-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="9e35d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e35d-108">0</span><span class="sxs-lookup"><span data-stu-id="9e35d-108">0</span></span>  <br/> |<span data-ttu-id="9e35d-109">Как указано для страницы; на вкладке " **Конструктор** " щелкните стрелку в группе **Параметры страницы** и перейдите на вкладку **Макет и маршрутизации** , чтобы увидеть спецификации страниц</span><span class="sxs-lookup"><span data-stu-id="9e35d-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="9e35d-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="9e35d-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="9e35d-111">1</span><span class="sxs-lookup"><span data-stu-id="9e35d-111">1</span></span>  <br/> |<span data-ttu-id="9e35d-112">Никогда не</span><span class="sxs-lookup"><span data-stu-id="9e35d-112">Never</span></span>  <br/> |<span data-ttu-id="9e35d-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="9e35d-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="9e35d-114">2</span><span class="sxs-lookup"><span data-stu-id="9e35d-114">2</span></span>  <br/> |<span data-ttu-id="9e35d-115">Всегда</span><span class="sxs-lookup"><span data-stu-id="9e35d-115">Always</span></span>  <br/> |<span data-ttu-id="9e35d-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="9e35d-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="9e35d-117">3</span><span class="sxs-lookup"><span data-stu-id="9e35d-117">3</span></span>  <br/> |<span data-ttu-id="9e35d-118">Другие ссылки соединителя</span><span class="sxs-lookup"><span data-stu-id="9e35d-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="9e35d-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="9e35d-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="9e35d-120">4</span><span class="sxs-lookup"><span data-stu-id="9e35d-120">4</span></span>  <br/> |<span data-ttu-id="9e35d-121">Ни одна из соединительные линии</span><span class="sxs-lookup"><span data-stu-id="9e35d-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="9e35d-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="9e35d-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e35d-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e35d-123">Remarks</span></span>

<span data-ttu-id="9e35d-124">Можно также значение ячейки с выбор динамического соединителя, нажав кнопку **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " и затем выбрав вкладку **соединителя** .</span><span class="sxs-lookup"><span data-stu-id="9e35d-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="9e35d-125">Чтобы получить ссылку на ячейку ConLineJumpCode по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="9e35d-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e35d-126">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9e35d-126">Cell name:</span></span>  <br/> |<span data-ttu-id="9e35d-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="9e35d-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="9e35d-128">Для получения ссылки на ячейки ConLineJumpCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9e35d-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e35d-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9e35d-129">Section index:</span></span>  <br/> |<span data-ttu-id="9e35d-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e35d-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9e35d-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9e35d-131">Row index:</span></span>  <br/> |<span data-ttu-id="9e35d-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9e35d-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9e35d-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9e35d-133">Cell index:</span></span>  <br/> |<span data-ttu-id="9e35d-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="9e35d-134">**visSLOJumpCode**</span></span> <br/> |
   

