---
title: Ячейка PageLineJumpDirX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Определяет направление строки пересечения на горизонтальную динамических соединители на странице документа, для которого не применяются локальные направление.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814338"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="dda64-103">Ячейка PageLineJumpDirX (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="dda64-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="dda64-104">Определяет направление строки пересечения на горизонтальную динамических соединители на странице документа, для которого не применяются локальные направление.</span><span class="sxs-lookup"><span data-stu-id="dda64-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="dda64-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="dda64-105">**Value**</span></span>|<span data-ttu-id="dda64-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="dda64-106">**Line jump direction**</span></span>|<span data-ttu-id="dda64-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="dda64-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="dda64-108">0</span><span class="sxs-lookup"><span data-stu-id="dda64-108">0</span></span>  <br/> | <span data-ttu-id="dda64-109">По умолчанию; слева или параметров страницы для фигур</span><span class="sxs-lookup"><span data-stu-id="dda64-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="dda64-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="dda64-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="dda64-111">1</span><span class="sxs-lookup"><span data-stu-id="dda64-111">1</span></span>  <br/> | <span data-ttu-id="dda64-112">Вверх </span><span class="sxs-lookup"><span data-stu-id="dda64-112">Up</span></span>  <br/> |<span data-ttu-id="dda64-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="dda64-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="dda64-114">2</span><span class="sxs-lookup"><span data-stu-id="dda64-114">2</span></span>  <br/> | <span data-ttu-id="dda64-115">Вниз</span><span class="sxs-lookup"><span data-stu-id="dda64-115">Down</span></span>  <br/> |<span data-ttu-id="dda64-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="dda64-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dda64-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="dda64-117">Remarks</span></span>

<span data-ttu-id="dda64-118">Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dda64-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dda64-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="dda64-119">Cell name:</span></span>  <br/> | <span data-ttu-id="dda64-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="dda64-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="dda64-121">Для получения ссылки на ячейки PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dda64-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dda64-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dda64-122">Section index:</span></span>  <br/> |<span data-ttu-id="dda64-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dda64-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dda64-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dda64-124">Row index:</span></span>  <br/> |<span data-ttu-id="dda64-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="dda64-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="dda64-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dda64-126">Cell index:</span></span>  <br/> |<span data-ttu-id="dda64-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="dda64-127">**visPLOJumpDirX**</span></span> <br/> |
   

