---
title: Ячейка XRulerDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Задает горизонтальную деления на линейке для страницы.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815190"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="a67ea-103">Ячейка XRulerDensity (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="a67ea-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a67ea-104">Задает горизонтальную деления на линейке для страницы.</span><span class="sxs-lookup"><span data-stu-id="a67ea-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="a67ea-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a67ea-105">**Value**</span></span>|<span data-ttu-id="a67ea-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a67ea-106">**Description**</span></span>|<span data-ttu-id="a67ea-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a67ea-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a67ea-108">0</span><span class="sxs-lookup"><span data-stu-id="a67ea-108">0</span></span>  <br/> |<span data-ttu-id="a67ea-109">Предопределенная</span><span class="sxs-lookup"><span data-stu-id="a67ea-109">Fixed</span></span>  <br/> |<span data-ttu-id="a67ea-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="a67ea-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="a67ea-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="a67ea-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="a67ea-112">Крупной</span><span class="sxs-lookup"><span data-stu-id="a67ea-112">Coarse</span></span>  <br/> |<span data-ttu-id="a67ea-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="a67ea-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="a67ea-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="a67ea-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="a67ea-115">Обычный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a67ea-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="a67ea-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="a67ea-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="a67ea-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="a67ea-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="a67ea-118">Оптимизация</span><span class="sxs-lookup"><span data-stu-id="a67ea-118">Fine</span></span>  <br/> |<span data-ttu-id="a67ea-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="a67ea-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a67ea-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="a67ea-120">Remarks</span></span>

<span data-ttu-id="a67ea-121">В этой ячейке соответствует параметру горизонтальной **подразделами** в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="a67ea-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a67ea-122">Чтобы получить ссылку на ячейку XRulerDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a67ea-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a67ea-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a67ea-123">Cell name:</span></span>  <br/> |<span data-ttu-id="a67ea-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="a67ea-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="a67ea-125">Для получения ссылки на ячейки XRulerDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a67ea-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a67ea-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a67ea-126">Section index:</span></span>  <br/> |<span data-ttu-id="a67ea-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a67ea-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a67ea-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a67ea-128">Row index:</span></span>  <br/> |<span data-ttu-id="a67ea-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a67ea-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a67ea-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a67ea-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a67ea-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="a67ea-131">**visXRulerDensity**</span></span> <br/> |
   

