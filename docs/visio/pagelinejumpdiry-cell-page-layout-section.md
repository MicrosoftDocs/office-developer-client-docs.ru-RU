---
title: PageLineJumpDirY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Определяет направление переходов по вертикальным динамическим соединителям на странице рисования, к которой не применено локальное направление перехода.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414678"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="e543d-103">PageLineJumpDirY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e543d-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="e543d-104">Определяет направление переходов по вертикальным динамическим соединителям на странице рисования, к которой не применено локальное направление перехода.</span><span class="sxs-lookup"><span data-stu-id="e543d-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="e543d-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e543d-105">**Value**</span></span>|<span data-ttu-id="e543d-106">**Направление перехода по строке**</span><span class="sxs-lookup"><span data-stu-id="e543d-106">**Line jump direction**</span></span>|<span data-ttu-id="e543d-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e543d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e543d-108">0</span><span class="sxs-lookup"><span data-stu-id="e543d-108">0</span></span>  <br/> | <span data-ttu-id="e543d-109">По умолчанию; вверх или параметр страницы для фигур</span><span class="sxs-lookup"><span data-stu-id="e543d-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="e543d-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="e543d-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="e543d-111">1 </span><span class="sxs-lookup"><span data-stu-id="e543d-111">1</span></span>  <br/> | <span data-ttu-id="e543d-112">Left</span><span class="sxs-lookup"><span data-stu-id="e543d-112">Left</span></span>  <br/> |<span data-ttu-id="e543d-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="e543d-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="e543d-114">2 </span><span class="sxs-lookup"><span data-stu-id="e543d-114">2</span></span>  <br/> | <span data-ttu-id="e543d-115">Right</span><span class="sxs-lookup"><span data-stu-id="e543d-115">Right</span></span>  <br/> |<span data-ttu-id="e543d-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="e543d-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e543d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e543d-117">Remarks</span></span>

<span data-ttu-id="e543d-118">Чтобы получить ссылку на ячейку PageLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e543d-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e543d-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e543d-119">Cell name:</span></span>  <br/> | <span data-ttu-id="e543d-120">PageLineJumpDiry</span><span class="sxs-lookup"><span data-stu-id="e543d-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="e543d-121">Чтобы получить ссылку на ячейку PageLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e543d-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e543d-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e543d-122">Section index:</span></span>  <br/> |<span data-ttu-id="e543d-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e543d-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e543d-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e543d-124">Row index:</span></span>  <br/> |<span data-ttu-id="e543d-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e543d-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e543d-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e543d-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e543d-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="e543d-127">**visPLOJumpDirY**</span></span> <br/> |
   

