---
title: LineRouteExt Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Определяет внешний вид по умолчанию для всех соединитеителей на странице рисования.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410625"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="a9216-103">LineRouteExt Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="a9216-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="a9216-104">Определяет внешний вид по умолчанию для всех соединитеителей на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="a9216-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="a9216-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a9216-105">**Value**</span></span>|<span data-ttu-id="a9216-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9216-106">**Description**</span></span>|<span data-ttu-id="a9216-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a9216-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a9216-108">0</span><span class="sxs-lookup"><span data-stu-id="a9216-108">0</span></span>  <br/> | <span data-ttu-id="a9216-109">По умолчанию (прямо)</span><span class="sxs-lookup"><span data-stu-id="a9216-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="a9216-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="a9216-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="a9216-111">1 </span><span class="sxs-lookup"><span data-stu-id="a9216-111">1</span></span>  <br/> | <span data-ttu-id="a9216-112">Прямо</span><span class="sxs-lookup"><span data-stu-id="a9216-112">Straight</span></span>  <br/> |<span data-ttu-id="a9216-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="a9216-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="a9216-114">2 </span><span class="sxs-lookup"><span data-stu-id="a9216-114">2</span></span>  <br/> | <span data-ttu-id="a9216-115">Curved</span><span class="sxs-lookup"><span data-stu-id="a9216-115">Curved</span></span>  <br/> |<span data-ttu-id="a9216-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="a9216-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9216-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9216-117">Remarks</span></span>

<span data-ttu-id="a9216-118">Чтобы получить ссылку на ячейку LineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a9216-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9216-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a9216-119">Cell name:</span></span>  <br/> | <span data-ttu-id="a9216-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="a9216-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="a9216-121">Чтобы получить ссылку на ячейку LineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a9216-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9216-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a9216-122">Section index:</span></span>  <br/> |<span data-ttu-id="a9216-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9216-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a9216-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a9216-124">Row index:</span></span>  <br/> |<span data-ttu-id="a9216-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a9216-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a9216-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a9216-126">Cell index:</span></span>  <br/> |<span data-ttu-id="a9216-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="a9216-127">**visPLOLineRouteExt**</span></span> <br/> |
   

