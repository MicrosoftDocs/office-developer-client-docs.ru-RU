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
description: Определяет направление пересечения линий на горизонтальных динамических соединительных линиях на странице документа, для которых вы не применили локальное направление перехода.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431010"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="cb800-103">PageLineJumpDirX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="cb800-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="cb800-104">Определяет направление пересечения линий на горизонтальных динамических соединительных линиях на странице документа, для которых вы не применили локальное направление перехода.</span><span class="sxs-lookup"><span data-stu-id="cb800-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="cb800-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="cb800-105">**Value**</span></span>|<span data-ttu-id="cb800-106">**Направление пересечения линий**</span><span class="sxs-lookup"><span data-stu-id="cb800-106">**Line jump direction**</span></span>|<span data-ttu-id="cb800-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="cb800-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="cb800-108">нуль</span><span class="sxs-lookup"><span data-stu-id="cb800-108">0</span></span>  <br/> | <span data-ttu-id="cb800-109">Умолчани слева или параметры страницы для фигур</span><span class="sxs-lookup"><span data-stu-id="cb800-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="cb800-110">**Висложумпдирксдефаулт**</span><span class="sxs-lookup"><span data-stu-id="cb800-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="cb800-111">1,1</span><span class="sxs-lookup"><span data-stu-id="cb800-111">1</span></span>  <br/> | <span data-ttu-id="cb800-112">Настройка</span><span class="sxs-lookup"><span data-stu-id="cb800-112">Up</span></span>  <br/> |<span data-ttu-id="cb800-113">**Висложумпдирксуп**</span><span class="sxs-lookup"><span data-stu-id="cb800-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="cb800-114">2</span><span class="sxs-lookup"><span data-stu-id="cb800-114">2</span></span>  <br/> | <span data-ttu-id="cb800-115">Понижен</span><span class="sxs-lookup"><span data-stu-id="cb800-115">Down</span></span>  <br/> |<span data-ttu-id="cb800-116">**Висложумпдирксдовн**</span><span class="sxs-lookup"><span data-stu-id="cb800-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb800-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb800-117">Remarks</span></span>

<span data-ttu-id="cb800-118">Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="cb800-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb800-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="cb800-119">Cell name:</span></span>  <br/> | <span data-ttu-id="cb800-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="cb800-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="cb800-121">Чтобы получить ссылку на ячейку PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="cb800-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cb800-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cb800-122">Section index:</span></span>  <br/> |<span data-ttu-id="cb800-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cb800-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cb800-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cb800-124">Row index:</span></span>  <br/> |<span data-ttu-id="cb800-125">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="cb800-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="cb800-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cb800-126">Cell index:</span></span>  <br/> |<span data-ttu-id="cb800-127">**Виспложумпдиркс**</span><span class="sxs-lookup"><span data-stu-id="cb800-127">**visPLOJumpDirX**</span></span> <br/> |
   

