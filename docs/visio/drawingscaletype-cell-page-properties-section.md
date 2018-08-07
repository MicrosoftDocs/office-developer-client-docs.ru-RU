---
title: Ячейка DrawingScaleType (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Определяет масштаб документа, указанный в диалоговом окне Параметры страницы (щелкните стрелку Параметры страницы на вкладке "Главная").
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813662"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="62740-103">Ячейка DrawingScaleType (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="62740-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="62740-104">Определяет масштаб документа, указанный в диалоговом окне **Параметры страницы** (щелкните стрелку **Параметры страницы** на вкладке **Главная** ).</span><span class="sxs-lookup"><span data-stu-id="62740-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="62740-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="62740-105">**Value**</span></span>|<span data-ttu-id="62740-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62740-106">**Description**</span></span>|<span data-ttu-id="62740-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="62740-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="62740-108">0</span><span class="sxs-lookup"><span data-stu-id="62740-108">0</span></span>  <br/> | <span data-ttu-id="62740-109">Нет масштаба</span><span class="sxs-lookup"><span data-stu-id="62740-109">No Scale</span></span>  <br/> |<span data-ttu-id="62740-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="62740-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="62740-111">1</span><span class="sxs-lookup"><span data-stu-id="62740-111">1</span></span>  <br/> | <span data-ttu-id="62740-112">Архитектурные масштаба</span><span class="sxs-lookup"><span data-stu-id="62740-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="62740-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="62740-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="62740-114">2</span><span class="sxs-lookup"><span data-stu-id="62740-114">2</span></span>  <br/> | <span data-ttu-id="62740-115">Масштаб Гражданское Engineering</span><span class="sxs-lookup"><span data-stu-id="62740-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="62740-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="62740-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="62740-117">3</span><span class="sxs-lookup"><span data-stu-id="62740-117">3</span></span>  <br/> | <span data-ttu-id="62740-118">Настраиваемые масштаба</span><span class="sxs-lookup"><span data-stu-id="62740-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="62740-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="62740-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="62740-120">4</span><span class="sxs-lookup"><span data-stu-id="62740-120">4</span></span>  <br/> | <span data-ttu-id="62740-121">Метрики</span><span class="sxs-lookup"><span data-stu-id="62740-121">Metric</span></span>  <br/> |<span data-ttu-id="62740-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="62740-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="62740-123">5</span><span class="sxs-lookup"><span data-stu-id="62740-123">5</span></span>  <br/> | <span data-ttu-id="62740-124">Схема Engineering масштаба</span><span class="sxs-lookup"><span data-stu-id="62740-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="62740-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="62740-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62740-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="62740-126">Remarks</span></span>

<span data-ttu-id="62740-127">Чтобы получить ссылку на ячейку DrawingScaleType по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="62740-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62740-128">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="62740-128">Cell name:</span></span>  <br/> | <span data-ttu-id="62740-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="62740-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="62740-130">Для получения ссылки на ячейки DrawingScaleType по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="62740-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62740-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="62740-131">Section index:</span></span>  <br/> |<span data-ttu-id="62740-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62740-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62740-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="62740-133">Row index:</span></span>  <br/> |<span data-ttu-id="62740-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="62740-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="62740-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="62740-135">Cell index:</span></span>  <br/> |<span data-ttu-id="62740-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="62740-136">**visPageDrawScaleType**</span></span> <br/> |
   

