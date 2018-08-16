---
title: Ячейка Y Dynamics (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Представляет y-координату для точки привязки управляющего маркера в локальных координатах. Точка привязки используется для эластичного соединения при движении.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815241"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="a1759-104">Ячейка Y Dynamics (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="a1759-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="a1759-105">Представляет *y*-координату для точки привязки управляющего маркера в локальных координатах.</span><span class="sxs-lookup"><span data-stu-id="a1759-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="a1759-106">Точка привязки используется для эластичного соединения при движении.</span><span class="sxs-lookup"><span data-stu-id="a1759-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1759-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1759-107">Remarks</span></span>

<span data-ttu-id="a1759-108">Чтобы получить ссылку на ячейку Y Dynamics по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="a1759-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1759-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a1759-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a1759-110">Controls.</span><span class="sxs-lookup"><span data-stu-id="a1759-110">Controls</span></span>  <span data-ttu-id="a1759-111">*имя* .YDyn, где Controls.</span><span class="sxs-lookup"><span data-stu-id="a1759-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="a1759-112">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a1759-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="a1759-113">Чтобы получить ссылку на ячейку Y Dynamics по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a1759-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1759-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a1759-114">Section index:</span></span>  <br/> |<span data-ttu-id="a1759-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="a1759-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="a1759-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a1759-116">Row index:</span></span>  <br/> |<span data-ttu-id="a1759-117">**visRowControl** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="a1759-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a1759-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a1759-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a1759-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="a1759-119">**visCtlYDyn**</span></span> <br/> |
   

