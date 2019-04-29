---
title: Ячейка YGridDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Указывает тип вертикальной сетки для использования.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429812"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="84c98-103">Ячейка YGridDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="84c98-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="84c98-104">Указывает тип вертикальной сетки для использования.</span><span class="sxs-lookup"><span data-stu-id="84c98-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="84c98-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="84c98-105">**Value**</span></span>|<span data-ttu-id="84c98-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="84c98-106">**Description**</span></span>|<span data-ttu-id="84c98-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="84c98-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84c98-108">нуль</span><span class="sxs-lookup"><span data-stu-id="84c98-108">0</span></span>  <br/> |<span data-ttu-id="84c98-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84c98-109">Fixed</span></span>  <br/> |<span data-ttu-id="84c98-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="84c98-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="84c98-111">2</span><span class="sxs-lookup"><span data-stu-id="84c98-111">2</span></span>  <br/> |<span data-ttu-id="84c98-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="84c98-112">Coarse</span></span>  <br/> |<span data-ttu-id="84c98-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="84c98-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="84c98-114">SP4</span><span class="sxs-lookup"><span data-stu-id="84c98-114">4</span></span>  <br/> |<span data-ttu-id="84c98-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84c98-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="84c98-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="84c98-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="84c98-117">8,5</span><span class="sxs-lookup"><span data-stu-id="84c98-117">8</span></span>  <br/> |<span data-ttu-id="84c98-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="84c98-118">Fine</span></span>  <br/> |<span data-ttu-id="84c98-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="84c98-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84c98-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="84c98-120">Remarks</span></span>

<span data-ttu-id="84c98-121">Эта ячейка соответствует параметру **Интервал между линиями сетки по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="84c98-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="84c98-122">Чтобы получить ссылку на ячейку YGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="84c98-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84c98-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="84c98-123">Cell name:</span></span>  <br/> |<span data-ttu-id="84c98-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="84c98-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="84c98-125">Чтобы получить ссылку на ячейку YGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="84c98-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84c98-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="84c98-126">Section index:</span></span>  <br/> |<span data-ttu-id="84c98-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84c98-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="84c98-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="84c98-128">Row index:</span></span>  <br/> |<span data-ttu-id="84c98-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="84c98-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="84c98-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="84c98-130">Cell index:</span></span>  <br/> |<span data-ttu-id="84c98-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="84c98-131">**visYGridDensity**</span></span> <br/> |
   

