---
title: HAlign Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Определяет горизонтальное выравнивание текста в блоке текста фигуры.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360181"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="c588d-103">HAlign Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="c588d-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="c588d-104">Определяет горизонтальное выравнивание текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="c588d-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="c588d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="c588d-105">**Value**</span></span>|<span data-ttu-id="c588d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c588d-106">**Description**</span></span>|<span data-ttu-id="c588d-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c588d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c588d-108">нуль</span><span class="sxs-lookup"><span data-stu-id="c588d-108">0</span></span>  <br/> | <span data-ttu-id="c588d-109">Выравнивание по левому краю</span><span class="sxs-lookup"><span data-stu-id="c588d-109">Left align</span></span>  <br/> |<span data-ttu-id="c588d-110">**Вишорзлефт**</span><span class="sxs-lookup"><span data-stu-id="c588d-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="c588d-111">1,1</span><span class="sxs-lookup"><span data-stu-id="c588d-111">1</span></span>  <br/> | <span data-ttu-id="c588d-112">Center</span><span class="sxs-lookup"><span data-stu-id="c588d-112">Center</span></span>  <br/> |<span data-ttu-id="c588d-113">**Вишорзцентер**</span><span class="sxs-lookup"><span data-stu-id="c588d-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="c588d-114">2</span><span class="sxs-lookup"><span data-stu-id="c588d-114">2</span></span>  <br/> | <span data-ttu-id="c588d-115">Выравнивание по правому краю</span><span class="sxs-lookup"><span data-stu-id="c588d-115">Right align</span></span>  <br/> |<span data-ttu-id="c588d-116">**Вишорзригхт**</span><span class="sxs-lookup"><span data-stu-id="c588d-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="c588d-117">4</span><span class="sxs-lookup"><span data-stu-id="c588d-117">3</span></span>  <br/> | <span data-ttu-id="c588d-118">Justify</span><span class="sxs-lookup"><span data-stu-id="c588d-118">Justify</span></span>  <br/> |<span data-ttu-id="c588d-119">**Вишорзжустифи**</span><span class="sxs-lookup"><span data-stu-id="c588d-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="c588d-120">SP4</span><span class="sxs-lookup"><span data-stu-id="c588d-120">4</span></span>  <br/> | <span data-ttu-id="c588d-121">Принудительное выравнивание</span><span class="sxs-lookup"><span data-stu-id="c588d-121">Force justify</span></span>  <br/> |<span data-ttu-id="c588d-122">**Вишорзфорце**</span><span class="sxs-lookup"><span data-stu-id="c588d-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c588d-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="c588d-123">Remarks</span></span>

<span data-ttu-id="c588d-124">ВыРовнять по ширине пробелы между словами в каждой строке, кроме последней строки абзаца, чтобы выровнять левую и правую части текста по полям.</span><span class="sxs-lookup"><span data-stu-id="c588d-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="c588d-125">Принудительно выравнивает каждую строку в абзаце, в том числе последнюю.</span><span class="sxs-lookup"><span data-stu-id="c588d-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="c588d-126">Чтобы получить ссылку на ячейку HAlign по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c588d-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c588d-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c588d-127">Cell name:</span></span>  <br/> | <span data-ttu-id="c588d-128">Para. Хорзалигн [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c588d-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c588d-129">Чтобы получить ссылку на ячейку HAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c588d-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c588d-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c588d-130">Section index:</span></span>  <br/> |<span data-ttu-id="c588d-131">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="c588d-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c588d-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c588d-132">Row index:</span></span>  <br/> |<span data-ttu-id="c588d-133">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c588d-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c588d-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c588d-134">Cell index:</span></span>  <br/> |<span data-ttu-id="c588d-135">**Вишорзалигн**</span><span class="sxs-lookup"><span data-stu-id="c588d-135">**visHorzAlign**</span></span> <br/> |
   

