---
title: Ячейка YGridSpacing (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: Указывает расстояние между вертикальными линиями фиксированной сетки (YGridDensity = 0).
ms.openlocfilehash: 638479719ee0649bf271403249e2cde2ddccf09c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815225"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="0e823-103">Ячейка YGridSpacing (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="0e823-103">YGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="0e823-104">Указывает расстояние между вертикальными линиями фиксированной сетки (YGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="0e823-104">Specifies the distance between vertical lines in a fixed grid (YGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0e823-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e823-105">Remarks</span></span>

<span data-ttu-id="0e823-106">**Минимальный интервал** по вертикали, соответствует параметра в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="0e823-106">Corresponds to the vertical **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="0e823-107">Чтобы получить ссылку на ячейку YGridSpacing по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0e823-107">To get a reference to the YGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e823-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0e823-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0e823-109">YGridSpacing</span><span class="sxs-lookup"><span data-stu-id="0e823-109">YGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="0e823-110">Для получения ссылки на ячейки YGridSpacing по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0e823-110">To get a reference to the YGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e823-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e823-111">Section index:</span></span>  <br/> |<span data-ttu-id="0e823-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e823-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0e823-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e823-113">Row index:</span></span>  <br/> |<span data-ttu-id="0e823-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="0e823-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="0e823-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e823-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0e823-116">**visYGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="0e823-116">**visYGridSpacing**</span></span> <br/> |
   

