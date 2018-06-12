---
title: Ячейка Y (раздел элементы управления)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Представляет y-координата, который указывает расположение управляющего маркера фигуры в локальной системе координат.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815207"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="19a8a-103">Ячейка Y (раздел элементы управления)</span><span class="sxs-lookup"><span data-stu-id="19a8a-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="19a8a-104">Представляет *y* -координата, который указывает расположение управляющего маркера фигуры в локальной системе координат.</span><span class="sxs-lookup"><span data-stu-id="19a8a-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19a8a-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="19a8a-105">Remarks</span></span>

<span data-ttu-id="19a8a-106">Чтобы получить ссылку на ячейку Y по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="19a8a-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19a8a-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="19a8a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="19a8a-108">Элементы управления.</span><span class="sxs-lookup"><span data-stu-id="19a8a-108">Controls.</span></span>  <span data-ttu-id="19a8a-109">*имя* . Элементы управления Ywhere.</span><span class="sxs-lookup"><span data-stu-id="19a8a-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="19a8a-110">*имя* — это имя строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="19a8a-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="19a8a-111">Для получения ссылки на ячейки Y по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="19a8a-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19a8a-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="19a8a-112">Section index:</span></span>  <br/> |<span data-ttu-id="19a8a-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="19a8a-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="19a8a-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="19a8a-114">Row index:</span></span>  <br/> |<span data-ttu-id="19a8a-115">**visRowControl** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="19a8a-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="19a8a-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="19a8a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="19a8a-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="19a8a-117">**visCtlY**</span></span> <br/> |
   

