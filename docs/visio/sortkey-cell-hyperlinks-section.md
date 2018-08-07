---
title: Ячейка SortKey (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Число, определяющее порядок гиперссылки, которые отображаются в контекстном меню.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814924"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="6a4d5-103">Ячейка SortKey (раздел "Гиперссылки")</span><span class="sxs-lookup"><span data-stu-id="6a4d5-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="6a4d5-104">Число, определяющее порядок гиперссылки, которые отображаются в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="6a4d5-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a4d5-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a4d5-105">Remarks</span></span>

<span data-ttu-id="6a4d5-106">В меню Упорядочить от низшего к наибольшим, с нижней номера отображаются в верхней части меню отображаются гиперссылки в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="6a4d5-106">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu.</span></span> <span data-ttu-id="6a4d5-107">Если две строки гиперссылки имеют такое же значение ячейки SortKey, порядок определяется порядок физических строк.</span><span class="sxs-lookup"><span data-stu-id="6a4d5-107">If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order.</span></span> <span data-ttu-id="6a4d5-108">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="6a4d5-108">The default is 0 (zero).</span></span> 
  
<span data-ttu-id="6a4d5-109">Чтобы получить ссылку на ячейку SortKey по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6a4d5-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a4d5-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6a4d5-110">Cell name:</span></span>  <br/> |<span data-ttu-id="6a4d5-111">Гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="6a4d5-111">Hyperlink.</span></span> <span data-ttu-id="6a4d5-112">*имя* . SortKey, где гиперссылки *.name* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="6a4d5-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6a4d5-113">Для получения ссылки на ячейки SortKey по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6a4d5-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a4d5-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6a4d5-114">Section index:</span></span>  <br/> |<span data-ttu-id="6a4d5-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="6a4d5-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="6a4d5-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6a4d5-116">Row index:</span></span>  <br/> |<span data-ttu-id="6a4d5-117">**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6a4d5-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6a4d5-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6a4d5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6a4d5-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="6a4d5-119">**visHLinkSortKey**</span></span> <br/> |
   

