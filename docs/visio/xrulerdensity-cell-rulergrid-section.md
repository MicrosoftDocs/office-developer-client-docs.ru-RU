---
title: Ячейка XRulerDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Определяет горизонтальные промежуточные деления линейки для страницы.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411472"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="ac9c2-103">Ячейка XRulerDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="ac9c2-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ac9c2-104">Определяет горизонтальные промежуточные деления линейки для страницы.</span><span class="sxs-lookup"><span data-stu-id="ac9c2-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="ac9c2-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-105">**Value**</span></span>|<span data-ttu-id="ac9c2-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-106">**Description**</span></span>|<span data-ttu-id="ac9c2-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac9c2-108">нуль</span><span class="sxs-lookup"><span data-stu-id="ac9c2-108">0</span></span>  <br/> |<span data-ttu-id="ac9c2-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="ac9c2-109">Fixed</span></span>  <br/> |<span data-ttu-id="ac9c2-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="ac9c2-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="ac9c2-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="ac9c2-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="ac9c2-112">Coarse</span></span>  <br/> |<span data-ttu-id="ac9c2-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="ac9c2-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="ac9c2-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="ac9c2-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac9c2-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="ac9c2-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="ac9c2-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="ac9c2-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="ac9c2-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="ac9c2-118">Fine</span></span>  <br/> |<span data-ttu-id="ac9c2-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac9c2-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac9c2-120">Remarks</span></span>

<span data-ttu-id="ac9c2-121">Эта ячейка соответствует параметру **Промежуточные деления по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="ac9c2-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ac9c2-122">Чтобы получить ссылку на ячейку XRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac9c2-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ac9c2-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="ac9c2-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="ac9c2-125">Чтобы получить ссылку на ячейку XRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac9c2-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-126">Section index:</span></span>  <br/> |<span data-ttu-id="ac9c2-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ac9c2-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-128">Row index:</span></span>  <br/> |<span data-ttu-id="ac9c2-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ac9c2-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ac9c2-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ac9c2-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="ac9c2-131">**visXRulerDensity**</span></span> <br/> |
   

