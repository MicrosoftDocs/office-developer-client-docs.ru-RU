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
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327323"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="16438-103">Ячейка XGridSpacing (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="16438-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="16438-104">Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="16438-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16438-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="16438-105">Remarks</span></span>

<span data-ttu-id="16438-106">Эта ячейка соответствует параметру **Минимальный интервал** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="16438-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="16438-107">Чтобы получить ссылку на ячейку XGridSpacing по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="16438-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16438-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="16438-108">Cell name:</span></span>  <br/> |<span data-ttu-id="16438-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="16438-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="16438-110">Чтобы получить ссылку на ячейку XGridSpacing по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="16438-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16438-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="16438-111">Section index:</span></span>  <br/> |<span data-ttu-id="16438-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16438-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="16438-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="16438-113">Row index:</span></span>  <br/> |<span data-ttu-id="16438-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="16438-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="16438-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="16438-115">Cell index:</span></span>  <br/> |<span data-ttu-id="16438-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="16438-116">**visXGridSpacing**</span></span> <br/> |
   

