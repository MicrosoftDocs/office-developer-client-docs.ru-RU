---
title: Ячейка X (раздел "Теги действий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Положение на оси x в локальных координатах фигуры, относительно которого размещается кнопка тега действия.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431115"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="d67cc-103">Ячейка X (раздел "Теги действий")</span><span class="sxs-lookup"><span data-stu-id="d67cc-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="d67cc-104">Положение на оси *x* в локальных координатах фигуры, относительно которого размещается кнопка тега действия.</span><span class="sxs-lookup"><span data-stu-id="d67cc-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d67cc-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="d67cc-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d67cc-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="d67cc-106">Remarks</span></span>

<span data-ttu-id="d67cc-107">Ячейки X и Y определяют точку в локальных координатах фигуры, а ячейки X Justify и Y Justify определяют, где должна быть размещена кнопка тега действия относительно этой точки.</span><span class="sxs-lookup"><span data-stu-id="d67cc-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="d67cc-108">Чтобы получить ссылку на ячейку X по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="d67cc-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d67cc-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d67cc-109">Cell name:</span></span>  <br/> |<span data-ttu-id="d67cc-110">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="d67cc-110">SmartTags.</span></span> <span data-ttu-id="d67cc-111">*имя* .X, где SmartTags.</span><span class="sxs-lookup"><span data-stu-id="d67cc-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="d67cc-112">*имя* — название строки тегов действий.</span><span class="sxs-lookup"><span data-stu-id="d67cc-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="d67cc-113">Чтобы получить ссылку на ячейку X по индексу из программы, укажите свойство **CellsSRC** с такими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d67cc-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d67cc-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d67cc-114">Section index:</span></span>  <br/> |<span data-ttu-id="d67cc-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="d67cc-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="d67cc-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d67cc-116">Row index:</span></span>  <br/> |<span data-ttu-id="d67cc-117">**visRowSmartTag** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="d67cc-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d67cc-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d67cc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d67cc-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="d67cc-119">**visSmartTagX**</span></span> <br/> |
   

