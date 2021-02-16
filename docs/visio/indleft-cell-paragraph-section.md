---
title: IndLeft Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Представляет расстояние, на которое все строки текста в абзаце отступят от левого поля текстового блока. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, отступ слева остается тем же.
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405165"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="b5636-105">IndLeft Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="b5636-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="b5636-106">Представляет расстояние, на которое все строки текста в абзаце отступят от левого поля текстового блока.</span><span class="sxs-lookup"><span data-stu-id="b5636-106">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block.</span></span> <span data-ttu-id="b5636-107">Это значение не зависит от масштаба рисования.</span><span class="sxs-lookup"><span data-stu-id="b5636-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="b5636-108">Если рисунок масштабировать, отступ слева остается тем же.</span><span class="sxs-lookup"><span data-stu-id="b5636-108">If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5636-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5636-109">Remarks</span></span>

<span data-ttu-id="b5636-110">Чтобы получить ссылку на ячейку IndLeft по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b5636-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5636-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b5636-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b5636-112">Para.IndLeft[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b5636-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b5636-113">Чтобы получить ссылку на ячейку IndLeft по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b5636-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5636-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b5636-114">Section index:</span></span>  <br/> |<span data-ttu-id="b5636-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="b5636-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="b5636-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b5636-116">Row index:</span></span>  <br/> |<span data-ttu-id="b5636-117">**visRowParagraph**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b5636-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b5636-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b5636-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b5636-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="b5636-119">**visIndentLeft**</span></span> <br/> |
   

