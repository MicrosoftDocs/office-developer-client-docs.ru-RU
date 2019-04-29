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
description: Задает выравнивание табуляции.
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425542"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="c55bc-103">Alignment Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="c55bc-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="c55bc-104">Задает выравнивание табуляции.</span><span class="sxs-lookup"><span data-stu-id="c55bc-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="c55bc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c55bc-105">**Value**</span></span>|<span data-ttu-id="c55bc-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="c55bc-106">**Alignment**</span></span>|<span data-ttu-id="c55bc-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c55bc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c55bc-108">нуль</span><span class="sxs-lookup"><span data-stu-id="c55bc-108">0</span></span>  <br/> | <span data-ttu-id="c55bc-109">Left</span><span class="sxs-lookup"><span data-stu-id="c55bc-109">Left</span></span>  <br/> |<span data-ttu-id="c55bc-110">**Вистабстоплефт**</span><span class="sxs-lookup"><span data-stu-id="c55bc-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="c55bc-111">1,1</span><span class="sxs-lookup"><span data-stu-id="c55bc-111">1</span></span>  <br/> | <span data-ttu-id="c55bc-112">Center</span><span class="sxs-lookup"><span data-stu-id="c55bc-112">Center</span></span>  <br/> |<span data-ttu-id="c55bc-113">**Вистабстопцентер**</span><span class="sxs-lookup"><span data-stu-id="c55bc-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="c55bc-114">2</span><span class="sxs-lookup"><span data-stu-id="c55bc-114">2</span></span>  <br/> | <span data-ttu-id="c55bc-115">Right</span><span class="sxs-lookup"><span data-stu-id="c55bc-115">Right</span></span>  <br/> |<span data-ttu-id="c55bc-116">**Вистабстопригхт**</span><span class="sxs-lookup"><span data-stu-id="c55bc-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="c55bc-117">4</span><span class="sxs-lookup"><span data-stu-id="c55bc-117">3</span></span>  <br/> | <span data-ttu-id="c55bc-118">Десятичный</span><span class="sxs-lookup"><span data-stu-id="c55bc-118">Decimal</span></span>  <br/> |<span data-ttu-id="c55bc-119">**ВистабстопдеЦимал**</span><span class="sxs-lookup"><span data-stu-id="c55bc-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="c55bc-120">SP4</span><span class="sxs-lookup"><span data-stu-id="c55bc-120">4</span></span>  <br/> | <span data-ttu-id="c55bc-121">Числ</span><span class="sxs-lookup"><span data-stu-id="c55bc-121">Comma</span></span>  <br/> |<span data-ttu-id="c55bc-122">**Вистабстопкомма**</span><span class="sxs-lookup"><span data-stu-id="c55bc-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c55bc-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c55bc-123">Remarks</span></span>

<span data-ttu-id="c55bc-124">Чтобы получить ссылку на ячейку выравнивания по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="c55bc-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c55bc-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c55bc-125">Cell name:</span></span>  <br/> | <span data-ttu-id="c55bc-126">Знаков.</span><span class="sxs-lookup"><span data-stu-id="c55bc-126">Tabs.</span></span>  <span data-ttu-id="c55bc-127">*ИЖ* , где *i и j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="c55bc-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="c55bc-128">Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c55bc-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c55bc-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c55bc-129">Section index:</span></span>  <br/> |<span data-ttu-id="c55bc-130">**Виссектионтаб**</span><span class="sxs-lookup"><span data-stu-id="c55bc-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="c55bc-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c55bc-131">Row index:</span></span>  <br/> |<span data-ttu-id="c55bc-132">**висровтаб +** \*\* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c55bc-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c55bc-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c55bc-133">Cell index:</span></span>  <br/> | <span data-ttu-id="c55bc-134">(*j* \* 3) **+ вистабалигн**</span><span class="sxs-lookup"><span data-stu-id="c55bc-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

