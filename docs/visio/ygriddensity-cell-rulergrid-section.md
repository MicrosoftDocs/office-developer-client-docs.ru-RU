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
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815224"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="5c31c-103">Ячейка YGridDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="5c31c-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="5c31c-104">Указывает тип вертикальной сетки для использования.</span><span class="sxs-lookup"><span data-stu-id="5c31c-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="5c31c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5c31c-105">**Value**</span></span>|<span data-ttu-id="5c31c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c31c-106">**Description**</span></span>|<span data-ttu-id="5c31c-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="5c31c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c31c-108">0</span><span class="sxs-lookup"><span data-stu-id="5c31c-108">0%</span></span>  <br/> |<span data-ttu-id="5c31c-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="5c31c-109">Fixed</span></span>  <br/> |<span data-ttu-id="5c31c-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="5c31c-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="5c31c-111">2</span><span class="sxs-lookup"><span data-stu-id="5c31c-111">2</span></span>  <br/> |<span data-ttu-id="5c31c-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="5c31c-112">Coarse</span></span>  <br/> |<span data-ttu-id="5c31c-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="5c31c-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="5c31c-114">4</span><span class="sxs-lookup"><span data-stu-id="5c31c-114">4</span></span>  <br/> |<span data-ttu-id="5c31c-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c31c-115">Normal (default).</span></span>  <br/> |<span data-ttu-id="5c31c-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="5c31c-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="5c31c-117">8</span><span class="sxs-lookup"><span data-stu-id="5c31c-117"> :=8</span></span>  <br/> |<span data-ttu-id="5c31c-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="5c31c-118">Fine</span></span>  <br/> |<span data-ttu-id="5c31c-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="5c31c-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c31c-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c31c-120">Remarks</span></span>

<span data-ttu-id="5c31c-121">Эта ячейка соответствует параметру **Интервал между линиями сетки по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="5c31c-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="5c31c-122">Чтобы получить ссылку на ячейку YGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="5c31c-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c31c-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c31c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="5c31c-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="5c31c-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="5c31c-125">Чтобы получить ссылку на ячейку YGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5c31c-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c31c-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5c31c-126">Section index:</span></span>  <br/> |<span data-ttu-id="5c31c-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c31c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c31c-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5c31c-128">Row index:</span></span>  <br/> |<span data-ttu-id="5c31c-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="5c31c-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="5c31c-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c31c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="5c31c-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="5c31c-131">**visYGridDensity**</span></span> <br/> |
   

