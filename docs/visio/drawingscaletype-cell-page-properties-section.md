---
title: DrawingScaleType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Определяет масштаб документа, выбранный в диалоговом окне "Параметры страницы" (щелкните стрелку настройки страницы на вкладке "Главная").
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428741"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="f74ae-103">DrawingScaleType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f74ae-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="f74ae-104">Определяет масштаб документа, выбранный в диалоговом окне " **Параметры страницы** " (щелкните стрелку **настройки страницы** на вкладке " **Главная** ").</span><span class="sxs-lookup"><span data-stu-id="f74ae-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="f74ae-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f74ae-105">**Value**</span></span>|<span data-ttu-id="f74ae-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f74ae-106">**Description**</span></span>|<span data-ttu-id="f74ae-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f74ae-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f74ae-108">нуль</span><span class="sxs-lookup"><span data-stu-id="f74ae-108">0</span></span>  <br/> | <span data-ttu-id="f74ae-109">Без масштаба</span><span class="sxs-lookup"><span data-stu-id="f74ae-109">No Scale</span></span>  <br/> |<span data-ttu-id="f74ae-110">**висноскале**</span><span class="sxs-lookup"><span data-stu-id="f74ae-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="f74ae-111">1,1</span><span class="sxs-lookup"><span data-stu-id="f74ae-111">1</span></span>  <br/> | <span data-ttu-id="f74ae-112">Архитектурный масштаб</span><span class="sxs-lookup"><span data-stu-id="f74ae-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="f74ae-113">**висарчитектурал**</span><span class="sxs-lookup"><span data-stu-id="f74ae-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="f74ae-114">2</span><span class="sxs-lookup"><span data-stu-id="f74ae-114">2</span></span>  <br/> | <span data-ttu-id="f74ae-115">Масштабирование гражданского проектирования</span><span class="sxs-lookup"><span data-stu-id="f74ae-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="f74ae-116">**висенгиниринг**</span><span class="sxs-lookup"><span data-stu-id="f74ae-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="f74ae-117">4</span><span class="sxs-lookup"><span data-stu-id="f74ae-117">3</span></span>  <br/> | <span data-ttu-id="f74ae-118">Настраиваемый масштаб</span><span class="sxs-lookup"><span data-stu-id="f74ae-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="f74ae-119">**висскалекустом**</span><span class="sxs-lookup"><span data-stu-id="f74ae-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="f74ae-120">4 </span><span class="sxs-lookup"><span data-stu-id="f74ae-120">4</span></span>  <br/> | <span data-ttu-id="f74ae-121">Метрика</span><span class="sxs-lookup"><span data-stu-id="f74ae-121">Metric</span></span>  <br/> |<span data-ttu-id="f74ae-122">**висскалеметрик**</span><span class="sxs-lookup"><span data-stu-id="f74ae-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="f74ae-123">5 </span><span class="sxs-lookup"><span data-stu-id="f74ae-123">5</span></span>  <br/> | <span data-ttu-id="f74ae-124">Механическая масштабируемость</span><span class="sxs-lookup"><span data-stu-id="f74ae-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="f74ae-125">**висскалемечаникал**</span><span class="sxs-lookup"><span data-stu-id="f74ae-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f74ae-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="f74ae-126">Remarks</span></span>

<span data-ttu-id="f74ae-127">Чтобы получить ссылку на ячейку DrawingScaleType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f74ae-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f74ae-128">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f74ae-128">Cell name:</span></span>  <br/> | <span data-ttu-id="f74ae-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="f74ae-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="f74ae-130">Чтобы получить ссылку на ячейку DrawingScaleType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f74ae-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f74ae-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f74ae-131">Section index:</span></span>  <br/> |<span data-ttu-id="f74ae-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f74ae-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f74ae-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f74ae-133">Row index:</span></span>  <br/> |<span data-ttu-id="f74ae-134">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="f74ae-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="f74ae-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f74ae-135">Cell index:</span></span>  <br/> |<span data-ttu-id="f74ae-136">**виспажедравскалетипе**</span><span class="sxs-lookup"><span data-stu-id="f74ae-136">**visPageDrawScaleType**</span></span> <br/> |
   

