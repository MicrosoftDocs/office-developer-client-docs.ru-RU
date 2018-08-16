---
title: Ячейка X (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Представляет x-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815187"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="17440-103">Ячейка X (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="17440-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="17440-104">Представляет *x*-координату, определяющую расположение управляющего маркера фигуры в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="17440-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="17440-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="17440-105">Remarks</span></span>

<span data-ttu-id="17440-106">Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="17440-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17440-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="17440-107">Cell name:</span></span>  <br/> | <span data-ttu-id="17440-108">Controls.</span><span class="sxs-lookup"><span data-stu-id="17440-108">Controls</span></span>  <span data-ttu-id="17440-109">*имя* .X, где Controls.</span><span class="sxs-lookup"><span data-stu-id="17440-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="17440-110">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="17440-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="17440-111">Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="17440-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17440-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="17440-112">Section index:</span></span>  <br/> |<span data-ttu-id="17440-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="17440-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="17440-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="17440-114">Row index:</span></span>  <br/> |<span data-ttu-id="17440-115">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="17440-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="17440-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="17440-116">Cell index:</span></span>  <br/> |<span data-ttu-id="17440-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="17440-117">**visCtlX**</span></span> <br/> |
   

