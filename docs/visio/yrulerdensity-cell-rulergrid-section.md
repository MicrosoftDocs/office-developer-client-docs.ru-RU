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
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406803"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="a0873-103">Ячейка YRulerDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="a0873-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a0873-104">Определяет вертикальные промежуточные деления линейки для страницы.</span><span class="sxs-lookup"><span data-stu-id="a0873-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="a0873-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a0873-105">**Value**</span></span>|<span data-ttu-id="a0873-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0873-106">**Description**</span></span>|<span data-ttu-id="a0873-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a0873-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0873-108">0</span><span class="sxs-lookup"><span data-stu-id="a0873-108">0</span></span>  <br/> |<span data-ttu-id="a0873-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="a0873-109">Fixed</span></span>  <br/> |<span data-ttu-id="a0873-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="a0873-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="a0873-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="a0873-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="a0873-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="a0873-112">Coarse</span></span>  <br/> |<span data-ttu-id="a0873-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="a0873-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="a0873-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="a0873-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="a0873-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0873-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="a0873-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="a0873-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="a0873-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="a0873-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="a0873-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="a0873-118">Fine</span></span>  <br/> |<span data-ttu-id="a0873-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="a0873-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0873-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0873-120">Remarks</span></span>

<span data-ttu-id="a0873-121">Эта ячейка соответствует параметру **Промежуточные деления по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="a0873-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a0873-122">Чтобы получить ссылку на ячейку YRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="a0873-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0873-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a0873-123">Cell name:</span></span>  <br/> |<span data-ttu-id="a0873-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="a0873-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="a0873-125">Чтобы получить ссылку на ячейку YRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a0873-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0873-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a0873-126">Section index:</span></span>  <br/> |<span data-ttu-id="a0873-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0873-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0873-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a0873-128">Row index:</span></span>  <br/> |<span data-ttu-id="a0873-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a0873-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a0873-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a0873-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a0873-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="a0873-131">**visYRulerDensity**</span></span> <br/> |
   

