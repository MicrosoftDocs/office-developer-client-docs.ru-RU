---
title: Угол ячейки (раздел Преобразование фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Представляет фигуры текущий угол вращения относительно его родительского элемента. Формула по умолчанию для угла фигуры 1 D: = ATAN2(EndY-BeginY,EndX-BeginX).'
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813145"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="20c79-104">Угол ячейки (раздел Преобразование фигуры)</span><span class="sxs-lookup"><span data-stu-id="20c79-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="20c79-105">Представляет фигуры текущий угол вращения относительно его родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="20c79-105">Represents the shape's current angle of rotation in relation to its parent.</span></span> <span data-ttu-id="20c79-106">Формула по умолчанию для угла фигуры 1 D: = ATAN2(EndY-BeginY,EndX-BeginX).</span><span class="sxs-lookup"><span data-stu-id="20c79-106">The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20c79-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="20c79-107">Remarks</span></span>

<span data-ttu-id="20c79-108">Для получения ссылки на ячейки угол по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="20c79-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20c79-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="20c79-109">Cell name:</span></span>  <br/> | <span data-ttu-id="20c79-110">Угол</span><span class="sxs-lookup"><span data-stu-id="20c79-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="20c79-111">Для получения ссылки на ячейки угол по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="20c79-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20c79-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="20c79-112">Section index:</span></span>  <br/> |<span data-ttu-id="20c79-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20c79-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20c79-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="20c79-114">Row index:</span></span>  <br/> |<span data-ttu-id="20c79-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="20c79-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="20c79-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="20c79-116">Cell index:</span></span>  <br/> |<span data-ttu-id="20c79-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="20c79-117">**visXFormAngle**</span></span> <br/> |
   

