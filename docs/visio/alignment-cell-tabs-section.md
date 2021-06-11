---
title: Alignment Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Указывает выравнивание вкладок.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425542"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="c5d48-103">Alignment Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="c5d48-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="c5d48-104">Указывает выравнивание вкладок.</span><span class="sxs-lookup"><span data-stu-id="c5d48-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="c5d48-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c5d48-105">**Value**</span></span>|<span data-ttu-id="c5d48-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="c5d48-106">**Alignment**</span></span>|<span data-ttu-id="c5d48-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c5d48-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c5d48-108">0</span><span class="sxs-lookup"><span data-stu-id="c5d48-108">0</span></span>  <br/> | <span data-ttu-id="c5d48-109">Left</span><span class="sxs-lookup"><span data-stu-id="c5d48-109">Left</span></span>  <br/> |<span data-ttu-id="c5d48-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="c5d48-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="c5d48-111">1</span><span class="sxs-lookup"><span data-stu-id="c5d48-111">1</span></span>  <br/> | <span data-ttu-id="c5d48-112">Center</span><span class="sxs-lookup"><span data-stu-id="c5d48-112">Center</span></span>  <br/> |<span data-ttu-id="c5d48-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="c5d48-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="c5d48-114">2</span><span class="sxs-lookup"><span data-stu-id="c5d48-114">2</span></span>  <br/> | <span data-ttu-id="c5d48-115">Right</span><span class="sxs-lookup"><span data-stu-id="c5d48-115">Right</span></span>  <br/> |<span data-ttu-id="c5d48-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="c5d48-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="c5d48-117">3</span><span class="sxs-lookup"><span data-stu-id="c5d48-117">3</span></span>  <br/> | <span data-ttu-id="c5d48-118">Десятичное число</span><span class="sxs-lookup"><span data-stu-id="c5d48-118">Decimal</span></span>  <br/> |<span data-ttu-id="c5d48-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="c5d48-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="c5d48-120">4 </span><span class="sxs-lookup"><span data-stu-id="c5d48-120">4</span></span>  <br/> | <span data-ttu-id="c5d48-121">Запятая</span><span class="sxs-lookup"><span data-stu-id="c5d48-121">Comma</span></span>  <br/> |<span data-ttu-id="c5d48-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="c5d48-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5d48-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5d48-123">Remarks</span></span>

<span data-ttu-id="c5d48-124">Чтобы получить ссылку на ячейку Выравнивание по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c5d48-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5d48-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c5d48-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c5d48-126">Вкладки.</span><span class="sxs-lookup"><span data-stu-id="c5d48-126">Tabs.</span></span>  <span data-ttu-id="c5d48-127">*ij,*            *где i и j =*  <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="c5d48-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="c5d48-128">Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c5d48-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5d48-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c5d48-129">Section index:</span></span>  <br/> |<span data-ttu-id="c5d48-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="c5d48-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="c5d48-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c5d48-131">Row index:</span></span>  <br/> |<span data-ttu-id="c5d48-132">**visRowTab +** *i,*            *где i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c5d48-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c5d48-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c5d48-133">Cell index:</span></span>  <br/> | <span data-ttu-id="c5d48-134">(*j*  \*3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="c5d48-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

