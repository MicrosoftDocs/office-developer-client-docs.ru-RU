---
title: PageLineJumpDirX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Определяет направление переходов по горизонтальным динамическим соединитетелям на странице рисования, к которой не применено локальное направление перехода.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431010"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="0db00-103">PageLineJumpDirX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="0db00-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="0db00-104">Определяет направление переходов по горизонтальным динамическим соединитетелям на странице рисования, к которой не применено локальное направление перехода.</span><span class="sxs-lookup"><span data-stu-id="0db00-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="0db00-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0db00-105">**Value**</span></span>|<span data-ttu-id="0db00-106">**Направление перехода по строке**</span><span class="sxs-lookup"><span data-stu-id="0db00-106">**Line jump direction**</span></span>|<span data-ttu-id="0db00-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="0db00-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0db00-108">0</span><span class="sxs-lookup"><span data-stu-id="0db00-108">0</span></span>  <br/> | <span data-ttu-id="0db00-109">По умолчанию; слева или параметр страницы для фигур</span><span class="sxs-lookup"><span data-stu-id="0db00-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="0db00-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="0db00-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="0db00-111">1 </span><span class="sxs-lookup"><span data-stu-id="0db00-111">1</span></span>  <br/> | <span data-ttu-id="0db00-112">Вверх</span><span class="sxs-lookup"><span data-stu-id="0db00-112">Up</span></span>  <br/> |<span data-ttu-id="0db00-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="0db00-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="0db00-114">2 </span><span class="sxs-lookup"><span data-stu-id="0db00-114">2</span></span>  <br/> | <span data-ttu-id="0db00-115">Вниз</span><span class="sxs-lookup"><span data-stu-id="0db00-115">Down</span></span>  <br/> |<span data-ttu-id="0db00-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="0db00-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0db00-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0db00-117">Remarks</span></span>

<span data-ttu-id="0db00-118">Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0db00-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0db00-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0db00-119">Cell name:</span></span>  <br/> | <span data-ttu-id="0db00-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="0db00-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="0db00-121">Чтобы получить ссылку на ячейку PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0db00-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0db00-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0db00-122">Section index:</span></span>  <br/> |<span data-ttu-id="0db00-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0db00-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0db00-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0db00-124">Row index:</span></span>  <br/> |<span data-ttu-id="0db00-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0db00-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0db00-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0db00-126">Cell index:</span></span>  <br/> |<span data-ttu-id="0db00-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="0db00-127">**visPLOJumpDirX**</span></span> <br/> |
   

