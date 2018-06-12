---
title: Ячейка XGridDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Указывает тип сетки по горизонтали.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815194"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="fe5a5-103">Ячейка XGridDensity (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="fe5a5-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="fe5a5-104">Указывает тип сетки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="fe5a5-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="fe5a5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-105">**Value**</span></span>|<span data-ttu-id="fe5a5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-106">**Description**</span></span>|<span data-ttu-id="fe5a5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe5a5-108">0</span><span class="sxs-lookup"><span data-stu-id="fe5a5-108">0</span></span>  <br/> |<span data-ttu-id="fe5a5-109">Предопределенная</span><span class="sxs-lookup"><span data-stu-id="fe5a5-109">Fixed</span></span>  <br/> |<span data-ttu-id="fe5a5-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="fe5a5-111">2</span><span class="sxs-lookup"><span data-stu-id="fe5a5-111">2</span></span>  <br/> |<span data-ttu-id="fe5a5-112">Крупной</span><span class="sxs-lookup"><span data-stu-id="fe5a5-112">Coarse</span></span>  <br/> |<span data-ttu-id="fe5a5-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="fe5a5-114">4</span><span class="sxs-lookup"><span data-stu-id="fe5a5-114">4</span></span>  <br/> |<span data-ttu-id="fe5a5-115">Обычный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe5a5-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="fe5a5-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="fe5a5-117">8</span><span class="sxs-lookup"><span data-stu-id="fe5a5-117">8</span></span>  <br/> |<span data-ttu-id="fe5a5-118">Оптимизация</span><span class="sxs-lookup"><span data-stu-id="fe5a5-118">Fine</span></span>  <br/> |<span data-ttu-id="fe5a5-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe5a5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="fe5a5-120">Remarks</span></span>

<span data-ttu-id="fe5a5-121">В этой ячейке соответствует горизонтальный **Интервал сетки** параметра в **линейки &amp; сетки** диалоговое окно (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="fe5a5-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="fe5a5-122">Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fe5a5-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe5a5-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fe5a5-123">Cell name:</span></span>  <br/> |<span data-ttu-id="fe5a5-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="fe5a5-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="fe5a5-125">Для получения ссылки на ячейки XGridDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fe5a5-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe5a5-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fe5a5-126">Section index:</span></span>  <br/> |<span data-ttu-id="fe5a5-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fe5a5-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fe5a5-128">Row index:</span></span>  <br/> |<span data-ttu-id="fe5a5-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="fe5a5-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fe5a5-130">Cell index:</span></span>  <br/> |<span data-ttu-id="fe5a5-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="fe5a5-131">**visXGridDensity**</span></span> <br/> |
   

