---
title: Ячейка X (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Представляет x-координату для точки соединения в локальных координатах.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815182"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="3d46b-103">Ячейка X (раздел "Точки соединения")</span><span class="sxs-lookup"><span data-stu-id="3d46b-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="3d46b-104">Представляет *x*-координату для точки соединения в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="3d46b-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d46b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d46b-105">Remarks</span></span>

<span data-ttu-id="3d46b-106">Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="3d46b-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d46b-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3d46b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3d46b-108">Connections.X *i*, где *i* = <1>, 2, 3…</span><span class="sxs-lookup"><span data-stu-id="3d46b-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3d46b-109">Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3d46b-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d46b-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3d46b-110">Section index:</span></span>  <br/> |<span data-ttu-id="3d46b-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="3d46b-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="3d46b-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3d46b-112">Row index:</span></span>  <br/> |<span data-ttu-id="3d46b-113">**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="3d46b-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3d46b-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3d46b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3d46b-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="3d46b-115">**visX**</span></span> <br/> |
   

