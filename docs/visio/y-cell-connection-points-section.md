---
title: Ячейка Y (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Представляет y-координату для точки соединения в локальных координатах.
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410849"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="bcac8-103">Ячейка Y (раздел "Точки соединения")</span><span class="sxs-lookup"><span data-stu-id="bcac8-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="bcac8-104">Представляет *y*-координату для точки соединения в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="bcac8-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bcac8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bcac8-105">Remarks</span></span>

<span data-ttu-id="bcac8-106">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="bcac8-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcac8-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bcac8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="bcac8-108">Connections.Y *i*, где *i* = <1>, 2, 3…</span><span class="sxs-lookup"><span data-stu-id="bcac8-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bcac8-109">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bcac8-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bcac8-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bcac8-110">Section index:</span></span>  <br/> |<span data-ttu-id="bcac8-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="bcac8-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="bcac8-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bcac8-112">Row index:</span></span>  <br/> |<span data-ttu-id="bcac8-113">**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="bcac8-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bcac8-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bcac8-114">Cell index:</span></span>  <br/> |<span data-ttu-id="bcac8-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="bcac8-115">**visY**</span></span> <br/> |
   

