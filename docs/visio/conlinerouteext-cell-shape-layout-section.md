---
title: ConLineRouteExt Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Определяет внешний вид соединителя.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327106"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="ab5d9-103">ConLineRouteExt Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ab5d9-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ab5d9-104">Определяет внешний вид соединителя.</span><span class="sxs-lookup"><span data-stu-id="ab5d9-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="ab5d9-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-105">**Value**</span></span>|<span data-ttu-id="ab5d9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-106">**Description**</span></span>|<span data-ttu-id="ab5d9-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ab5d9-108">нуль</span><span class="sxs-lookup"><span data-stu-id="ab5d9-108">0</span></span>  <br/> | <span data-ttu-id="ab5d9-109">Умолчани использовать параметр страницы</span><span class="sxs-lookup"><span data-stu-id="ab5d9-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="ab5d9-110">**Вислораутикстдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="ab5d9-111">1,1</span><span class="sxs-lookup"><span data-stu-id="ab5d9-111">1</span></span>  <br/> | <span data-ttu-id="ab5d9-112">Располагает</span><span class="sxs-lookup"><span data-stu-id="ab5d9-112">Straight</span></span>  <br/> |<span data-ttu-id="ab5d9-113">**Вислораутикстстраигхт**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="ab5d9-114">2</span><span class="sxs-lookup"><span data-stu-id="ab5d9-114">2</span></span>  <br/> | <span data-ttu-id="ab5d9-115">Прямолинейны</span><span class="sxs-lookup"><span data-stu-id="ab5d9-115">Curved</span></span>  <br/> |<span data-ttu-id="ab5d9-116">**Вислораутикстнурбс**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab5d9-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="ab5d9-117">Remarks</span></span>

<span data-ttu-id="ab5d9-118">Чтобы получить ссылку на ячейку ConLineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab5d9-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ab5d9-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="ab5d9-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="ab5d9-121">Чтобы получить ссылку на ячейку ConLineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ab5d9-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-122">Section index:</span></span>  <br/> |<span data-ttu-id="ab5d9-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ab5d9-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-124">Row index:</span></span>  <br/> |<span data-ttu-id="ab5d9-125">**Висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ab5d9-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ab5d9-126">Cell index:</span></span>  <br/> |<span data-ttu-id="ab5d9-127">**Висслолинераутикст**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-127">**visSLOLineRouteExt**</span></span> <br/> |
   

