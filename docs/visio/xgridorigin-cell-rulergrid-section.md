---
title: Ячейка XGridOrigin (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Задает горизонтальной оси начала сетки.
ms.openlocfilehash: 0cc6ff10f9bb4ba7ee0a13a48cb55b7dcd0fa013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815199"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a><span data-ttu-id="176b9-103">Ячейка XGridOrigin (линейки &amp; сетка)</span><span class="sxs-lookup"><span data-stu-id="176b9-103">XGridOrigin Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="176b9-104">Задает горизонтальной оси начала сетки.</span><span class="sxs-lookup"><span data-stu-id="176b9-104">Specifies the horizontal coordinate of the grid origin.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="176b9-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="176b9-105">Remarks</span></span>

<span data-ttu-id="176b9-106">В этой ячейке соответствует горизонтальной **начала сетки** параметра в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** .</span><span class="sxs-lookup"><span data-stu-id="176b9-106">This cell corresponds to the horizontal **Grid origin** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow.</span></span> 
  
<span data-ttu-id="176b9-107">Чтобы получить ссылку на ячейку XGridOrigin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="176b9-107">To get a reference to the XGridOrigin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="176b9-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="176b9-108">Cell name:</span></span>  <br/> |<span data-ttu-id="176b9-109">XGridOrigin</span><span class="sxs-lookup"><span data-stu-id="176b9-109">XGridOrigin</span></span>  <br/> |
   
<span data-ttu-id="176b9-110">Для получения ссылки на ячейки XGridOrigin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="176b9-110">To get a reference to the XGridOrigin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="176b9-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="176b9-111">Section index:</span></span>  <br/> |<span data-ttu-id="176b9-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="176b9-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="176b9-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="176b9-113">Row index:</span></span>  <br/> |<span data-ttu-id="176b9-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="176b9-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="176b9-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="176b9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="176b9-116">**visXGridOrigin**</span><span class="sxs-lookup"><span data-stu-id="176b9-116">**visXGridOrigin**</span></span> <br/> |
   

