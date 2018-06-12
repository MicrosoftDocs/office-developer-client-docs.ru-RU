---
title: X Dynamics ячейки (раздел элементы управления)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Представляет x-координаты точки привязки управляющего маркера в локальной системе координат.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815211"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="055ca-103">X Dynamics ячейки (раздел элементы управления)</span><span class="sxs-lookup"><span data-stu-id="055ca-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="055ca-104">Представляет *x* -координаты точки привязки управляющего маркера в локальной системе координат.</span><span class="sxs-lookup"><span data-stu-id="055ca-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="055ca-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="055ca-105">Remarks</span></span>

<span data-ttu-id="055ca-106">Точка привязки используется для эластичное во время dynamics.</span><span class="sxs-lookup"><span data-stu-id="055ca-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="055ca-107">Для получения ссылки на ячейки X Dynamics по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="055ca-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="055ca-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="055ca-108">Cell name:</span></span>  <br/> | <span data-ttu-id="055ca-109">Элементы управления.</span><span class="sxs-lookup"><span data-stu-id="055ca-109">Controls.</span></span>  <span data-ttu-id="055ca-110">*имя* . Элементы управления XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="055ca-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="055ca-111">*имя* — это имя строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="055ca-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="055ca-112">Для получения ссылки на ячейки X Dynamics по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="055ca-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="055ca-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="055ca-113">Section index:</span></span>  <br/> |<span data-ttu-id="055ca-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="055ca-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="055ca-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="055ca-115">Row index:</span></span>  <br/> |<span data-ttu-id="055ca-116">**visRowControl** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="055ca-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="055ca-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="055ca-117">Cell index:</span></span>  <br/> |<span data-ttu-id="055ca-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="055ca-118">**visCtlXDyn**</span></span> <br/> |
   

