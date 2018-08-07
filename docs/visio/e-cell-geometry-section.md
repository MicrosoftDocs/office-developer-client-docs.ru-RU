---
title: Ячейка E (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Содержит формулу неоднородной rational сплайн (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813672"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="01b9c-103">Ячейка E (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="01b9c-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="01b9c-104">Содержит формулу неоднородной rational сплайн (NURBS).</span><span class="sxs-lookup"><span data-stu-id="01b9c-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01b9c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="01b9c-105">Remarks</span></span>

<span data-ttu-id="01b9c-106">Для получения ссылки на ячейки E по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="01b9c-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01b9c-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="01b9c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="01b9c-108">Геометрия *i* . E *j* где *i* и *j* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="01b9c-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="01b9c-109">Для получения ссылки на ячейки E по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="01b9c-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01b9c-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="01b9c-110">Section index:</span></span>  <br/> |<span data-ttu-id="01b9c-111">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="01b9c-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="01b9c-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="01b9c-112">Row index:</span></span>  <br/> |<span data-ttu-id="01b9c-113">**visRowVertex** +  *j* где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="01b9c-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="01b9c-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="01b9c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="01b9c-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="01b9c-115">**visNURBSData**</span></span> <br/> |
   

