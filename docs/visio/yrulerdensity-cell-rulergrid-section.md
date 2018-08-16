---
title: Ячейка YRulerDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Определяет вертикальные промежуточные деления линейки для страницы.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815222"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="525e0-103">Ячейка YRulerDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="525e0-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="525e0-104">Определяет вертикальные промежуточные деления линейки для страницы.</span><span class="sxs-lookup"><span data-stu-id="525e0-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="525e0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="525e0-105">**Value**</span></span>|<span data-ttu-id="525e0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="525e0-106">**Description**</span></span>|<span data-ttu-id="525e0-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="525e0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="525e0-108">0</span><span class="sxs-lookup"><span data-stu-id="525e0-108">0%</span></span>  <br/> |<span data-ttu-id="525e0-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="525e0-109">Fixed</span></span>  <br/> |<span data-ttu-id="525e0-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="525e0-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="525e0-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="525e0-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="525e0-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="525e0-112">Coarse</span></span>  <br/> |<span data-ttu-id="525e0-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="525e0-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="525e0-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="525e0-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="525e0-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="525e0-115">Normal (default).</span></span>  <br/> |<span data-ttu-id="525e0-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="525e0-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="525e0-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="525e0-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="525e0-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="525e0-118">Fine</span></span>  <br/> |<span data-ttu-id="525e0-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="525e0-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="525e0-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="525e0-120">Remarks</span></span>

<span data-ttu-id="525e0-121">Эта ячейка соответствует параметру **Промежуточные деления по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="525e0-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="525e0-122">Чтобы получить ссылку на ячейку YRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="525e0-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="525e0-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="525e0-123">Cell name:</span></span>  <br/> |<span data-ttu-id="525e0-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="525e0-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="525e0-125">Чтобы получить ссылку на ячейку YRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="525e0-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="525e0-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="525e0-126">Section index:</span></span>  <br/> |<span data-ttu-id="525e0-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="525e0-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="525e0-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="525e0-128">Row index:</span></span>  <br/> |<span data-ttu-id="525e0-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="525e0-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="525e0-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="525e0-130">Cell index:</span></span>  <br/> |<span data-ttu-id="525e0-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="525e0-131">**visYRulerDensity**</span></span> <br/> |
   

