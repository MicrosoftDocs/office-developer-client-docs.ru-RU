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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341540"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="f6cc7-103">Alignment Cell (Tabs Section)</span><span class="sxs-lookup"><span data-stu-id="f6cc7-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="f6cc7-104">Задает выравнивание табуляции.</span><span class="sxs-lookup"><span data-stu-id="f6cc7-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="f6cc7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-105">**Value**</span></span>|<span data-ttu-id="f6cc7-106">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-106">**Alignment**</span></span>|<span data-ttu-id="f6cc7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f6cc7-108">нуль</span><span class="sxs-lookup"><span data-stu-id="f6cc7-108">0</span></span>  <br/> | <span data-ttu-id="f6cc7-109">Left</span><span class="sxs-lookup"><span data-stu-id="f6cc7-109">Left</span></span>  <br/> |<span data-ttu-id="f6cc7-110">**Вистабстоплефт**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="f6cc7-111">1,1</span><span class="sxs-lookup"><span data-stu-id="f6cc7-111">1</span></span>  <br/> | <span data-ttu-id="f6cc7-112">Center</span><span class="sxs-lookup"><span data-stu-id="f6cc7-112">Center</span></span>  <br/> |<span data-ttu-id="f6cc7-113">**Вистабстопцентер**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="f6cc7-114">2</span><span class="sxs-lookup"><span data-stu-id="f6cc7-114">2</span></span>  <br/> | <span data-ttu-id="f6cc7-115">Right</span><span class="sxs-lookup"><span data-stu-id="f6cc7-115">Right</span></span>  <br/> |<span data-ttu-id="f6cc7-116">**Вистабстопригхт**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="f6cc7-117">4</span><span class="sxs-lookup"><span data-stu-id="f6cc7-117">3</span></span>  <br/> | <span data-ttu-id="f6cc7-118">Десятичное число</span><span class="sxs-lookup"><span data-stu-id="f6cc7-118">Decimal</span></span>  <br/> |<span data-ttu-id="f6cc7-119">**ВистабстопдеЦимал**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="f6cc7-120">SP4</span><span class="sxs-lookup"><span data-stu-id="f6cc7-120">4</span></span>  <br/> | <span data-ttu-id="f6cc7-121">Числ</span><span class="sxs-lookup"><span data-stu-id="f6cc7-121">Comma</span></span>  <br/> |<span data-ttu-id="f6cc7-122">**Вистабстопкомма**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6cc7-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6cc7-123">Remarks</span></span>

<span data-ttu-id="f6cc7-124">Чтобы получить ссылку на ячейку выравнивания по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6cc7-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-125">Cell name:</span></span>  <br/> | <span data-ttu-id="f6cc7-126">Знаков.</span><span class="sxs-lookup"><span data-stu-id="f6cc7-126">Tabs.</span></span>  <span data-ttu-id="f6cc7-127">*ИЖ* , где *i и j =* <1>, 2, 3</span><span class="sxs-lookup"><span data-stu-id="f6cc7-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="f6cc7-128">Чтобы получить ссылку на ячейку выравнивания по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6cc7-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-129">Section index:</span></span>  <br/> |<span data-ttu-id="f6cc7-130">**Виссектионтаб**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="f6cc7-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-131">Row index:</span></span>  <br/> |<span data-ttu-id="f6cc7-132">**висровтаб +** \*\* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f6cc7-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f6cc7-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6cc7-133">Cell index:</span></span>  <br/> | <span data-ttu-id="f6cc7-134">(*j* \* 3) **+ вистабалигн**</span><span class="sxs-lookup"><span data-stu-id="f6cc7-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

