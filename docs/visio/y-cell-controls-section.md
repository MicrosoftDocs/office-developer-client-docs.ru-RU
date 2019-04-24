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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360153"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="0c796-103">Ячейка Y (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="0c796-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="0c796-104">Представляет *y*-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="0c796-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c796-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c796-105">Remarks</span></span>

<span data-ttu-id="0c796-106">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="0c796-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c796-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0c796-107">Cell name:</span></span>  <br/> | <span data-ttu-id="0c796-108">Controls.</span><span class="sxs-lookup"><span data-stu-id="0c796-108">Controls.</span></span>  <span data-ttu-id="0c796-109">*имя* .Y, где Controls.</span><span class="sxs-lookup"><span data-stu-id="0c796-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="0c796-110">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="0c796-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="0c796-111">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0c796-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c796-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0c796-112">Section index:</span></span>  <br/> |<span data-ttu-id="0c796-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="0c796-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="0c796-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0c796-114">Row index:</span></span>  <br/> |<span data-ttu-id="0c796-115">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="0c796-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0c796-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0c796-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0c796-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="0c796-117">**visCtlY**</span></span> <br/> |
   

