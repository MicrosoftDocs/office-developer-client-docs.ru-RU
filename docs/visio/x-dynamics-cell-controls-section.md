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
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322304"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="d3093-103">Ячейка X Dynamics (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="d3093-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="d3093-104">Представляет *x*-координату для точки привязки управляющего маркера в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="d3093-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d3093-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3093-105">Remarks</span></span>

<span data-ttu-id="d3093-106">Точка привязки используется для эластичного соединения при движении.</span><span class="sxs-lookup"><span data-stu-id="d3093-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="d3093-107">Чтобы получить ссылку на ячейку X Dynamics по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="d3093-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3093-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3093-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d3093-109">Controls.</span><span class="sxs-lookup"><span data-stu-id="d3093-109">Controls.</span></span>  <span data-ttu-id="d3093-110">*имя* .XDyn, где Controls.</span><span class="sxs-lookup"><span data-stu-id="d3093-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="d3093-111">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d3093-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="d3093-112">Чтобы получить ссылку на ячейку X Dynamics по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d3093-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3093-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d3093-113">Section index:</span></span>  <br/> |<span data-ttu-id="d3093-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="d3093-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="d3093-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d3093-115">Row index:</span></span>  <br/> |<span data-ttu-id="d3093-116">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="d3093-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d3093-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3093-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d3093-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="d3093-118">**visCtlXDyn**</span></span> <br/> |
   

