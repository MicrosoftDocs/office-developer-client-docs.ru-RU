---
title: Выравнивание ячейки (вкладки раздел)
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
# <a name="alignment-cell-tabs-section"></a><span data-ttu-id="096b8-103">Выравнивание ячейки (вкладки раздел)</span><span class="sxs-lookup"><span data-stu-id="096b8-103">Alignment Cell (Tabs Section)</span></span>

<span data-ttu-id="096b8-104">Задает выравнивание табуляции.</span><span class="sxs-lookup"><span data-stu-id="096b8-104">Specifies the tab alignment.</span></span>
  
|<span data-ttu-id="096b8-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="096b8-105">**Value**</span></span>|<span data-ttu-id="096b8-106">**Выравнивание**</span><span class="sxs-lookup"><span data-stu-id="096b8-106">**Alignment**</span></span>|<span data-ttu-id="096b8-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="096b8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="096b8-108">0</span><span class="sxs-lookup"><span data-stu-id="096b8-108">0</span></span>  <br/> | <span data-ttu-id="096b8-109">Слева</span><span class="sxs-lookup"><span data-stu-id="096b8-109">Left</span></span>  <br/> |<span data-ttu-id="096b8-110">**visTabStopLeft**</span><span class="sxs-lookup"><span data-stu-id="096b8-110">**visTabStopLeft**</span></span> <br/> |
| <span data-ttu-id="096b8-111">1</span><span class="sxs-lookup"><span data-stu-id="096b8-111">1</span></span>  <br/> | <span data-ttu-id="096b8-112">Центр</span><span class="sxs-lookup"><span data-stu-id="096b8-112">Center</span></span>  <br/> |<span data-ttu-id="096b8-113">**visTabStopCenter**</span><span class="sxs-lookup"><span data-stu-id="096b8-113">**visTabStopCenter**</span></span> <br/> |
| <span data-ttu-id="096b8-114">2</span><span class="sxs-lookup"><span data-stu-id="096b8-114">2</span></span>  <br/> | <span data-ttu-id="096b8-115">Правильно</span><span class="sxs-lookup"><span data-stu-id="096b8-115">Right</span></span>  <br/> |<span data-ttu-id="096b8-116">**visTabStopRight**</span><span class="sxs-lookup"><span data-stu-id="096b8-116">**visTabStopRight**</span></span> <br/> |
| <span data-ttu-id="096b8-117">3</span><span class="sxs-lookup"><span data-stu-id="096b8-117">3</span></span>  <br/> | <span data-ttu-id="096b8-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="096b8-118">Decimal</span></span>  <br/> |<span data-ttu-id="096b8-119">**visTabStopDecimal**</span><span class="sxs-lookup"><span data-stu-id="096b8-119">**visTabStopDecimal**</span></span> <br/> |
| <span data-ttu-id="096b8-120">4</span><span class="sxs-lookup"><span data-stu-id="096b8-120">4</span></span>  <br/> | <span data-ttu-id="096b8-121">Разделители</span><span class="sxs-lookup"><span data-stu-id="096b8-121">Comma</span></span>  <br/> |<span data-ttu-id="096b8-122">**visTabStopComma**</span><span class="sxs-lookup"><span data-stu-id="096b8-122">**visTabStopComma**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="096b8-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="096b8-123">Remarks</span></span>

<span data-ttu-id="096b8-124">Для получения ссылки на ячейки выравнивание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="096b8-124">To get a reference to the Alignment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="096b8-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="096b8-125">Cell name:</span></span>  <br/> | <span data-ttu-id="096b8-126">Вкладки.</span><span class="sxs-lookup"><span data-stu-id="096b8-126">Tabs.</span></span>  <span data-ttu-id="096b8-127">*ij* где *i и j =* < 1 > 2, 3</span><span class="sxs-lookup"><span data-stu-id="096b8-127">*ij*            where  *i and j =*  <1>, 2, 3</span></span>  <br/> |
   
<span data-ttu-id="096b8-128">Для получения ссылки на ячейки выравнивание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="096b8-128">To get a reference to the Alignment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="096b8-129">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="096b8-129">Section index:</span></span>  <br/> |<span data-ttu-id="096b8-130">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="096b8-130">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="096b8-131">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="096b8-131">Row index:</span></span>  <br/> |<span data-ttu-id="096b8-132">**visRowTab +** *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="096b8-132">**visRowTab +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="096b8-133">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="096b8-133">Cell index:</span></span>  <br/> | <span data-ttu-id="096b8-134">(*j* \* 3) **+ visTabAlign**</span><span class="sxs-lookup"><span data-stu-id="096b8-134">(*j*  \*3) **+ visTabAlign**</span></span> <br/> |
   

