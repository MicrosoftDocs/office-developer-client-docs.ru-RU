---
title: Ячейка XGridDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Указывает тип горизонтальной сетки для использования.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328990"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="9b4a5-103">Ячейка XGridDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="9b4a5-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="9b4a5-104">Указывает тип горизонтальной сетки для использования.</span><span class="sxs-lookup"><span data-stu-id="9b4a5-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="9b4a5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-105">**Value**</span></span>|<span data-ttu-id="9b4a5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-106">**Description**</span></span>|<span data-ttu-id="9b4a5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b4a5-108">нуль</span><span class="sxs-lookup"><span data-stu-id="9b4a5-108">0</span></span>  <br/> |<span data-ttu-id="9b4a5-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="9b4a5-109">Fixed</span></span>  <br/> |<span data-ttu-id="9b4a5-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="9b4a5-111">2</span><span class="sxs-lookup"><span data-stu-id="9b4a5-111">2</span></span>  <br/> |<span data-ttu-id="9b4a5-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="9b4a5-112">Coarse</span></span>  <br/> |<span data-ttu-id="9b4a5-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="9b4a5-114">SP4</span><span class="sxs-lookup"><span data-stu-id="9b4a5-114">4</span></span>  <br/> |<span data-ttu-id="9b4a5-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b4a5-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="9b4a5-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="9b4a5-117">8,5</span><span class="sxs-lookup"><span data-stu-id="9b4a5-117">8</span></span>  <br/> |<span data-ttu-id="9b4a5-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="9b4a5-118">Fine</span></span>  <br/> |<span data-ttu-id="9b4a5-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b4a5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b4a5-120">Remarks</span></span>

<span data-ttu-id="9b4a5-121">Эта ячейка соответствует параметру **Интервал между линиями сетки по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="9b4a5-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="9b4a5-122">Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b4a5-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-123">Cell name:</span></span>  <br/> |<span data-ttu-id="9b4a5-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="9b4a5-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="9b4a5-125">Чтобы получить ссылку на ячейку XGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b4a5-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-126">Section index:</span></span>  <br/> |<span data-ttu-id="9b4a5-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9b4a5-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-128">Row index:</span></span>  <br/> |<span data-ttu-id="9b4a5-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="9b4a5-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b4a5-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9b4a5-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="9b4a5-131">**visXGridDensity**</span></span> <br/> |
   

