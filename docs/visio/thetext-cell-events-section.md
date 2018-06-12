---
title: Ячейка TheText (раздел событий)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Ячейка события, которое вычисляется при изменении текста или текста композиции фигуры.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815025"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="2a1d6-103">Ячейка TheText (раздел событий)</span><span class="sxs-lookup"><span data-stu-id="2a1d6-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="2a1d6-104">Ячейка события, которое вычисляется при изменении текста или текста композиции фигуры.</span><span class="sxs-lookup"><span data-stu-id="2a1d6-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a1d6-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a1d6-105">Remarks</span></span>

<span data-ttu-id="2a1d6-106">Событие ячеек вычисляются только в том случае, когда возникает событие, не после ввода формул.</span><span class="sxs-lookup"><span data-stu-id="2a1d6-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span> <span data-ttu-id="2a1d6-107">Можно использовать ячейку TheText для пересчета триггер, например для пересчета текст ширину и высоту с помощью функции (TEXTWIDTH) и TEXTHEIGHT ().</span><span class="sxs-lookup"><span data-stu-id="2a1d6-107">You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="2a1d6-108">Чтобы получить ссылку на ячейку TheText по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2a1d6-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a1d6-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2a1d6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2a1d6-110">TheText</span><span class="sxs-lookup"><span data-stu-id="2a1d6-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="2a1d6-111">Для получения ссылки на ячейки TheText по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2a1d6-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a1d6-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2a1d6-112">Section index:</span></span>  <br/> |<span data-ttu-id="2a1d6-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a1d6-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2a1d6-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2a1d6-114">Row index:</span></span>  <br/> |<span data-ttu-id="2a1d6-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="2a1d6-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="2a1d6-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2a1d6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2a1d6-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="2a1d6-117">**visEvtCellTheText**</span></span> <br/> |
   

