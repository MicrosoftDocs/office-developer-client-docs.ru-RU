---
title: TheText Cell (Events Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Ячейка события, которая оценивается при смене текста или текстовой композиции фигуры.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435168"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="6b3cf-103">TheText Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="6b3cf-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="6b3cf-104">Ячейка события, которая оценивается при смене текста или текстовой композиции фигуры.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b3cf-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b3cf-105">Remarks</span></span>

<span data-ttu-id="6b3cf-106">Ячейки событий оцениваются только при событии, а не при вводе формулы.</span><span class="sxs-lookup"><span data-stu-id="6b3cf-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span> <span data-ttu-id="6b3cf-107">Ячейку TheText можно использовать для запуска пересчета, например для пересчета ширины и высоты текста с помощью функций TEXTWIDTH( ) и TEXTHEIGHT( ).</span><span class="sxs-lookup"><span data-stu-id="6b3cf-107">You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="6b3cf-108">Чтобы получить ссылку на ячейку TheText по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b3cf-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6b3cf-110">TheText</span><span class="sxs-lookup"><span data-stu-id="6b3cf-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="6b3cf-111">Чтобы получить ссылку на ячейку TheText по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b3cf-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-112">Section index:</span></span>  <br/> |<span data-ttu-id="6b3cf-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b3cf-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b3cf-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-114">Row index:</span></span>  <br/> |<span data-ttu-id="6b3cf-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="6b3cf-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="6b3cf-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6b3cf-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6b3cf-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="6b3cf-117">**visEvtCellTheText**</span></span> <br/> |
   

