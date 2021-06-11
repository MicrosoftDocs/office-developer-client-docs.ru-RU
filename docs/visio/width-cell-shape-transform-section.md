---
title: Width Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Содержит ширину выбранной фигуры в единицах рисования. Формула по умолчанию для определения ширины формы 1-D:'
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415196"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="ed2d8-104">Width Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="ed2d8-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="ed2d8-105">Содержит ширину выбранной фигуры в единицах рисования.</span><span class="sxs-lookup"><span data-stu-id="ed2d8-105">Contains the width of the selected shape in drawing units.</span></span> <span data-ttu-id="ed2d8-106">Формула по умолчанию для определения ширины формы 1-D:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-106">The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="ed2d8-107">= SQRT((EndX - BeginX) ^ 2 + (Endy - Beginy) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="ed2d8-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed2d8-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed2d8-108">Remarks</span></span>

<span data-ttu-id="ed2d8-109">Чтобы получить ссылку на ячейку Width по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed2d8-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="ed2d8-111">Width</span><span class="sxs-lookup"><span data-stu-id="ed2d8-111">Width</span></span>  <br/> |
   
<span data-ttu-id="ed2d8-112">Чтобы получить ссылку на ячейку Ширина по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed2d8-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-113">Section index:</span></span>  <br/> |<span data-ttu-id="ed2d8-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed2d8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed2d8-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-115">Row index:</span></span>  <br/> |<span data-ttu-id="ed2d8-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="ed2d8-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="ed2d8-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed2d8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="ed2d8-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="ed2d8-118">**visXFormWidth**</span></span> <br/> |
   

