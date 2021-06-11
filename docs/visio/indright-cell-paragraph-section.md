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
description: Представляет расстояние, на которое все строки текста в абзаце отступили от правой границы текстового блока. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, правый отступ остается тем же.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408868"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="fd8aa-105">IndRight Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="fd8aa-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="fd8aa-106">Представляет расстояние, на которое все строки текста в абзаце отступили от правой границы текстового блока.</span><span class="sxs-lookup"><span data-stu-id="fd8aa-106">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block.</span></span> <span data-ttu-id="fd8aa-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="fd8aa-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="fd8aa-108">Если рисунок масштабировать, правый отступ остается тем же.</span><span class="sxs-lookup"><span data-stu-id="fd8aa-108">If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd8aa-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd8aa-109">Remarks</span></span>

<span data-ttu-id="fd8aa-110">Чтобы получить ссылку на ячейку IndRight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd8aa-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fd8aa-112">Para.IndRight[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fd8aa-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fd8aa-113">Чтобы получить ссылку на ячейку IndRight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd8aa-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-114">Section index:</span></span>  <br/> |<span data-ttu-id="fd8aa-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="fd8aa-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="fd8aa-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-116">Row index:</span></span>  <br/> |<span data-ttu-id="fd8aa-117">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="fd8aa-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fd8aa-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fd8aa-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fd8aa-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="fd8aa-119">**visIndentRight**</span></span> <br/> |
   

