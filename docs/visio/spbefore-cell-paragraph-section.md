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
description: Определяет количество пробелов, вставленных перед каждым абзацем в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна, если это первый абзац в текстовом блоке, ячейка TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329885"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="97c66-103">SpBefore Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="97c66-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="97c66-104">Определяет количество пробелов, вставленных перед каждым абзацем в блоке текста фигуры, в дополнение к любому пробелу из ячейки сплайна, если это первый абзац в текстовом блоке, ячейка TopMargin.</span><span class="sxs-lookup"><span data-stu-id="97c66-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97c66-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97c66-105">Remarks</span></span>

<span data-ttu-id="97c66-106">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="97c66-106">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="97c66-107">Если масштаб документа изменяется, то параметр пробел до параметра остается прежним.</span><span class="sxs-lookup"><span data-stu-id="97c66-107">If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="97c66-108">Чтобы получить ссылку на ячейку "до" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="97c66-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c66-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="97c66-109">Cell name:</span></span>  <br/> | <span data-ttu-id="97c66-110">Para. @ перед [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="97c66-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="97c66-111">Чтобы получить ссылку на ячейку CellsSRC по индексу из программы, используйте свойство \*\*\*\* со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="97c66-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c66-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="97c66-112">Section index:</span></span>  <br/> |<span data-ttu-id="97c66-113">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="97c66-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="97c66-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="97c66-114">Row index:</span></span>  <br/> |<span data-ttu-id="97c66-115">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97c66-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97c66-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="97c66-116">Cell index:</span></span>  <br/> |<span data-ttu-id="97c66-117">**Висспацебефоре**</span><span class="sxs-lookup"><span data-stu-id="97c66-117">**visSpaceBefore**</span></span> <br/> |
   

