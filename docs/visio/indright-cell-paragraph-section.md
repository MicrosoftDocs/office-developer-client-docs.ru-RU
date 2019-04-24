---
title: IndRight Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Представляет расстояние для всех строк текста в абзаце с отступом от правого поля блока текста. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, отступ справа остается прежним.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335345"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="dccd0-105">IndRight Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="dccd0-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="dccd0-106">Представляет расстояние для всех строк текста в абзаце с отступом от правого поля блока текста.</span><span class="sxs-lookup"><span data-stu-id="dccd0-106">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block.</span></span> <span data-ttu-id="dccd0-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="dccd0-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="dccd0-108">Если масштаб документа изменяется, отступ справа остается прежним.</span><span class="sxs-lookup"><span data-stu-id="dccd0-108">If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dccd0-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dccd0-109">Remarks</span></span>

<span data-ttu-id="dccd0-110">Чтобы получить ссылку на ячейку IndRight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dccd0-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dccd0-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dccd0-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dccd0-112">Para. IndRight [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dccd0-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dccd0-113">Чтобы получить ссылку на ячейку IndRight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dccd0-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dccd0-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dccd0-114">Section index:</span></span>  <br/> |<span data-ttu-id="dccd0-115">**Виссектионпараграф**</span><span class="sxs-lookup"><span data-stu-id="dccd0-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="dccd0-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dccd0-116">Row index:</span></span>  <br/> |<span data-ttu-id="dccd0-117">**висровпараграф** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dccd0-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dccd0-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dccd0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dccd0-119">**Висиндентригхт**</span><span class="sxs-lookup"><span data-stu-id="dccd0-119">**visIndentRight**</span></span> <br/> |
   

