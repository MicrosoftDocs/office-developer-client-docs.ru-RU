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
description: Ячейка события, вычисляемая при изменении текста фигуры или текстовой композиции.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435168"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="5d255-103">TheText Cell (Events Section)</span><span class="sxs-lookup"><span data-stu-id="5d255-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="5d255-104">Ячейка события, вычисляемая при изменении текста фигуры или текстовой композиции.</span><span class="sxs-lookup"><span data-stu-id="5d255-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d255-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d255-105">Remarks</span></span>

<span data-ttu-id="5d255-106">Ячейки событий оцениваются только при возникновении события, а не при вводе формул.</span><span class="sxs-lookup"><span data-stu-id="5d255-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span> <span data-ttu-id="5d255-107">Вы можете использовать ячейку TheText для запуска пересчета, например для пересчета ширины и высоты текста с помощью функций TEXTWIDTH () и TEXTHEIGHT ().</span><span class="sxs-lookup"><span data-stu-id="5d255-107">You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="5d255-108">Чтобы получить ссылку на ячейку TheText по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5d255-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d255-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5d255-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5d255-110">TheText</span><span class="sxs-lookup"><span data-stu-id="5d255-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="5d255-111">Чтобы получить ссылку на ячейку TheText по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5d255-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d255-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5d255-112">Section index:</span></span>  <br/> |<span data-ttu-id="5d255-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d255-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5d255-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5d255-114">Row index:</span></span>  <br/> |<span data-ttu-id="5d255-115">**висровевент**</span><span class="sxs-lookup"><span data-stu-id="5d255-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="5d255-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5d255-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5d255-117">**висевтцеллсетекст**</span><span class="sxs-lookup"><span data-stu-id="5d255-117">**visEvtCellTheText**</span></span> <br/> |
   

