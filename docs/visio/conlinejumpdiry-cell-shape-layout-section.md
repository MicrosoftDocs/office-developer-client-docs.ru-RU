---
title: ConLineJumpDirY Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404773"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="f8dfb-103">ConLineJumpDirY Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="f8dfb-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f8dfb-104">Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="f8dfb-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="f8dfb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-105">**Value**</span></span>|<span data-ttu-id="f8dfb-106">**Направление пересечения линий**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-106">**Line Jump Direction**</span></span>|<span data-ttu-id="f8dfb-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f8dfb-108">нуль</span><span class="sxs-lookup"><span data-stu-id="f8dfb-108">0</span></span>  <br/> | <span data-ttu-id="f8dfb-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8dfb-109">Page default</span></span>  <br/> |<span data-ttu-id="f8dfb-110">**Висложумпдиридефаулт**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="f8dfb-111">1,1</span><span class="sxs-lookup"><span data-stu-id="f8dfb-111">1</span></span>  <br/> | <span data-ttu-id="f8dfb-112">Left</span><span class="sxs-lookup"><span data-stu-id="f8dfb-112">Left</span></span>  <br/> |<span data-ttu-id="f8dfb-113">**Висложумпдирилефт**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="f8dfb-114">2</span><span class="sxs-lookup"><span data-stu-id="f8dfb-114">2</span></span>  <br/> | <span data-ttu-id="f8dfb-115">Right</span><span class="sxs-lookup"><span data-stu-id="f8dfb-115">Right</span></span>  <br/> |<span data-ttu-id="f8dfb-116">**Висложумпдириригхт**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8dfb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8dfb-117">Remarks</span></span>

<span data-ttu-id="f8dfb-118">Чтобы задать вертикальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirY в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="f8dfb-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="f8dfb-119">Чтобы получить ссылку на ячейку ConLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8dfb-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-120">Cell name:</span></span>  <br/> | <span data-ttu-id="f8dfb-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="f8dfb-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="f8dfb-122">Чтобы получить ссылку на ячейку ConLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8dfb-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-123">Section index:</span></span>  <br/> |<span data-ttu-id="f8dfb-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8dfb-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-125">Row index:</span></span>  <br/> |<span data-ttu-id="f8dfb-126">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="f8dfb-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f8dfb-127">Cell index:</span></span>  <br/> |<span data-ttu-id="f8dfb-128">**Виссложумпдири**</span><span class="sxs-lookup"><span data-stu-id="f8dfb-128">**visSLOJumpDirY**</span></span> <br/> |
   

