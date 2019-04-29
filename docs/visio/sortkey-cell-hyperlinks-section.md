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
description: Число, определяющее порядок гиперссылок в контекстном меню.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406383"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="d1730-103">SortKey Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="d1730-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="d1730-104">Число, определяющее порядок гиперссылок в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="d1730-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1730-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1730-105">Remarks</span></span>

<span data-ttu-id="d1730-106">Гиперссылки в контекстном меню отображаются в меню, отсортированном от самого низкого до более высокого, с меньшими номерами в верхней части меню.</span><span class="sxs-lookup"><span data-stu-id="d1730-106">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu.</span></span> <span data-ttu-id="d1730-107">Если две строки гиперссылок имеют одинаковое значение ячейки SortKey, порядок определяется физическим порядком строк.</span><span class="sxs-lookup"><span data-stu-id="d1730-107">If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order.</span></span> <span data-ttu-id="d1730-108">Значение по умолчанию — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="d1730-108">The default is 0 (zero).</span></span> 
  
<span data-ttu-id="d1730-109">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d1730-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1730-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d1730-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d1730-111">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="d1730-111">Hyperlink.</span></span> <span data-ttu-id="d1730-112">*Name (имя* ). SortKey, где Hyperlink *. Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="d1730-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d1730-113">Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d1730-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1730-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d1730-114">Section index:</span></span>  <br/> |<span data-ttu-id="d1730-115">**Виссектионхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="d1730-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="d1730-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d1730-116">Row index:</span></span>  <br/> |<span data-ttu-id="d1730-117">**visRow1stHyperlink** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d1730-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d1730-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d1730-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d1730-119">**Вишлинксорткэй**</span><span class="sxs-lookup"><span data-stu-id="d1730-119">**visHLinkSortKey**</span></span> <br/> |
   

