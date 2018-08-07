---
title: Ячейка PageLineJumpDirY (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Определяет направление строки пересечения на вертикальной динамической соединители на странице документа, для которого не применяются локальные направление.
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814349"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="6a6cb-103">Ячейка PageLineJumpDirY (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="6a6cb-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="6a6cb-104">Определяет направление строки пересечения на вертикальной динамической соединители на странице документа, для которого не применяются локальные направление.</span><span class="sxs-lookup"><span data-stu-id="6a6cb-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="6a6cb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-105">**Value**</span></span>|<span data-ttu-id="6a6cb-106">**Направление**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-106">**Line jump direction**</span></span>|<span data-ttu-id="6a6cb-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6a6cb-108">0</span><span class="sxs-lookup"><span data-stu-id="6a6cb-108">0</span></span>  <br/> | <span data-ttu-id="6a6cb-109">По умолчанию; вверх или параметров страницы для фигур</span><span class="sxs-lookup"><span data-stu-id="6a6cb-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="6a6cb-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="6a6cb-111">1</span><span class="sxs-lookup"><span data-stu-id="6a6cb-111">1</span></span>  <br/> | <span data-ttu-id="6a6cb-112">Left</span><span class="sxs-lookup"><span data-stu-id="6a6cb-112">Left</span></span>  <br/> |<span data-ttu-id="6a6cb-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="6a6cb-114">2</span><span class="sxs-lookup"><span data-stu-id="6a6cb-114">2</span></span>  <br/> | <span data-ttu-id="6a6cb-115">Right</span><span class="sxs-lookup"><span data-stu-id="6a6cb-115">Right</span></span>  <br/> |<span data-ttu-id="6a6cb-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a6cb-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a6cb-117">Remarks</span></span>

<span data-ttu-id="6a6cb-118">Чтобы получить ссылку на ячейку PageLineJumpDirY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6a6cb-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a6cb-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6a6cb-119">Cell name:</span></span>  <br/> | <span data-ttu-id="6a6cb-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="6a6cb-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="6a6cb-121">Для получения ссылки на ячейки PageLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6a6cb-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a6cb-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6a6cb-122">Section index:</span></span>  <br/> |<span data-ttu-id="6a6cb-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a6cb-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6a6cb-124">Row index:</span></span>  <br/> |<span data-ttu-id="6a6cb-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="6a6cb-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6a6cb-126">Cell index:</span></span>  <br/> |<span data-ttu-id="6a6cb-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="6a6cb-127">**visPLOJumpDirY**</span></span> <br/> |
   

