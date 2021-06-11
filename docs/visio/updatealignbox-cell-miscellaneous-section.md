---
title: UpdateAlignBox Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1085
localization_priority: Normal
ms.assetid: 3e3f8dc9-203f-447d-9674-eb0be2d557d1
description: Пересчитывание прямоугольника выбора при перемещении ручки управления.
ms.openlocfilehash: 3b9d46b48002b6b3b1729df014fb0627a9c7f152
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414797"
---
# <a name="updatealignbox-cell-miscellaneous-section"></a><span data-ttu-id="508d5-103">UpdateAlignBox Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="508d5-103">UpdateAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="508d5-104">Пересчитывание прямоугольника выбора при перемещении ручки управления.</span><span class="sxs-lookup"><span data-stu-id="508d5-104">Recalculates the selection rectangle whenever a control handle is moved.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="508d5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="508d5-105">Remarks</span></span>

<span data-ttu-id="508d5-106">Чтобы получить ссылку на ячейку UpdateAlignBox по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="508d5-106">To get a reference to the UpdateAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="508d5-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="508d5-107">Cell name:</span></span>  <br/> | <span data-ttu-id="508d5-108">UpdateAlignBox</span><span class="sxs-lookup"><span data-stu-id="508d5-108">UpdateAlignBox</span></span>  <br/> |
   
<span data-ttu-id="508d5-109">Чтобы получить ссылку на ячейку UpdateAlignBox по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="508d5-109">To get a reference to the UpdateAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="508d5-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="508d5-110">Section index:</span></span>  <br/> |<span data-ttu-id="508d5-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="508d5-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="508d5-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="508d5-112">Row index:</span></span>  <br/> |<span data-ttu-id="508d5-113">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="508d5-113">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="508d5-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="508d5-114">Cell index:</span></span>  <br/> |<span data-ttu-id="508d5-115">**visUpdateAlignBox**</span><span class="sxs-lookup"><span data-stu-id="508d5-115">**visUpdateAlignBox**</span></span> <br/> |
   

