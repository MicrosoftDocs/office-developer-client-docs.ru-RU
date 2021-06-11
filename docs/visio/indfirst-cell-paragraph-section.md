---
title: IndFirst Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Представляет расстояние, на которое в текстовом блоке фигуры находится первая строка каждого абзаца, отступив от левого отступа абзаца. Это значение не зависит от масштаба рисунка. Если рисунок масштабироваться, отступ первой строки остается тем же.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410324"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="d2db4-105">IndFirst Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="d2db4-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="d2db4-106">Представляет расстояние, на которое в текстовом блоке фигуры находится первая строка каждого абзаца, отступив от левого отступа абзаца.</span><span class="sxs-lookup"><span data-stu-id="d2db4-106">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph.</span></span> <span data-ttu-id="d2db4-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="d2db4-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="d2db4-108">Если рисунок масштабироваться, отступ первой строки остается тем же.</span><span class="sxs-lookup"><span data-stu-id="d2db4-108">If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2db4-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2db4-109">Remarks</span></span>

<span data-ttu-id="d2db4-110">Чтобы получить ссылку на ячейку IndFirst по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d2db4-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2db4-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d2db4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="d2db4-112">Para.IndFirst[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d2db4-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2db4-113">Чтобы получить ссылку на ячейку IndFirst по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d2db4-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2db4-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d2db4-114">Section index:</span></span>  <br/> |<span data-ttu-id="d2db4-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="d2db4-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="d2db4-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d2db4-116">Row index:</span></span>  <br/> |<span data-ttu-id="d2db4-117">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="d2db4-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d2db4-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d2db4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d2db4-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="d2db4-119">**visIndentFirst**</span></span> <br/> |
   

