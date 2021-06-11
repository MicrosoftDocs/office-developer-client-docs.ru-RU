---
title: SortKey Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Номер, определяя порядок гиперссылки, которые отображаются в меню ярлыков.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406383"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="c88e5-103">SortKey Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="c88e5-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="c88e5-104">Номер, определяя порядок гиперссылки, которые отображаются в меню ярлыков.</span><span class="sxs-lookup"><span data-stu-id="c88e5-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c88e5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="c88e5-105">Remarks</span></span>

<span data-ttu-id="c88e5-106">Гиперссылки в меню ярлыка отображаются в меню, отсортировали от самого низкого до самого высокого, а в верхней части меню отображаются более низкие числа.</span><span class="sxs-lookup"><span data-stu-id="c88e5-106">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu.</span></span> <span data-ttu-id="c88e5-107">Если две строки гиперссылки имеют одинаковое значение ячейки SortKey, порядок определяется физическим порядком строки.</span><span class="sxs-lookup"><span data-stu-id="c88e5-107">If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order.</span></span> <span data-ttu-id="c88e5-108">По умолчанию значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="c88e5-108">The default is 0 (zero).</span></span> 
  
<span data-ttu-id="c88e5-109">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c88e5-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c88e5-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c88e5-110">Cell name:</span></span>  <br/> |<span data-ttu-id="c88e5-111">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="c88e5-111">Hyperlink.</span></span> <span data-ttu-id="c88e5-112">*имя*  . SortKey, где  *Hyperlink .name*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="c88e5-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c88e5-113">Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c88e5-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c88e5-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c88e5-114">Section index:</span></span>  <br/> |<span data-ttu-id="c88e5-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="c88e5-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="c88e5-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c88e5-116">Row index:</span></span>  <br/> |<span data-ttu-id="c88e5-117">**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="c88e5-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c88e5-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c88e5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c88e5-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="c88e5-119">**visHLinkSortKey**</span></span> <br/> |
   

