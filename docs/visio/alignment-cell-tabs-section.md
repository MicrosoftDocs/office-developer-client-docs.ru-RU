---
title: Ячейка Alignment (раздел "Вкладки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: Задает выравнивание табуляции.
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813139"
---
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="6d0f1-103">Ячейка Alignment (раздел "Вкладки")</span><span class="sxs-lookup"><span data-stu-id="6d0f1-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="6d0f1-104">Задает выравнивание табуляции.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="6d0f1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-105">**Value**</span></span>|<span data-ttu-id="6d0f1-106">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-106">**Alignment**</span></span>|<span data-ttu-id="6d0f1-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6d0f1-108">0</span><span class="sxs-lookup"><span data-stu-id="6d0f1-108">0</span></span>  <br/> | <span data-ttu-id="6d0f1-109">Left</span><span class="sxs-lookup"><span data-stu-id="6d0f1-109">Left</span></span>  <br/> |<span data-ttu-id="6d0f1-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="6d0f1-111">1</span><span class="sxs-lookup"><span data-stu-id="6d0f1-111">1</span></span>  <br/> | <span data-ttu-id="6d0f1-112">Center</span><span class="sxs-lookup"><span data-stu-id="6d0f1-112">Center</span></span>  <br/> |<span data-ttu-id="6d0f1-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="6d0f1-114">2</span><span class="sxs-lookup"><span data-stu-id="6d0f1-114">2</span></span>  <br/> | <span data-ttu-id="6d0f1-115">Right</span><span class="sxs-lookup"><span data-stu-id="6d0f1-115">Right</span></span>  <br/> |<span data-ttu-id="6d0f1-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="6d0f1-117">3</span><span class="sxs-lookup"><span data-stu-id="6d0f1-117">3</span></span>  <br/> | <span data-ttu-id="6d0f1-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="6d0f1-118">Decimal</span></span>  <br/> |<span data-ttu-id="6d0f1-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="6d0f1-120">4</span><span class="sxs-lookup"><span data-stu-id="6d0f1-120">4</span></span>  <br/> | <span data-ttu-id="6d0f1-121">Разделители</span><span class="sxs-lookup"><span data-stu-id="6d0f1-121">Comma</span></span>  <br/> |<span data-ttu-id="6d0f1-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d0f1-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d0f1-123">Remarks</span></span>

<span data-ttu-id="6d0f1-124">Для получения ссылки на ячейки выравнивание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6d0f1-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d0f1-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-125">Cell name:</span></span>  <br/> | <span data-ttu-id="6d0f1-126">Вкладки.</span><span class="sxs-lookup"><span data-stu-id="6d0f1-126">Tabs.</span></span>  <span data-ttu-id="6d0f1-127">*ij* где *i и j =* < 1 > 2, 3</span><span class="sxs-lookup"><span data-stu-id="6d0f1-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="6d0f1-128">Для получения ссылки на ячейки выравнивание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6d0f1-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d0f1-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6d0f1-129">Section index:</span></span>  <br/> |<span data-ttu-id="6d0f1-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="6d0f1-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6d0f1-131">Row index:</span></span>  <br/> |<span data-ttu-id="6d0f1-132">**visRowTab +** *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d0f1-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d0f1-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6d0f1-133">Cell index:</span></span>  <br/> | <span data-ttu-id="6d0f1-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="6d0f1-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

