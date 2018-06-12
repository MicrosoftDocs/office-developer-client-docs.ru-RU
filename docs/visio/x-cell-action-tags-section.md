---
title: X ячейки (действие помечает раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: X - координаты в локальной системе координат фигуры вокруг которых размещается кнопка тега действия.
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815178"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="3ae59-103">X ячейки (действие помечает раздел)</span><span class="sxs-lookup"><span data-stu-id="3ae59-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="3ae59-104">*X* -координат в локальной системе координат фигуры вокруг которых размещается кнопка тега действия.</span><span class="sxs-lookup"><span data-stu-id="3ae59-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3ae59-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="3ae59-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ae59-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="3ae59-106">Remarks</span></span>

<span data-ttu-id="3ae59-107">Ячейки X и Y указывать точки в локальной системе координат фигуры и ячейки обоснование X и Y ширине поместить кнопки тега действия по отношению к точке.</span><span class="sxs-lookup"><span data-stu-id="3ae59-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="3ae59-108">Чтобы получить ссылку на ячейку X по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3ae59-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ae59-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="3ae59-109">Cell name:</span></span>  <br/> |<span data-ttu-id="3ae59-110">Смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="3ae59-110">SmartTags.</span></span> <span data-ttu-id="3ae59-111">*имя* . X, где смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="3ae59-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="3ae59-112">*имя* — это имя строки тега действия</span><span class="sxs-lookup"><span data-stu-id="3ae59-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3ae59-113">Для получения ссылки на ячейки X по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="3ae59-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ae59-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3ae59-114">Section index:</span></span>  <br/> |<span data-ttu-id="3ae59-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3ae59-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3ae59-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3ae59-116">Row index:</span></span>  <br/> |<span data-ttu-id="3ae59-117">**visRowSmartTag** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ae59-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ae59-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3ae59-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3ae59-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="3ae59-119">**visSmartTagX**</span></span> <br/> |
   

