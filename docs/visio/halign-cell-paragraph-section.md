---
title: Ячейка HAlign (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Определяет горизонтальное выравнивание текста в блоке текста фигуры.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813893"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="8a3fa-103">Ячейка HAlign (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="8a3fa-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="8a3fa-104">Определяет горизонтальное выравнивание текста в блоке текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="8a3fa-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="8a3fa-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-105">**Value**</span></span>|<span data-ttu-id="8a3fa-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-106">**Description**</span></span>|<span data-ttu-id="8a3fa-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8a3fa-108">0</span><span class="sxs-lookup"><span data-stu-id="8a3fa-108">0</span></span>  <br/> | <span data-ttu-id="8a3fa-109">Выравнивание по левому краю</span><span class="sxs-lookup"><span data-stu-id="8a3fa-109">Left align</span></span>  <br/> |<span data-ttu-id="8a3fa-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="8a3fa-111">1</span><span class="sxs-lookup"><span data-stu-id="8a3fa-111">1</span></span>  <br/> | <span data-ttu-id="8a3fa-112">Center</span><span class="sxs-lookup"><span data-stu-id="8a3fa-112">Center</span></span>  <br/> |<span data-ttu-id="8a3fa-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="8a3fa-114">2</span><span class="sxs-lookup"><span data-stu-id="8a3fa-114">2</span></span>  <br/> | <span data-ttu-id="8a3fa-115">По правому краю</span><span class="sxs-lookup"><span data-stu-id="8a3fa-115">Right align</span></span>  <br/> |<span data-ttu-id="8a3fa-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="8a3fa-117">3</span><span class="sxs-lookup"><span data-stu-id="8a3fa-117">3</span></span>  <br/> | <span data-ttu-id="8a3fa-118">Выравнивание</span><span class="sxs-lookup"><span data-stu-id="8a3fa-118">Justify</span></span>  <br/> |<span data-ttu-id="8a3fa-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="8a3fa-120">4</span><span class="sxs-lookup"><span data-stu-id="8a3fa-120">4</span></span>  <br/> | <span data-ttu-id="8a3fa-121">Выровнять force</span><span class="sxs-lookup"><span data-stu-id="8a3fa-121">Force justify</span></span>  <br/> |<span data-ttu-id="8a3fa-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a3fa-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a3fa-123">Remarks</span></span>

<span data-ttu-id="8a3fa-124">Выровнять интервала между слов в каждой строки, кроме последней строки абзаца для выравнивания как слева и справа от текста с помощью поля.</span><span class="sxs-lookup"><span data-stu-id="8a3fa-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="8a3fa-125">Выровнять force выравнивает каждой строки в абзаце, включая последний.</span><span class="sxs-lookup"><span data-stu-id="8a3fa-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="8a3fa-126">Чтобы получить ссылку на ячейку HAlign по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8a3fa-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a3fa-127">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8a3fa-127">Cell name:</span></span>  <br/> | <span data-ttu-id="8a3fa-128">Para.HorzAlign [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8a3fa-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8a3fa-129">Для получения ссылки на ячейки HAlign по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8a3fa-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a3fa-130">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8a3fa-130">Section index:</span></span>  <br/> |<span data-ttu-id="8a3fa-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8a3fa-132">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8a3fa-132">Row index:</span></span>  <br/> |<span data-ttu-id="8a3fa-133">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8a3fa-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8a3fa-134">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8a3fa-134">Cell index:</span></span>  <br/> |<span data-ttu-id="8a3fa-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="8a3fa-135">**visHorzAlign**</span></span> <br/> |
   

