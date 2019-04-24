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
description: Представляет расстояние отступа первой строки каждого абзаца в блоке текста фигуры слева от левого отступа абзаца. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ первой строки остается прежним.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335359"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="6428d-105">IndFirst Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="6428d-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="6428d-106">Представляет расстояние отступа первой строки каждого абзаца в блоке текста фигуры слева от левого отступа абзаца.</span><span class="sxs-lookup"><span data-stu-id="6428d-106">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph.</span></span> <span data-ttu-id="6428d-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="6428d-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="6428d-108">Если масштаб документа изменяется, отступ первой строки остается прежним.</span><span class="sxs-lookup"><span data-stu-id="6428d-108">If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6428d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6428d-109">Remarks</span></span>

<span data-ttu-id="6428d-110">Чтобы получить ссылку на ячейку Индфирст по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6428d-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6428d-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6428d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="6428d-112">Para. Индфирст [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6428d-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6428d-113">Чтобы получить ссылку на ячейку Индфирст по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6428d-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6428d-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6428d-114">Section index:</span></span>  <br/> |<span data-ttu-id="6428d-115">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="6428d-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="6428d-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6428d-116">Row index:</span></span>  <br/> |<span data-ttu-id="6428d-117">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6428d-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6428d-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6428d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6428d-119">**Висиндентфирст**</span><span class="sxs-lookup"><span data-stu-id="6428d-119">**visIndentFirst**</span></span> <br/> |
   

