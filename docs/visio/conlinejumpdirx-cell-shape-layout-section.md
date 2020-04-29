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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415042"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="7b706-103">ConLineJumpDirX Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="7b706-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7b706-104">Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b706-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="7b706-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7b706-105">**Value**</span></span>|<span data-ttu-id="7b706-106">**Направление пересечения линий**</span><span class="sxs-lookup"><span data-stu-id="7b706-106">**Line jump direction**</span></span>|<span data-ttu-id="7b706-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7b706-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7b706-108">нуль</span><span class="sxs-lookup"><span data-stu-id="7b706-108">0</span></span>  <br/> | <span data-ttu-id="7b706-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7b706-109">Page default</span></span>  <br/> |<span data-ttu-id="7b706-110">**висложумпдирксдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7b706-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="7b706-111">1,1</span><span class="sxs-lookup"><span data-stu-id="7b706-111">1</span></span>  <br/> | <span data-ttu-id="7b706-112">Настройка</span><span class="sxs-lookup"><span data-stu-id="7b706-112">Up</span></span>  <br/> |<span data-ttu-id="7b706-113">**висложумпдирксуп**</span><span class="sxs-lookup"><span data-stu-id="7b706-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="7b706-114">2</span><span class="sxs-lookup"><span data-stu-id="7b706-114">2</span></span>  <br/> | <span data-ttu-id="7b706-115">Понижен</span><span class="sxs-lookup"><span data-stu-id="7b706-115">Down</span></span>  <br/> |<span data-ttu-id="7b706-116">**висложумпдирксдовн**</span><span class="sxs-lookup"><span data-stu-id="7b706-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b706-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="7b706-117">Remarks</span></span>

<span data-ttu-id="7b706-118">Чтобы задать горизонтальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirX в разделе Макет страницы.</span><span class="sxs-lookup"><span data-stu-id="7b706-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="7b706-119">Чтобы получить ссылку на ячейку ConLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="7b706-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b706-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7b706-120">Cell name:</span></span>  <br/> | <span data-ttu-id="7b706-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="7b706-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="7b706-122">Чтобы получить ссылку на ячейку ConLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7b706-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b706-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7b706-123">Section index:</span></span>  <br/> |<span data-ttu-id="7b706-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b706-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7b706-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7b706-125">Row index:</span></span>  <br/> |<span data-ttu-id="7b706-126">**висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="7b706-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="7b706-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7b706-127">Cell index:</span></span>  <br/> |<span data-ttu-id="7b706-128">**виссложумпдиркс**</span><span class="sxs-lookup"><span data-stu-id="7b706-128">**visSLOJumpDirX**</span></span> <br/> |
   

