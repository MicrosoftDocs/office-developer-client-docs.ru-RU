---
title: Ячейка XGridOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Указывает горизонтальную координату начала сетки.
ms.openlocfilehash: ee58ea7d950dd7e422f8a60a13bac8aa4ed353a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428622"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="36054-103">Ячейка XGridOrigin (раздел "Линейка и сетка")</span><span class="sxs-lookup"><span data-stu-id="36054-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="36054-104">Указывает горизонтальную координату начала сетки.</span><span class="sxs-lookup"><span data-stu-id="36054-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36054-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="36054-105">Remarks</span></span>

<span data-ttu-id="36054-106">Эта ячейка соответствует параметру **Начало сетки** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**).</span><span class="sxs-lookup"><span data-stu-id="36054-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="36054-107">Чтобы получить ссылку на ячейку XGridOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="36054-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36054-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="36054-108">Cell name:</span></span>  <br/> |<span data-ttu-id="36054-109">XGridOrigin</span><span class="sxs-lookup"><span data-stu-id="36054-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="36054-110">Чтобы получить ссылку на ячейку XGridOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="36054-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36054-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="36054-111">Section index:</span></span>  <br/> |<span data-ttu-id="36054-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="36054-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="36054-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="36054-113">Row index:</span></span>  <br/> |<span data-ttu-id="36054-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="36054-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="36054-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="36054-115">Cell index:</span></span>  <br/> |<span data-ttu-id="36054-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="36054-116">**visXGridOrigin**</span></span> <br/> |
   

