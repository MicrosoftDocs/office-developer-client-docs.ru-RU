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
description: Определяет горизонтальное выравнивание текста в текстовом блоке фигуры.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414741"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="4286a-103">HAlign Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="4286a-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="4286a-104">Определяет горизонтальное выравнивание текста в текстовом блоке фигуры.</span><span class="sxs-lookup"><span data-stu-id="4286a-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="4286a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4286a-105">**Value**</span></span>|<span data-ttu-id="4286a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4286a-106">**Description**</span></span>|<span data-ttu-id="4286a-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="4286a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4286a-108">0</span><span class="sxs-lookup"><span data-stu-id="4286a-108">0</span></span>  <br/> | <span data-ttu-id="4286a-109">Выравнивание по левую</span><span class="sxs-lookup"><span data-stu-id="4286a-109">Left align</span></span>  <br/> |<span data-ttu-id="4286a-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="4286a-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="4286a-111">1 </span><span class="sxs-lookup"><span data-stu-id="4286a-111">1</span></span>  <br/> | <span data-ttu-id="4286a-112">Center</span><span class="sxs-lookup"><span data-stu-id="4286a-112">Center</span></span>  <br/> |<span data-ttu-id="4286a-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="4286a-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="4286a-114">2 </span><span class="sxs-lookup"><span data-stu-id="4286a-114">2</span></span>  <br/> | <span data-ttu-id="4286a-115">Выравнивание по правому направлению</span><span class="sxs-lookup"><span data-stu-id="4286a-115">Right align</span></span>  <br/> |<span data-ttu-id="4286a-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="4286a-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="4286a-117">3 </span><span class="sxs-lookup"><span data-stu-id="4286a-117">3</span></span>  <br/> | <span data-ttu-id="4286a-118">Justify</span><span class="sxs-lookup"><span data-stu-id="4286a-118">Justify</span></span>  <br/> |<span data-ttu-id="4286a-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="4286a-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="4286a-120">4 </span><span class="sxs-lookup"><span data-stu-id="4286a-120">4</span></span>  <br/> | <span data-ttu-id="4286a-121">Принудительное обоснование</span><span class="sxs-lookup"><span data-stu-id="4286a-121">Force justify</span></span>  <br/> |<span data-ttu-id="4286a-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="4286a-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4286a-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="4286a-123">Remarks</span></span>

<span data-ttu-id="4286a-124">Justify добавляет пробел между словами в каждой строке, кроме последней строки абзаца, чтобы выровнять левую и правую части текста с полями.</span><span class="sxs-lookup"><span data-stu-id="4286a-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="4286a-125">Принудительное обоснование обустроит каждую строку абзаца, включая последнюю.</span><span class="sxs-lookup"><span data-stu-id="4286a-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="4286a-126">Чтобы получить ссылку на ячейку HAlign по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4286a-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4286a-127">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4286a-127">Cell name:</span></span>  <br/> | <span data-ttu-id="4286a-128">Para.HorzAlign[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4286a-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4286a-129">Чтобы получить ссылку на ячейку HAlign по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4286a-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4286a-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4286a-130">Section index:</span></span>  <br/> |<span data-ttu-id="4286a-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="4286a-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="4286a-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4286a-132">Row index:</span></span>  <br/> |<span data-ttu-id="4286a-133">**visRowParagraph**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4286a-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4286a-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4286a-134">Cell index:</span></span>  <br/> |<span data-ttu-id="4286a-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="4286a-135">**visHorzAlign**</span></span> <br/> |
   

