---
title: SpBefore Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Определяет объем пространства, вставляемого перед каждым абзацем в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine, если это первый абзац в текстовом блоке, ячейка TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425759"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="c9e9b-103">SpBefore Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="c9e9b-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="c9e9b-104">Определяет объем пространства, вставляемого перед каждым абзацем в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine, если это первый абзац в текстовом блоке, ячейка TopMargin.</span><span class="sxs-lookup"><span data-stu-id="c9e9b-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9e9b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9e9b-105">Remarks</span></span>

<span data-ttu-id="c9e9b-106">Это значение не зависит от масштаба рисования.</span><span class="sxs-lookup"><span data-stu-id="c9e9b-106">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="c9e9b-107">Если рисунок масштабировать, параметр "Пробел перед" остается тем же.</span><span class="sxs-lookup"><span data-stu-id="c9e9b-107">If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="c9e9b-108">Чтобы получить ссылку на ячейку SpBefore по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9e9b-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c9e9b-110">Para.SpBefore[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c9e9b-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c9e9b-111">Чтобы получить ссылку на ячейку SpBefore по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9e9b-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-112">Section index:</span></span>  <br/> |<span data-ttu-id="c9e9b-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="c9e9b-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="c9e9b-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-114">Row index:</span></span>  <br/> |<span data-ttu-id="c9e9b-115">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c9e9b-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c9e9b-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c9e9b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c9e9b-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="c9e9b-117">**visSpaceBefore**</span></span> <br/> |
   

