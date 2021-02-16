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
description: Определяет X-компонент для требуемого вектора выравнивания совпадающих точек подключения. Ячейка DirX /A также используется для ориентирования присоединенной ногой динамического соединителя. Эта ячейка принимает значение с плавающей за точкой.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422399"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="8fcc1-105">DirX / A Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="8fcc1-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="8fcc1-106">Определяет  *x-компонент*  для требуемого вектора выравнивания совпадающих точек подключения.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="8fcc1-107">Ячейка DirX /A также используется для ориентирования присоединенной ногой динамического соединителя.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="8fcc1-108">Эта ячейка принимает значение с плавающей за точкой.</span><span class="sxs-lookup"><span data-stu-id="8fcc1-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8fcc1-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8fcc1-109">Remarks</span></span>

<span data-ttu-id="8fcc1-110">Чтобы получить ссылку на ячейку DirX или ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fcc1-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8fcc1-112">Connections.DirX[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8fcc1-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8fcc1-113">Чтобы получить ссылку на DirX / ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8fcc1-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-114">Section index:</span></span>  <br/> |<span data-ttu-id="8fcc1-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="8fcc1-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="8fcc1-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-116">Row index:</span></span>  <br/> |<span data-ttu-id="8fcc1-117">**visRowConnectionPts**  +   *i,* *где i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="8fcc1-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="8fcc1-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8fcc1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8fcc1-119">**visCnnctDirX** (неширимые строки)           **visCnnctA** (расширенные строки)</span><span class="sxs-lookup"><span data-stu-id="8fcc1-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="8fcc1-120">Сведения о невыбранных и расширенных строках см. в строке "Точки подключения".</span><span class="sxs-lookup"><span data-stu-id="8fcc1-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

