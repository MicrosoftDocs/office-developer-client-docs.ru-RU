---
title: SpLine Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Определяет расстояние между одной строкой текста и следующим, выраженное в процентном выражении, где 100% — высота строки текста.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434916"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="e07dd-103">SpLine Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="e07dd-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="e07dd-104">Определяет расстояние между одной строкой текста и следующим, выраженное в процентном выражении, где 100% — высота строки текста.</span><span class="sxs-lookup"><span data-stu-id="e07dd-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="e07dd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e07dd-105">**Value**</span></span>|<span data-ttu-id="e07dd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e07dd-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e07dd-107">\>нуль</span><span class="sxs-lookup"><span data-stu-id="e07dd-107">\>0</span></span>  <br/> | <span data-ttu-id="e07dd-108">Абсолютные интервалы, независимо от размера шрифта</span><span class="sxs-lookup"><span data-stu-id="e07dd-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="e07dd-109">= 0</span><span class="sxs-lookup"><span data-stu-id="e07dd-109">=0</span></span>  <br/> | <span data-ttu-id="e07dd-110">Задать сплошной (интервал = 100% размера шрифта)</span><span class="sxs-lookup"><span data-stu-id="e07dd-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="e07dd-111">\<нуль</span><span class="sxs-lookup"><span data-stu-id="e07dd-111">\<0</span></span>  <br/> | <span data-ttu-id="e07dd-112">Процент размера шрифта (например,-120% дает 120% интервал)</span><span class="sxs-lookup"><span data-stu-id="e07dd-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e07dd-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e07dd-113">Remarks</span></span>

<span data-ttu-id="e07dd-114">Чтобы получить ссылку на ячейку сплайна по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e07dd-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e07dd-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e07dd-115">Cell name:</span></span>  <br/> | <span data-ttu-id="e07dd-116">Para.</span><span class="sxs-lookup"><span data-stu-id="e07dd-116">Para.</span></span> <span data-ttu-id="e07dd-117">Сплайн [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e07dd-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e07dd-118">Чтобы получить ссылку на ячейку сплайна по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e07dd-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e07dd-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e07dd-119">Section index:</span></span>  <br/> |<span data-ttu-id="e07dd-120">**виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="e07dd-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="e07dd-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e07dd-121">Row index:</span></span>  <br/> |<span data-ttu-id="e07dd-122">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e07dd-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e07dd-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e07dd-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e07dd-124">**висспацелине**</span><span class="sxs-lookup"><span data-stu-id="e07dd-124">**visSpaceLine**</span></span> <br/> |
   

