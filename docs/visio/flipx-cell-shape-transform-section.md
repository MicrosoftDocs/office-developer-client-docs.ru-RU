---
title: FlipX Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Указывает, была ли фигура перевернута горизонтально.
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415952"
---
# <a name="flipx-cell-shape-transform-section"></a><span data-ttu-id="fbefc-103">FlipX Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="fbefc-103">FlipX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="fbefc-104">Указывает, была ли фигура перевернута горизонтально.</span><span class="sxs-lookup"><span data-stu-id="fbefc-104">Indicates whether the shape has been flipped horizontally.</span></span>
  
|<span data-ttu-id="fbefc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fbefc-105">**Value**</span></span>|<span data-ttu-id="fbefc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbefc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fbefc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fbefc-107">TRUE</span></span>  <br/> | <span data-ttu-id="fbefc-108">Фигура перевернута горизонтально.</span><span class="sxs-lookup"><span data-stu-id="fbefc-108">The shape has been flipped horizontally.</span></span>  <br/> |
| <span data-ttu-id="fbefc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fbefc-109">FALSE</span></span>  <br/> | <span data-ttu-id="fbefc-110">Фигура не перевернута горизонтально.</span><span class="sxs-lookup"><span data-stu-id="fbefc-110">The shape has not been flipped horizontally.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbefc-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbefc-111">Remarks</span></span>

<span data-ttu-id="fbefc-112">Чтобы получить ссылку на ячейку FlipX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fbefc-112">To get a reference to the FlipX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbefc-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbefc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fbefc-114">FlipX</span><span class="sxs-lookup"><span data-stu-id="fbefc-114">FlipX</span></span>  <br/> |
   
<span data-ttu-id="fbefc-115">Чтобы получить ссылку на ячейку FlipX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fbefc-115">To get a reference to the FlipX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbefc-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fbefc-116">Section index:</span></span>  <br/> |<span data-ttu-id="fbefc-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fbefc-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fbefc-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fbefc-118">Row index:</span></span>  <br/> |<span data-ttu-id="fbefc-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="fbefc-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="fbefc-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fbefc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fbefc-121">**visXFormFlipX**</span><span class="sxs-lookup"><span data-stu-id="fbefc-121">**visXFormFlipX**</span></span> <br/> |
   

