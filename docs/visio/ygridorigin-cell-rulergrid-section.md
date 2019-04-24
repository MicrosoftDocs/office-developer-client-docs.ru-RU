---
title: Ячейка YGridOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: Указывает начало сетки по вертикали.
ms.openlocfilehash: fa8ee15d5ef2b5d581a9532336d3983bed17b1dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351676"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="bbfed-103">Ячейка YGridOrigin (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="bbfed-103">YGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="bbfed-104">Указывает начало сетки по вертикали.</span><span class="sxs-lookup"><span data-stu-id="bbfed-104">Specifies the vertical origin of the grid.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bbfed-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbfed-105">Remarks</span></span>

<span data-ttu-id="bbfed-106">Эта ячейка соответствует параметру **Начало сетки по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="bbfed-106">This cell corresponds to the vertical **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="bbfed-107">Чтобы получить ссылку на ячейку YGridOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="bbfed-107">To get a reference to the YGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbfed-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bbfed-108">Cell name:</span></span>  <br/> |<span data-ttu-id="bbfed-109">YGridOrigin</span><span class="sxs-lookup"><span data-stu-id="bbfed-109">YGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="bbfed-110">Чтобы получить ссылку на ячейку YGridOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bbfed-110">To get a reference to the YGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbfed-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bbfed-111">Section index:</span></span>  <br/> |<span data-ttu-id="bbfed-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbfed-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bbfed-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bbfed-113">Row index:</span></span>  <br/> |<span data-ttu-id="bbfed-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="bbfed-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="bbfed-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bbfed-115">Cell index:</span></span>  <br/> |<span data-ttu-id="bbfed-116">**visYGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="bbfed-116">**visYGridOrigin**</span></span> <br/> |
   

