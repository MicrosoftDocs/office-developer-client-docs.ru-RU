---
title: Ячейка YGridDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Указывает тип сетки по вертикали.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815224"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="e43d5-103">Ячейка YGridDensity (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="e43d5-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="e43d5-104">Указывает тип сетки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="e43d5-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="e43d5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e43d5-105">**Value**</span></span>|<span data-ttu-id="e43d5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e43d5-106">**Description**</span></span>|<span data-ttu-id="e43d5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e43d5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e43d5-108">0</span><span class="sxs-lookup"><span data-stu-id="e43d5-108">0</span></span>  <br/> |<span data-ttu-id="e43d5-109">Предопределенная</span><span class="sxs-lookup"><span data-stu-id="e43d5-109">Fixed</span></span>  <br/> |<span data-ttu-id="e43d5-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="e43d5-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="e43d5-111">2</span><span class="sxs-lookup"><span data-stu-id="e43d5-111">2</span></span>  <br/> |<span data-ttu-id="e43d5-112">Крупной</span><span class="sxs-lookup"><span data-stu-id="e43d5-112">Coarse</span></span>  <br/> |<span data-ttu-id="e43d5-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="e43d5-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="e43d5-114">4</span><span class="sxs-lookup"><span data-stu-id="e43d5-114">4</span></span>  <br/> |<span data-ttu-id="e43d5-115">Обычный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e43d5-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="e43d5-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="e43d5-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="e43d5-117">8</span><span class="sxs-lookup"><span data-stu-id="e43d5-117">8</span></span>  <br/> |<span data-ttu-id="e43d5-118">Оптимизация</span><span class="sxs-lookup"><span data-stu-id="e43d5-118">Fine</span></span>  <br/> |<span data-ttu-id="e43d5-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="e43d5-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e43d5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="e43d5-120">Remarks</span></span>

<span data-ttu-id="e43d5-121">В этой ячейке соответствует **сетки интервал** по вертикали параметра в **линейки &amp; сетки** диалоговое окно (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="e43d5-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="e43d5-122">Чтобы получить ссылку на ячейку YGridDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e43d5-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e43d5-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e43d5-123">Cell name:</span></span>  <br/> |<span data-ttu-id="e43d5-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="e43d5-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="e43d5-125">Для получения ссылки на ячейки YGridDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e43d5-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e43d5-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e43d5-126">Section index:</span></span>  <br/> |<span data-ttu-id="e43d5-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e43d5-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e43d5-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e43d5-128">Row index:</span></span>  <br/> |<span data-ttu-id="e43d5-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="e43d5-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="e43d5-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e43d5-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e43d5-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="e43d5-131">**visYGridDensity**</span></span> <br/> |
   

