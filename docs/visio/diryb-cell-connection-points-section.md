---
title: DirY / B Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Определяет Y-компонент для требуемого вектора выравнивания совпадающих точек подключения. Он также используется для ориентировки присоединенной ногой динамического соединителя. Эта ячейка принимает значение с плавающей за точкой.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417093"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="3ffe1-105">DirY / B Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="3ffe1-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="3ffe1-106">Определяет  *Y-компонент*  для требуемого вектора выравнивания совпадающих точек подключения.</span><span class="sxs-lookup"><span data-stu-id="3ffe1-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="3ffe1-107">Он также используется для ориентировки присоединенной ногой динамического соединителя.</span><span class="sxs-lookup"><span data-stu-id="3ffe1-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="3ffe1-108">Эта ячейка принимает значение с плавающей за точкой.</span><span class="sxs-lookup"><span data-stu-id="3ffe1-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ffe1-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ffe1-109">Remarks</span></span>

<span data-ttu-id="3ffe1-110">Чтобы получить ссылку на ячейку DirY / B по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ffe1-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-111">Cell name:</span></span>  <br/> |<span data-ttu-id="3ffe1-112">Connections.DirY[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3ffe1-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3ffe1-113">Чтобы получить ссылку на ячейку DirY /B по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ffe1-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-114">Section index:</span></span>  <br/> |<span data-ttu-id="3ffe1-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="3ffe1-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="3ffe1-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-116">Row index:</span></span>  <br/> |<span data-ttu-id="3ffe1-117">**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="3ffe1-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3ffe1-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3ffe1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3ffe1-119">**visCnnctDirY** (неширимые строки)           **visCnnctB** (расширенные строки)</span><span class="sxs-lookup"><span data-stu-id="3ffe1-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="3ffe1-120">Сведения о невыбранных и расширенных строках см. в строке "Точки подключения".</span><span class="sxs-lookup"><span data-stu-id="3ffe1-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

