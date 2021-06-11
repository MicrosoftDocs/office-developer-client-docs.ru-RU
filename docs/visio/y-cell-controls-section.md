---
title: Ячейка Y (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Представляет y-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407951"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="b69f3-103">Ячейка Y (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="b69f3-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="b69f3-104">Представляет *y*-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="b69f3-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b69f3-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b69f3-105">Remarks</span></span>

<span data-ttu-id="b69f3-106">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="b69f3-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b69f3-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b69f3-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b69f3-108">Controls.</span><span class="sxs-lookup"><span data-stu-id="b69f3-108">Controls.</span></span>  <span data-ttu-id="b69f3-109">*имя* .Y, где Controls.</span><span class="sxs-lookup"><span data-stu-id="b69f3-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="b69f3-110">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b69f3-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="b69f3-111">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b69f3-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b69f3-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b69f3-112">Section index:</span></span>  <br/> |<span data-ttu-id="b69f3-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="b69f3-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="b69f3-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b69f3-114">Row index:</span></span>  <br/> |<span data-ttu-id="b69f3-115">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="b69f3-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b69f3-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b69f3-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b69f3-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="b69f3-117">**visCtlY**</span></span> <br/> |
   

