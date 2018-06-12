---
title: Ячейка YRulerDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Определяет вертикальные деления на линейке для страницы.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815222"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="96c13-103">Ячейка YRulerDensity (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="96c13-103">YRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="96c13-104">Определяет вертикальные деления на линейке для страницы.</span><span class="sxs-lookup"><span data-stu-id="96c13-104">Specifies the vertical subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="96c13-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="96c13-105">**Value**</span></span>|<span data-ttu-id="96c13-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96c13-106">**Description**</span></span>|<span data-ttu-id="96c13-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="96c13-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="96c13-108">0</span><span class="sxs-lookup"><span data-stu-id="96c13-108">0</span></span>  <br/> |<span data-ttu-id="96c13-109">Предопределенная</span><span class="sxs-lookup"><span data-stu-id="96c13-109">Fixed</span></span>  <br/> |<span data-ttu-id="96c13-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="96c13-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="96c13-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="96c13-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="96c13-112">Крупной</span><span class="sxs-lookup"><span data-stu-id="96c13-112">Coarse</span></span>  <br/> |<span data-ttu-id="96c13-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="96c13-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="96c13-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="96c13-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="96c13-115">Обычный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96c13-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="96c13-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="96c13-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="96c13-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="96c13-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="96c13-118">Оптимизация</span><span class="sxs-lookup"><span data-stu-id="96c13-118">Fine</span></span>  <br/> |<span data-ttu-id="96c13-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="96c13-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96c13-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="96c13-120">Remarks</span></span>

<span data-ttu-id="96c13-121">В этой ячейке соответствует параметру вертикальной **подразделами** в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="96c13-121">This cell corresponds to the vertical **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="96c13-122">Чтобы получить ссылку на ячейку YRulerDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="96c13-122">To get a reference to the YRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96c13-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="96c13-123">Cell name:</span></span>  <br/> |<span data-ttu-id="96c13-124">YRulerDensity</span><span class="sxs-lookup"><span data-stu-id="96c13-124">YRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="96c13-125">Для получения ссылки на ячейки YRulerDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="96c13-125">To get a reference to the YRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96c13-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="96c13-126">Section index:</span></span>  <br/> |<span data-ttu-id="96c13-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="96c13-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="96c13-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="96c13-128">Row index:</span></span>  <br/> |<span data-ttu-id="96c13-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="96c13-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="96c13-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="96c13-130">Cell index:</span></span>  <br/> |<span data-ttu-id="96c13-131">**visYRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="96c13-131">**visYRulerDensity**</span></span> <br/> |
   

