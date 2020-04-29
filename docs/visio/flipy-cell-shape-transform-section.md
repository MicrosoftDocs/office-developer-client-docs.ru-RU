---
title: FlipY Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Указывает, была ли фигура отражена по вертикали.
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417450"
---
# <a name="flipy-cell-shape-transform-section"></a><span data-ttu-id="1f8d1-103">FlipY Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="1f8d1-103">FlipY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="1f8d1-104">Указывает, была ли фигура отражена по вертикали.</span><span class="sxs-lookup"><span data-stu-id="1f8d1-104">Indicates whether the shape has been flipped vertically.</span></span>
  
|<span data-ttu-id="1f8d1-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1f8d1-105">**Value**</span></span>|<span data-ttu-id="1f8d1-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f8d1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1f8d1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1f8d1-107">TRUE</span></span>  <br/> | <span data-ttu-id="1f8d1-108">Фигура была зеркально отражена по вертикали.</span><span class="sxs-lookup"><span data-stu-id="1f8d1-108">The shape has been flipped vertically.</span></span>  <br/> |
| <span data-ttu-id="1f8d1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1f8d1-109">FALSE</span></span>  <br/> | <span data-ttu-id="1f8d1-110">Фигура не была зеркально отражена по вертикали.</span><span class="sxs-lookup"><span data-stu-id="1f8d1-110">The shape has not been flipped vertically.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f8d1-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f8d1-111">Remarks</span></span>

<span data-ttu-id="1f8d1-112">Чтобы получить ссылку на перевернутую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-112">To get a reference to the FlipY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f8d1-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1f8d1-114">FlipY</span><span class="sxs-lookup"><span data-stu-id="1f8d1-114">FlipY</span></span>  <br/> |
   
<span data-ttu-id="1f8d1-115">Чтобы получить ссылку на перевернутую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-115">To get a reference to the FlipY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1f8d1-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-116">Section index:</span></span>  <br/> |<span data-ttu-id="1f8d1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1f8d1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1f8d1-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-118">Row index:</span></span>  <br/> |<span data-ttu-id="1f8d1-119">**висровксформаут**</span><span class="sxs-lookup"><span data-stu-id="1f8d1-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="1f8d1-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1f8d1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1f8d1-121">**висксформфлипи**</span><span class="sxs-lookup"><span data-stu-id="1f8d1-121">**visXFormFlipY**</span></span> <br/> |
   

