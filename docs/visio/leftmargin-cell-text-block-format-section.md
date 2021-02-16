---
title: LeftMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Определяет расстояние между левой границей текстового блока и текстом, который он содержит. Значение по умолчанию — 0,1 дюйма. Это значение не зависит от масштаба рисования. При масштабе рисования левое поле остается таким же.
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411339"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="987c7-106">LeftMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="987c7-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="987c7-107">Определяет расстояние между левой границей текстового блока и текстом, который он содержит.</span><span class="sxs-lookup"><span data-stu-id="987c7-107">Determines the distance between the left border of the text block and the text it contains.</span></span> <span data-ttu-id="987c7-108">Значение по умолчанию — 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="987c7-108">The default is 0.1 inch.</span></span> <span data-ttu-id="987c7-109">Это значение не зависит от масштаба рисования.</span><span class="sxs-lookup"><span data-stu-id="987c7-109">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="987c7-110">При масштабе рисования левое поле остается таким же.</span><span class="sxs-lookup"><span data-stu-id="987c7-110">If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="987c7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="987c7-111">Remarks</span></span>

<span data-ttu-id="987c7-112">Чтобы получить ссылку на ячейку LeftMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="987c7-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="987c7-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="987c7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="987c7-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="987c7-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="987c7-115">Чтобы получить ссылку на ячейку LeftMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="987c7-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="987c7-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="987c7-116">Section index:</span></span>  <br/> |<span data-ttu-id="987c7-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="987c7-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="987c7-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="987c7-118">Row index:</span></span>  <br/> |<span data-ttu-id="987c7-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="987c7-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="987c7-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="987c7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="987c7-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="987c7-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

