---
title: E Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Содержит формулу неоднородного рационального B-сплайна (NURBS).
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327393"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="02d40-103">E Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="02d40-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="02d40-104">Содержит формулу неоднородного рационального B-сплайна (NURBS).</span><span class="sxs-lookup"><span data-stu-id="02d40-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02d40-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="02d40-105">Remarks</span></span>

<span data-ttu-id="02d40-106">Чтобы получить ссылку на ячейку E по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="02d40-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02d40-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="02d40-107">Cell name:</span></span>  <br/> | <span data-ttu-id="02d40-108">Геометрия *i* . E *j* , где *i* и *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="02d40-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="02d40-109">Чтобы получить ссылку на ячейку E по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="02d40-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02d40-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="02d40-110">Section index:</span></span>  <br/> |<span data-ttu-id="02d40-111">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="02d40-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="02d40-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="02d40-112">Row index:</span></span>  <br/> |<span data-ttu-id="02d40-113">**visRowVertex** +  *j*, где *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="02d40-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="02d40-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="02d40-114">Cell index:</span></span>  <br/> |<span data-ttu-id="02d40-115">**Виснурбсдата**</span><span class="sxs-lookup"><span data-stu-id="02d40-115">**visNURBSData**</span></span> <br/> |
   

