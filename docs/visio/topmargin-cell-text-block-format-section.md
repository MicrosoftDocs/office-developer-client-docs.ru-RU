---
title: TopMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: Определяет расстояние между верхней границей блока текста и первой строкой текста, который он содержит. Значение по умолчанию — 4,0000 пт. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, верхнее поле остается прежним.
ms.openlocfilehash: 97d349fd4ddc3c76cda61e1ee7ce25909161e6fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435574"
---
# <a name="topmargin-cell-text-block-format-section"></a><span data-ttu-id="c01ef-106">TopMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="c01ef-106">TopMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="c01ef-107">Определяет расстояние между верхней границей блока текста и первой строкой текста, который он содержит.</span><span class="sxs-lookup"><span data-stu-id="c01ef-107">Determines the distance between the top border of the text block and the first line of text it contains.</span></span> <span data-ttu-id="c01ef-108">Значение по умолчанию — 4,0000 пт.</span><span class="sxs-lookup"><span data-stu-id="c01ef-108">The default is 4.0000 point.</span></span> <span data-ttu-id="c01ef-109">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="c01ef-109">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="c01ef-110">Если масштаб документа изменяется, верхнее поле остается прежним.</span><span class="sxs-lookup"><span data-stu-id="c01ef-110">If the drawing is scaled, the top margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c01ef-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c01ef-111">Remarks</span></span>

<span data-ttu-id="c01ef-112">Чтобы получить ссылку на ячейку TopMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="c01ef-112">To get a reference to the TopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c01ef-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c01ef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c01ef-114">TopMargin</span><span class="sxs-lookup"><span data-stu-id="c01ef-114">TopMargin</span></span>  <br/> |
   
<span data-ttu-id="c01ef-115">Чтобы получить ссылку на ячейку TopMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c01ef-115">To get a reference to the TopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c01ef-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c01ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="c01ef-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c01ef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c01ef-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c01ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="c01ef-119">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="c01ef-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="c01ef-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c01ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c01ef-121">**Висткстблктопмаргин**</span><span class="sxs-lookup"><span data-stu-id="c01ef-121">**visTxtBlkTopMargin**</span></span> <br/> |
   

