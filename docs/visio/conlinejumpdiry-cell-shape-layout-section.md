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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342744"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="8a237-103">ConLineJumpDirY Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="8a237-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="8a237-104">Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="8a237-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="8a237-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8a237-105">**Value**</span></span>|<span data-ttu-id="8a237-106">**Направление пересечения линий**</span><span class="sxs-lookup"><span data-stu-id="8a237-106">**Line Jump Direction**</span></span>|<span data-ttu-id="8a237-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="8a237-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8a237-108">нуль</span><span class="sxs-lookup"><span data-stu-id="8a237-108">0</span></span>  <br/> | <span data-ttu-id="8a237-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8a237-109">Page default</span></span>  <br/> |<span data-ttu-id="8a237-110">**Висложумпдиридефаулт**</span><span class="sxs-lookup"><span data-stu-id="8a237-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="8a237-111">1,1</span><span class="sxs-lookup"><span data-stu-id="8a237-111">1</span></span>  <br/> | <span data-ttu-id="8a237-112">Left</span><span class="sxs-lookup"><span data-stu-id="8a237-112">Left</span></span>  <br/> |<span data-ttu-id="8a237-113">**Висложумпдирилефт**</span><span class="sxs-lookup"><span data-stu-id="8a237-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="8a237-114">2</span><span class="sxs-lookup"><span data-stu-id="8a237-114">2</span></span>  <br/> | <span data-ttu-id="8a237-115">Right</span><span class="sxs-lookup"><span data-stu-id="8a237-115">Right</span></span>  <br/> |<span data-ttu-id="8a237-116">**Висложумпдириригхт**</span><span class="sxs-lookup"><span data-stu-id="8a237-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a237-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a237-117">Remarks</span></span>

<span data-ttu-id="8a237-118">Чтобы задать вертикальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirY в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="8a237-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="8a237-119">Чтобы получить ссылку на ячейку ConLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="8a237-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a237-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8a237-120">Cell name:</span></span>  <br/> | <span data-ttu-id="8a237-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="8a237-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="8a237-122">Чтобы получить ссылку на ячейку ConLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8a237-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a237-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8a237-123">Section index:</span></span>  <br/> |<span data-ttu-id="8a237-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8a237-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8a237-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8a237-125">Row index:</span></span>  <br/> |<span data-ttu-id="8a237-126">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="8a237-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="8a237-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8a237-127">Cell index:</span></span>  <br/> |<span data-ttu-id="8a237-128">**Виссложумпдири**</span><span class="sxs-lookup"><span data-stu-id="8a237-128">**visSLOJumpDirY**</span></span> <br/> |
   

