---
title: Ячейка YGridOrigin (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: Задает вертикальную начала сетки.
ms.openlocfilehash: 2d914fc15df8a100066ad17a2e35001fe8a4d587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815217"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="b2724-103">Ячейка YGridOrigin (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="b2724-103">YGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="b2724-104">Задает вертикальную начала сетки.</span><span class="sxs-lookup"><span data-stu-id="b2724-104">Specifies the vertical origin of the grid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2724-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2724-105">Remarks</span></span>

<span data-ttu-id="b2724-106">В этой ячейке соответствует вертикальной **начала сетки** параметра в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ).</span><span class="sxs-lookup"><span data-stu-id="b2724-106">This cell corresponds to the vertical **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="b2724-107">Чтобы получить ссылку на ячейку YGridOrigin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b2724-107">To get a reference to the YGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2724-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b2724-108">Cell name:</span></span>  <br/> |<span data-ttu-id="b2724-109">YGridOrigin</span><span class="sxs-lookup"><span data-stu-id="b2724-109">YGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="b2724-110">Для получения ссылки на ячейки YGridOrigin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b2724-110">To get a reference to the YGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2724-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b2724-111">Section index:</span></span>  <br/> |<span data-ttu-id="b2724-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2724-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b2724-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b2724-113">Row index:</span></span>  <br/> |<span data-ttu-id="b2724-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="b2724-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="b2724-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b2724-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b2724-116">**visYGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="b2724-116">**visYGridOrigin**</span></span> <br/> |
   

