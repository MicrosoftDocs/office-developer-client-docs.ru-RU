---
title: Ячейка ConLineJumpDirY (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813446"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="86ed5-103">Ячейка ConLineJumpDirY (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="86ed5-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="86ed5-104">Определяет направление пересечения линий при пересечении вертикальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="86ed5-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="86ed5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="86ed5-105">**Value**</span></span>|<span data-ttu-id="86ed5-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="86ed5-106">**Line Jump Direction**</span></span>|<span data-ttu-id="86ed5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="86ed5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="86ed5-108">0</span><span class="sxs-lookup"><span data-stu-id="86ed5-108">0</span></span>  <br/> | <span data-ttu-id="86ed5-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="86ed5-109">Page default</span></span>  <br/> |<span data-ttu-id="86ed5-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="86ed5-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="86ed5-111">1</span><span class="sxs-lookup"><span data-stu-id="86ed5-111">1</span></span>  <br/> | <span data-ttu-id="86ed5-112">Left</span><span class="sxs-lookup"><span data-stu-id="86ed5-112">Left</span></span>  <br/> |<span data-ttu-id="86ed5-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="86ed5-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="86ed5-114">2</span><span class="sxs-lookup"><span data-stu-id="86ed5-114">2</span></span>  <br/> | <span data-ttu-id="86ed5-115">Right</span><span class="sxs-lookup"><span data-stu-id="86ed5-115">Right</span></span>  <br/> |<span data-ttu-id="86ed5-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="86ed5-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86ed5-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="86ed5-117">Remarks</span></span>

<span data-ttu-id="86ed5-118">По умолчанию вертикали для *всех* соединителей переходит на страницу, использовать ячейку PageLineJumpDirY в разделе макет страницы.</span><span class="sxs-lookup"><span data-stu-id="86ed5-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="86ed5-119">Чтобы получить ссылку на ячейку ConLineJumpDirY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="86ed5-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86ed5-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="86ed5-120">Cell name:</span></span>  <br/> | <span data-ttu-id="86ed5-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="86ed5-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="86ed5-122">Для получения ссылки на ячейки ConLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="86ed5-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86ed5-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="86ed5-123">Section index:</span></span>  <br/> |<span data-ttu-id="86ed5-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86ed5-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="86ed5-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="86ed5-125">Row index:</span></span>  <br/> |<span data-ttu-id="86ed5-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="86ed5-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="86ed5-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="86ed5-127">Cell index:</span></span>  <br/> |<span data-ttu-id="86ed5-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="86ed5-128">**visSLOJumpDirY**</span></span> <br/> |
   

