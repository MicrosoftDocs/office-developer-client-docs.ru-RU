---
title: Ячейка XGridSpacing (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815188"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="87b6d-103">Ячейка XGridSpacing (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="87b6d-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="87b6d-104">Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="87b6d-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87b6d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="87b6d-105">Remarks</span></span>

<span data-ttu-id="87b6d-106">Эта ячейка соответствует параметру **Минимальный интервал** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="87b6d-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="87b6d-107">Чтобы получить ссылку на ячейку XGridSpacing по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="87b6d-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87b6d-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="87b6d-108">Cell name:</span></span>  <br/> |<span data-ttu-id="87b6d-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="87b6d-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="87b6d-110">Чтобы получить ссылку на ячейку XGridSpacing по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="87b6d-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87b6d-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="87b6d-111">Section index:</span></span>  <br/> |<span data-ttu-id="87b6d-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87b6d-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87b6d-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="87b6d-113">Row index:</span></span>  <br/> |<span data-ttu-id="87b6d-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="87b6d-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="87b6d-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="87b6d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="87b6d-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="87b6d-116">**visXGridSpacing**</span></span> <br/> |
   

