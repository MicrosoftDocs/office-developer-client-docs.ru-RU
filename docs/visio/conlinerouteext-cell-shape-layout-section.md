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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434615"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="255c7-103">ConLineRouteExt Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="255c7-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="255c7-104">Определяет внешний вид соединителя.</span><span class="sxs-lookup"><span data-stu-id="255c7-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="255c7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="255c7-105">**Value**</span></span>|<span data-ttu-id="255c7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="255c7-106">**Description**</span></span>|<span data-ttu-id="255c7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="255c7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="255c7-108">нуль</span><span class="sxs-lookup"><span data-stu-id="255c7-108">0</span></span>  <br/> | <span data-ttu-id="255c7-109">Умолчани использовать параметр страницы</span><span class="sxs-lookup"><span data-stu-id="255c7-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="255c7-110">**вислораутикстдефаулт**</span><span class="sxs-lookup"><span data-stu-id="255c7-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="255c7-111">1,1</span><span class="sxs-lookup"><span data-stu-id="255c7-111">1</span></span>  <br/> | <span data-ttu-id="255c7-112">Располагает</span><span class="sxs-lookup"><span data-stu-id="255c7-112">Straight</span></span>  <br/> |<span data-ttu-id="255c7-113">**вислораутикстстраигхт**</span><span class="sxs-lookup"><span data-stu-id="255c7-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="255c7-114">2</span><span class="sxs-lookup"><span data-stu-id="255c7-114">2</span></span>  <br/> | <span data-ttu-id="255c7-115">Прямолинейны</span><span class="sxs-lookup"><span data-stu-id="255c7-115">Curved</span></span>  <br/> |<span data-ttu-id="255c7-116">**вислораутикстнурбс**</span><span class="sxs-lookup"><span data-stu-id="255c7-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="255c7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="255c7-117">Remarks</span></span>

<span data-ttu-id="255c7-118">Чтобы получить ссылку на ячейку ConLineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="255c7-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="255c7-119">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="255c7-119">Cell name:</span></span>  <br/> | <span data-ttu-id="255c7-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="255c7-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="255c7-121">Чтобы получить ссылку на ячейку ConLineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="255c7-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="255c7-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="255c7-122">Section index:</span></span>  <br/> |<span data-ttu-id="255c7-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="255c7-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="255c7-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="255c7-124">Row index:</span></span>  <br/> |<span data-ttu-id="255c7-125">**висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="255c7-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="255c7-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="255c7-126">Cell index:</span></span>  <br/> |<span data-ttu-id="255c7-127">**висслолинераутикст**</span><span class="sxs-lookup"><span data-stu-id="255c7-127">**visSLOLineRouteExt**</span></span> <br/> |
   

