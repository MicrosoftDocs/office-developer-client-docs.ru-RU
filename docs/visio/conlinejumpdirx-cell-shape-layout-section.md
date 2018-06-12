---
title: Ячейка ConLineJumpDirX (раздел макет фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813458"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="ed057-103">Ячейка ConLineJumpDirX (раздел макет фигуры)</span><span class="sxs-lookup"><span data-stu-id="ed057-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ed057-104">Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ed057-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="ed057-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ed057-105">**Value**</span></span>|<span data-ttu-id="ed057-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="ed057-106">**Line jump direction**</span></span>|<span data-ttu-id="ed057-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ed057-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ed057-108">0</span><span class="sxs-lookup"><span data-stu-id="ed057-108">0</span></span>  <br/> | <span data-ttu-id="ed057-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ed057-109">Page default</span></span>  <br/> |<span data-ttu-id="ed057-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="ed057-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="ed057-111">1</span><span class="sxs-lookup"><span data-stu-id="ed057-111">1</span></span>  <br/> | <span data-ttu-id="ed057-112">Вверх </span><span class="sxs-lookup"><span data-stu-id="ed057-112">Up</span></span>  <br/> |<span data-ttu-id="ed057-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="ed057-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="ed057-114">2</span><span class="sxs-lookup"><span data-stu-id="ed057-114">2</span></span>  <br/> | <span data-ttu-id="ed057-115">Вниз</span><span class="sxs-lookup"><span data-stu-id="ed057-115">Down</span></span>  <br/> |<span data-ttu-id="ed057-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="ed057-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed057-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed057-117">Remarks</span></span>

<span data-ttu-id="ed057-118">По умолчанию горизонтали для *всех* соединителей переходит на страницу, использовать ячейку PageLineJumpDirX в разделе макет страницы.</span><span class="sxs-lookup"><span data-stu-id="ed057-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="ed057-119">Чтобы получить ссылку на ячейку ConLineJumpDirX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ed057-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed057-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="ed057-120">Cell name:</span></span>  <br/> | <span data-ttu-id="ed057-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="ed057-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="ed057-122">Для получения ссылки на ячейки ConLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="ed057-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed057-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ed057-123">Section index:</span></span>  <br/> |<span data-ttu-id="ed057-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed057-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed057-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ed057-125">Row index:</span></span>  <br/> |<span data-ttu-id="ed057-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ed057-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ed057-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ed057-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ed057-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="ed057-128">**visSLOJumpDirX**</span></span> <br/> |
   

