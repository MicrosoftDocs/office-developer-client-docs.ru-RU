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
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815190"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="35228-103">Ячейка XRulerDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="35228-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="35228-104">Определяет горизонтальные промежуточные деления линейки для страницы.</span><span class="sxs-lookup"><span data-stu-id="35228-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="35228-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="35228-105">**Value**</span></span>|<span data-ttu-id="35228-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35228-106">**Description**</span></span>|<span data-ttu-id="35228-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="35228-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35228-108">0</span><span class="sxs-lookup"><span data-stu-id="35228-108">0%</span></span>  <br/> |<span data-ttu-id="35228-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="35228-109">Fixed</span></span>  <br/> |<span data-ttu-id="35228-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="35228-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="35228-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="35228-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="35228-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="35228-112">Coarse</span></span>  <br/> |<span data-ttu-id="35228-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="35228-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="35228-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="35228-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="35228-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35228-115">Normal (default).</span></span>  <br/> |<span data-ttu-id="35228-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="35228-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="35228-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="35228-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="35228-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="35228-118">Fine</span></span>  <br/> |<span data-ttu-id="35228-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="35228-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35228-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="35228-120">Remarks</span></span>

<span data-ttu-id="35228-121">Эта ячейка соответствует параметру **Промежуточные деления по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="35228-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="35228-122">Чтобы получить ссылку на ячейку XRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="35228-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35228-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="35228-123">Cell name:</span></span>  <br/> |<span data-ttu-id="35228-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="35228-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="35228-125">Чтобы получить ссылку на ячейку XRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="35228-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35228-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="35228-126">Section index:</span></span>  <br/> |<span data-ttu-id="35228-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35228-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="35228-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="35228-128">Row index:</span></span>  <br/> |<span data-ttu-id="35228-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="35228-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="35228-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="35228-130">Cell index:</span></span>  <br/> |<span data-ttu-id="35228-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="35228-131">**visXRulerDensity**</span></span> <br/> |
   

