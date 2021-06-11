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
description: Определяет, можно ли выбрать или перетаскить фигуру, если пользователь щелкнуть заполненную область, задатую разделом Геометрия.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417723"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="acbae-103">NoQuickDrag Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="acbae-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="acbae-104">Определяет, можно ли выбрать или перетаскить фигуру, если пользователь щелкнуть заполненную область, задатую разделом Геометрия.</span><span class="sxs-lookup"><span data-stu-id="acbae-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="acbae-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="acbae-105">Remarks</span></span>

<span data-ttu-id="acbae-106">Чтобы получить ссылку на ячейку NoQuickDrag по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="acbae-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acbae-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="acbae-107">Cell name:</span></span>  <br/> |<span data-ttu-id="acbae-108">Геометрия  *i*  . NoQuickDrag, где \* i \* - <1>, 2, 3 ...</span><span class="sxs-lookup"><span data-stu-id="acbae-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="acbae-109">Чтобы получить ссылку на ячейку NoQuickDrag по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="acbae-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acbae-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="acbae-110">Section index:</span></span>  <br/> |<span data-ttu-id="acbae-111">**visSectionFirstComponent**  +   *i* , где *i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="acbae-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="acbae-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="acbae-112">Row index:</span></span>  <br/> |<span data-ttu-id="acbae-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="acbae-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="acbae-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="acbae-114">Cell index:</span></span>  <br/> |<span data-ttu-id="acbae-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="acbae-115">**visCompNoQuickDrag**</span></span> <br/> |
   

