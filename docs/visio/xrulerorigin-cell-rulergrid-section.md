---
title: Ячейка XRulerOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Указывает точку начала координат на линейке по оси X для страницы.
ms.openlocfilehash: d66fd324718ec46b1209c4726eeb2d27c21db8b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346454"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="ef867-103">Ячейка XRulerOrigin (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="ef867-103">XRulerOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ef867-104">Указывает точку начала координат на линейке по оси X для страницы.</span><span class="sxs-lookup"><span data-stu-id="ef867-104">Specifies the zero point on the x-axis ruler for the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef867-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ef867-105">Remarks</span></span>

<span data-ttu-id="ef867-106">Эта ячейка соответствует параметру **Ноль на горизонтальной линейке** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="ef867-106">This cell corresponds to the horizontal **Ruler zero** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ef867-107">Чтобы получить ссылку на ячейку XRulerOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="ef867-107">To get a reference to the XRulerOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef867-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ef867-108">Cell name:</span></span>  <br/> |<span data-ttu-id="ef867-109">XRulerOrigin</span><span class="sxs-lookup"><span data-stu-id="ef867-109">XRulerOrigin</span></span>  <br/> |
   
<span data-ttu-id="ef867-110">Чтобы получить ссылку на ячейку XRulerOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ef867-110">To get a reference to the XRulerOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef867-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ef867-111">Section index:</span></span>  <br/> |<span data-ttu-id="ef867-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ef867-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ef867-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ef867-113">Row index:</span></span>  <br/> |<span data-ttu-id="ef867-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ef867-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ef867-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ef867-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ef867-116">**visXRulerOrigin**</span><span class="sxs-lookup"><span data-stu-id="ef867-116">**visXRulerOrigin**</span></span> <br/> |
   

