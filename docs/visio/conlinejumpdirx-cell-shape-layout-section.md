---
title: ConLineJumpDirX Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342751"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="7e456-103">ConLineJumpDirX Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="7e456-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7e456-104">Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="7e456-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="7e456-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7e456-105">**Value**</span></span>|<span data-ttu-id="7e456-106">**Направление пересечения линий**</span><span class="sxs-lookup"><span data-stu-id="7e456-106">**Line jump direction**</span></span>|<span data-ttu-id="7e456-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7e456-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7e456-108">нуль</span><span class="sxs-lookup"><span data-stu-id="7e456-108">0</span></span>  <br/> | <span data-ttu-id="7e456-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7e456-109">Page default</span></span>  <br/> |<span data-ttu-id="7e456-110">**Висложумпдирксдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7e456-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="7e456-111">1,1</span><span class="sxs-lookup"><span data-stu-id="7e456-111">1</span></span>  <br/> | <span data-ttu-id="7e456-112">Настройка</span><span class="sxs-lookup"><span data-stu-id="7e456-112">Up</span></span>  <br/> |<span data-ttu-id="7e456-113">**Висложумпдирксуп**</span><span class="sxs-lookup"><span data-stu-id="7e456-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="7e456-114">2</span><span class="sxs-lookup"><span data-stu-id="7e456-114">2</span></span>  <br/> | <span data-ttu-id="7e456-115">Понижен</span><span class="sxs-lookup"><span data-stu-id="7e456-115">Down</span></span>  <br/> |<span data-ttu-id="7e456-116">**Висложумпдирксдовн**</span><span class="sxs-lookup"><span data-stu-id="7e456-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e456-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e456-117">Remarks</span></span>

<span data-ttu-id="7e456-118">Чтобы задать горизонтальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirX в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="7e456-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="7e456-119">Чтобы получить ссылку на ячейку ConLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="7e456-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e456-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7e456-120">Cell name:</span></span>  <br/> | <span data-ttu-id="7e456-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="7e456-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="7e456-122">Чтобы получить ссылку на ячейку ConLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7e456-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e456-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7e456-123">Section index:</span></span>  <br/> |<span data-ttu-id="7e456-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7e456-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7e456-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7e456-125">Row index:</span></span>  <br/> |<span data-ttu-id="7e456-126">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="7e456-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="7e456-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7e456-127">Cell index:</span></span>  <br/> |<span data-ttu-id="7e456-128">**Виссложумпдиркс**</span><span class="sxs-lookup"><span data-stu-id="7e456-128">**visSLOJumpDirX**</span></span> <br/> |
   

