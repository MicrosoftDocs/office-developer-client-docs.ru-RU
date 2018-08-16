---
title: Ячейка Y (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Положение на оси y в локальных координатах фигуры, относительно которого размещается кнопка тега действия.
ms.openlocfilehash: 641c868703c6e4b0b7e749f68813b5869b5728c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815208"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="060dc-103">Ячейка Y (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="060dc-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="060dc-104">Положение на оси *y* в локальных координатах фигуры, относительно которого размещается кнопка тега действия.</span><span class="sxs-lookup"><span data-stu-id="060dc-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="060dc-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="060dc-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="060dc-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="060dc-106">Remarks</span></span>

<span data-ttu-id="060dc-107">Ячейки X и Y определяют точку в локальных координатах фигуры, а ячейки X Justify и Y Justify определяют, где должна быть размещена кнопка тега действия относительно этой точки.</span><span class="sxs-lookup"><span data-stu-id="060dc-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="060dc-108">Чтобы получить ссылку на ячейку Y по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="060dc-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="060dc-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="060dc-109">Cell name:</span></span>  <br/> | <span data-ttu-id="060dc-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="060dc-110">SmartTags Property</span></span>  <span data-ttu-id="060dc-111">*имя* .Y, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="060dc-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="060dc-112">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="060dc-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="060dc-113">Чтобы получить ссылку на ячейку Y по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="060dc-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="060dc-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="060dc-114">Section index:</span></span>  <br/> |<span data-ttu-id="060dc-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="060dc-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="060dc-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="060dc-116">Row index:</span></span>  <br/> |<span data-ttu-id="060dc-117">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="060dc-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="060dc-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="060dc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="060dc-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="060dc-119">**visSmartTagY**</span></span> <br/> |
   

