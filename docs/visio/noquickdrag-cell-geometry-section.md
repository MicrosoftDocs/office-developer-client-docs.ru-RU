---
title: NoQuickDrag Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Определяет, можно ли выбрать или перетащить фигуру, когда пользователь щелкает область заливки, определенную в разделе "геометрия".
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341064"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="0cc30-103">NoQuickDrag Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="0cc30-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="0cc30-104">Определяет, можно ли выбрать или перетащить фигуру, когда пользователь щелкает область заливки, определенную в разделе "геометрия".</span><span class="sxs-lookup"><span data-stu-id="0cc30-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cc30-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cc30-105">Remarks</span></span>

<span data-ttu-id="0cc30-106">Чтобы получить ссылку на ячейку NoQuickDrag по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="0cc30-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0cc30-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0cc30-107">Cell name:</span></span>  <br/> |<span data-ttu-id="0cc30-108">Геометрия *i* . NoQuickDrag, где \* i \* – <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0cc30-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0cc30-109">Чтобы получить ссылку на ячейку NoQuickDrag по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0cc30-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0cc30-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0cc30-110">Section index:</span></span>  <br/> |<span data-ttu-id="0cc30-111">**виссектионфирсткомпонент** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0cc30-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0cc30-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0cc30-112">Row index:</span></span>  <br/> |<span data-ttu-id="0cc30-113">**Висровкомпонент**</span><span class="sxs-lookup"><span data-stu-id="0cc30-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="0cc30-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0cc30-114">Cell index:</span></span>  <br/> |<span data-ttu-id="0cc30-115">**Вискомпнокуиккдраг**</span><span class="sxs-lookup"><span data-stu-id="0cc30-115">**visCompNoQuickDrag**</span></span> <br/> |
   

