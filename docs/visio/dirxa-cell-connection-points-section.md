---
title: DirX / A Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Определяет x компонент для требуемого вектора выравнивания соответствующей точки подключения. Ячейка ячейка dirx/A также используется для ориентации присоединенной стороны динамической соединительной линии. Эта ячейка принимает значение с плавающей запятой.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332595"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="ba802-105">DirX / A Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="ba802-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="ba802-106">Определяет *x* компонент для требуемого вектора выравнивания соответствующей точки подключения.</span><span class="sxs-lookup"><span data-stu-id="ba802-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="ba802-107">Ячейка ячейка dirx/A также используется для ориентации присоединенной стороны динамической соединительной линии.</span><span class="sxs-lookup"><span data-stu-id="ba802-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="ba802-108">Эта ячейка принимает значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ba802-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba802-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba802-109">Remarks</span></span>

<span data-ttu-id="ba802-110">Чтобы получить ссылку на ячейку ячейка dirx/A по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ba802-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba802-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ba802-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ba802-112">Connections. ячейка dirx [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ba802-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ba802-113">Чтобы получить ссылку на ячейку ячейка dirx/A по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ba802-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba802-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ba802-114">Section index:</span></span>  <br/> |<span data-ttu-id="ba802-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="ba802-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="ba802-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ba802-116">Row index:</span></span>  <br/> |<span data-ttu-id="ba802-117">**висровконнектионптс** +  *i* , где *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="ba802-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="ba802-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ba802-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ba802-119">**вискннктдиркс** (нерасширенные строки)           **вискннкта** (расширенные строки)</span><span class="sxs-lookup"><span data-stu-id="ba802-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="ba802-120">Сведения о нерасширенных и расширенных строках можно найти в статье точки подключения.</span><span class="sxs-lookup"><span data-stu-id="ba802-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

