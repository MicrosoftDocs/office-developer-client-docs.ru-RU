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
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815194"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="f2d4e-103">Ячейка XGridDensity (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="f2d4e-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="f2d4e-104">Указывает тип горизонтальной сетки для использования.</span><span class="sxs-lookup"><span data-stu-id="f2d4e-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="f2d4e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-105">**Value**</span></span>|<span data-ttu-id="f2d4e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-106">**Description**</span></span>|<span data-ttu-id="f2d4e-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2d4e-108">0</span><span class="sxs-lookup"><span data-stu-id="f2d4e-108">0%</span></span>  <br/> |<span data-ttu-id="f2d4e-109">Фиксация</span><span class="sxs-lookup"><span data-stu-id="f2d4e-109">Fixed</span></span>  <br/> |<span data-ttu-id="f2d4e-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="f2d4e-111">2</span><span class="sxs-lookup"><span data-stu-id="f2d4e-111">2</span></span>  <br/> |<span data-ttu-id="f2d4e-112">С большими интервалами</span><span class="sxs-lookup"><span data-stu-id="f2d4e-112">Coarse</span></span>  <br/> |<span data-ttu-id="f2d4e-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="f2d4e-114">4</span><span class="sxs-lookup"><span data-stu-id="f2d4e-114">4</span></span>  <br/> |<span data-ttu-id="f2d4e-115">С обычными интервалами (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2d4e-115">Normal (default).</span></span>  <br/> |<span data-ttu-id="f2d4e-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="f2d4e-117">8</span><span class="sxs-lookup"><span data-stu-id="f2d4e-117"> :=8</span></span>  <br/> |<span data-ttu-id="f2d4e-118">С небольшими интервалами</span><span class="sxs-lookup"><span data-stu-id="f2d4e-118">Fine</span></span>  <br/> |<span data-ttu-id="f2d4e-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2d4e-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2d4e-120">Remarks</span></span>

<span data-ttu-id="f2d4e-121">Эта ячейка соответствует параметру **Интервал между линиями сетки по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="f2d4e-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="f2d4e-122">Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d4e-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f2d4e-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="f2d4e-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="f2d4e-125">Чтобы получить ссылку на ячейку XGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d4e-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-126">Section index:</span></span>  <br/> |<span data-ttu-id="f2d4e-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f2d4e-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-128">Row index:</span></span>  <br/> |<span data-ttu-id="f2d4e-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="f2d4e-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2d4e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f2d4e-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="f2d4e-131">**visXGridDensity**</span></span> <br/> |
   

