---
title: Ячейка SpLine (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Определяет расстояние между одну строку текста и следующим, выраженная в процентах, где 100% — высота строки текста.
ms.openlocfilehash: f2f290564d49a056bc3366707b25a7991f8c4401
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814926"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="cfa99-103">Ячейка SpLine (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="cfa99-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="cfa99-104">Определяет расстояние между одну строку текста и следующим, выраженная в процентах, где 100% — высота строки текста.</span><span class="sxs-lookup"><span data-stu-id="cfa99-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="cfa99-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="cfa99-105">**Value**</span></span>|<span data-ttu-id="cfa99-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cfa99-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cfa99-107">\>0</span><span class="sxs-lookup"><span data-stu-id="cfa99-107">\>0</span></span>  <br/> | <span data-ttu-id="cfa99-108">Абсолютный отступы, независимо от того, размер шрифта</span><span class="sxs-lookup"><span data-stu-id="cfa99-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="cfa99-109">= 0</span><span class="sxs-lookup"><span data-stu-id="cfa99-109">=0</span></span>  <br/> | <span data-ttu-id="cfa99-110">Задайте сплошной (интервал по = 100% от размера шрифта)</span><span class="sxs-lookup"><span data-stu-id="cfa99-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="cfa99-111">\<0</span><span class="sxs-lookup"><span data-stu-id="cfa99-111">\<0</span></span>  <br/> | <span data-ttu-id="cfa99-112">Процент от размера шрифта (, например-120% уступает интервал 120%)</span><span class="sxs-lookup"><span data-stu-id="cfa99-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfa99-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="cfa99-113">Remarks</span></span>

<span data-ttu-id="cfa99-114">Для получения ссылки на ячейки сплайн по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cfa99-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cfa99-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cfa99-115">Cell name:</span></span>  <br/> | <span data-ttu-id="cfa99-116">Абзац.</span><span class="sxs-lookup"><span data-stu-id="cfa99-116">Para.</span></span> <span data-ttu-id="cfa99-117">Сплайн [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cfa99-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cfa99-118">Для получения ссылки на ячейки сплайн по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cfa99-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cfa99-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cfa99-119">Section index:</span></span>  <br/> |<span data-ttu-id="cfa99-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="cfa99-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="cfa99-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cfa99-121">Row index:</span></span>  <br/> |<span data-ttu-id="cfa99-122">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cfa99-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cfa99-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cfa99-123">Cell index:</span></span>  <br/> |<span data-ttu-id="cfa99-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="cfa99-124">**visSpaceLine**</span></span> <br/> |
   

