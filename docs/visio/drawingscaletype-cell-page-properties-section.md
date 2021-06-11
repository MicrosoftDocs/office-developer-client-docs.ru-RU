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
description: Определяет масштаб рисования, выбранный в диалоговом окне Настройка страницы (щелкните стрелку установки страницы на вкладке Главная).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428741"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="25e9a-103">DrawingScaleType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="25e9a-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="25e9a-104">Определяет масштаб рисования, выбранный в диалоговом окне **Настройка** страницы (щелкните стрелку **установки** страницы на вкладке **Главная).**</span><span class="sxs-lookup"><span data-stu-id="25e9a-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="25e9a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="25e9a-105">**Value**</span></span>|<span data-ttu-id="25e9a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25e9a-106">**Description**</span></span>|<span data-ttu-id="25e9a-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="25e9a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="25e9a-108">0</span><span class="sxs-lookup"><span data-stu-id="25e9a-108">0</span></span>  <br/> | <span data-ttu-id="25e9a-109">Нет масштабирования</span><span class="sxs-lookup"><span data-stu-id="25e9a-109">No Scale</span></span>  <br/> |<span data-ttu-id="25e9a-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="25e9a-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="25e9a-111">1</span><span class="sxs-lookup"><span data-stu-id="25e9a-111">1</span></span>  <br/> | <span data-ttu-id="25e9a-112">Архитектурная шкала</span><span class="sxs-lookup"><span data-stu-id="25e9a-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="25e9a-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="25e9a-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="25e9a-114">2</span><span class="sxs-lookup"><span data-stu-id="25e9a-114">2</span></span>  <br/> | <span data-ttu-id="25e9a-115">Шкала гражданской инженерии</span><span class="sxs-lookup"><span data-stu-id="25e9a-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="25e9a-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="25e9a-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="25e9a-117">3</span><span class="sxs-lookup"><span data-stu-id="25e9a-117">3</span></span>  <br/> | <span data-ttu-id="25e9a-118">Настраиваемая шкала</span><span class="sxs-lookup"><span data-stu-id="25e9a-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="25e9a-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="25e9a-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="25e9a-120">4 </span><span class="sxs-lookup"><span data-stu-id="25e9a-120">4</span></span>  <br/> | <span data-ttu-id="25e9a-121">Метрика</span><span class="sxs-lookup"><span data-stu-id="25e9a-121">Metric</span></span>  <br/> |<span data-ttu-id="25e9a-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="25e9a-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="25e9a-123">5 </span><span class="sxs-lookup"><span data-stu-id="25e9a-123">5</span></span>  <br/> | <span data-ttu-id="25e9a-124">Масштаб машиностроения</span><span class="sxs-lookup"><span data-stu-id="25e9a-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="25e9a-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="25e9a-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25e9a-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="25e9a-126">Remarks</span></span>

<span data-ttu-id="25e9a-127">Чтобы получить ссылку на ячейку DrawingScaleType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="25e9a-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25e9a-128">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="25e9a-128">Cell name:</span></span>  <br/> | <span data-ttu-id="25e9a-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="25e9a-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="25e9a-130">Чтобы получить ссылку на ячейку DrawingScaleType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="25e9a-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25e9a-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="25e9a-131">Section index:</span></span>  <br/> |<span data-ttu-id="25e9a-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25e9a-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="25e9a-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="25e9a-133">Row index:</span></span>  <br/> |<span data-ttu-id="25e9a-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="25e9a-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="25e9a-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="25e9a-135">Cell index:</span></span>  <br/> |<span data-ttu-id="25e9a-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="25e9a-136">**visPageDrawScaleType**</span></span> <br/> |
   

