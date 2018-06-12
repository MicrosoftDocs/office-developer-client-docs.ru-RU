---
title: Ячейка Y Dynamics (раздел элементы управления)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Представляет y-координаты точки привязки управляющего маркера в локальной системе координат. Точка привязки используется для эластичное во время dynamics.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815241"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="f840f-104">Ячейка Y Dynamics (раздел элементы управления)</span><span class="sxs-lookup"><span data-stu-id="f840f-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="f840f-105">Представляет *y* -координаты точки привязки управляющего маркера в локальной системе координат.</span><span class="sxs-lookup"><span data-stu-id="f840f-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="f840f-106">Точка привязки используется для эластичное во время dynamics.</span><span class="sxs-lookup"><span data-stu-id="f840f-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f840f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="f840f-107">Remarks</span></span>

<span data-ttu-id="f840f-108">Для получения ссылки на ячейки Y Dynamics по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f840f-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f840f-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="f840f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f840f-110">Элементы управления.</span><span class="sxs-lookup"><span data-stu-id="f840f-110">Controls.</span></span>  <span data-ttu-id="f840f-111">*имя* . Элементы управления YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="f840f-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="f840f-112">*имя* — это имя строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f840f-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f840f-113">Для получения ссылки на ячейки Y Dynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="f840f-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f840f-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f840f-114">Section index:</span></span>  <br/> |<span data-ttu-id="f840f-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f840f-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f840f-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f840f-116">Row index:</span></span>  <br/> |<span data-ttu-id="f840f-117">**visRowControl** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f840f-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f840f-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f840f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f840f-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="f840f-119">**visCtlYDyn**</span></span> <br/> |
   

