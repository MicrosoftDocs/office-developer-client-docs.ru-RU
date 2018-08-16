---
title: Ячейка X Dynamics (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Представляет x-координату для точки привязки управляющего маркера в локальных координатах.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815211"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="6e99b-103">Ячейка X Dynamics (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="6e99b-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="6e99b-104">Представляет *x*-координату для точки привязки управляющего маркера в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="6e99b-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6e99b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e99b-105">Remarks</span></span>

<span data-ttu-id="6e99b-106">Точка привязки используется для эластичного соединения при движении.</span><span class="sxs-lookup"><span data-stu-id="6e99b-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="6e99b-107">Чтобы получить ссылку на ячейку X Dynamics по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="6e99b-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e99b-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6e99b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6e99b-109">Controls.</span><span class="sxs-lookup"><span data-stu-id="6e99b-109">Controls</span></span>  <span data-ttu-id="6e99b-110">*имя* .XDyn, где Controls.</span><span class="sxs-lookup"><span data-stu-id="6e99b-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="6e99b-111">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="6e99b-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="6e99b-112">Чтобы получить ссылку на ячейку X Dynamics по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6e99b-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e99b-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6e99b-113">Section index:</span></span>  <br/> |<span data-ttu-id="6e99b-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="6e99b-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="6e99b-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6e99b-115">Row index:</span></span>  <br/> |<span data-ttu-id="6e99b-116">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="6e99b-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6e99b-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6e99b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6e99b-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="6e99b-118">**visCtlXDyn**</span></span> <br/> |
   

