---
title: Ячейка YGridSpacing (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: Определяет расстояние между вертикальными линиями в фиксированной сетке (YGridDensity = 0).
ms.openlocfilehash: fc355b4e509494e9e7570122a8a3a7a3ce2e0588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417464"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="c8a44-103">Ячейка YGridSpacing (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="c8a44-103">YGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="c8a44-104">Определяет расстояние между вертикальными линиями в фиксированной сетке (YGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="c8a44-104">Specifies the distance between vertical lines in a fixed grid (YGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8a44-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8a44-105">Remarks</span></span>

<span data-ttu-id="c8a44-106">Соответствует параметру **Минимальный интервал по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="c8a44-106">Corresponds to the vertical **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="c8a44-107">Чтобы получить ссылку на ячейку YGridSpacing по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="c8a44-107">To get a reference to the YGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8a44-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c8a44-108">Cell name:</span></span>  <br/> |<span data-ttu-id="c8a44-109">YGridSpacing</span><span class="sxs-lookup"><span data-stu-id="c8a44-109">YGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="c8a44-110">Чтобы получить ссылку на ячейку YGridSpacing по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c8a44-110">To get a reference to the YGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8a44-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c8a44-111">Section index:</span></span>  <br/> |<span data-ttu-id="c8a44-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8a44-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c8a44-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c8a44-113">Row index:</span></span>  <br/> |<span data-ttu-id="c8a44-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="c8a44-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="c8a44-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c8a44-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c8a44-116">**visYGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="c8a44-116">**visYGridSpacing**</span></span> <br/> |
   

