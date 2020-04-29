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
description: Определяет расстояние между левой границей блока текста и содержащимся в нем текстом. Значение по умолчанию 0,1 дюйма. Это значение не зависит от масштаба рисунка. Если масштаб документа изменяется, левое поле остается прежним.
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411339"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="58d35-106">LeftMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="58d35-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="58d35-107">Определяет расстояние между левой границей блока текста и содержащимся в нем текстом.</span><span class="sxs-lookup"><span data-stu-id="58d35-107">Determines the distance between the left border of the text block and the text it contains.</span></span> <span data-ttu-id="58d35-108">Значение по умолчанию 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="58d35-108">The default is 0.1 inch.</span></span> <span data-ttu-id="58d35-109">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="58d35-109">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="58d35-110">Если масштаб документа изменяется, левое поле остается прежним.</span><span class="sxs-lookup"><span data-stu-id="58d35-110">If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58d35-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="58d35-111">Remarks</span></span>

<span data-ttu-id="58d35-112">Чтобы получить ссылку на ячейку LeftMargin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="58d35-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58d35-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="58d35-113">Cell name:</span></span>  <br/> | <span data-ttu-id="58d35-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="58d35-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="58d35-115">Чтобы получить ссылку на ячейку LeftMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="58d35-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58d35-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="58d35-116">Section index:</span></span>  <br/> |<span data-ttu-id="58d35-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58d35-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58d35-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="58d35-118">Row index:</span></span>  <br/> |<span data-ttu-id="58d35-119">**висровтекст**</span><span class="sxs-lookup"><span data-stu-id="58d35-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="58d35-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="58d35-120">Cell index:</span></span>  <br/> |<span data-ttu-id="58d35-121">**висткстблклефтмаргин**</span><span class="sxs-lookup"><span data-stu-id="58d35-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

