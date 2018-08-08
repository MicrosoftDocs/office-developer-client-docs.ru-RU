---
title: Ячейка ConLineRouteExt (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Определяет внешний соединитель.
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813464"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="02de4-103">Ячейка ConLineRouteExt (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="02de4-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="02de4-104">Определяет внешний соединитель.</span><span class="sxs-lookup"><span data-stu-id="02de4-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="02de4-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="02de4-105">**Value**</span></span>|<span data-ttu-id="02de4-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02de4-106">**Description**</span></span>|<span data-ttu-id="02de4-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="02de4-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="02de4-108">0</span><span class="sxs-lookup"><span data-stu-id="02de4-108">0</span></span>  <br/> | <span data-ttu-id="02de4-109">По умолчанию; Использование параметров страницы</span><span class="sxs-lookup"><span data-stu-id="02de4-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="02de4-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="02de4-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="02de4-111">1</span><span class="sxs-lookup"><span data-stu-id="02de4-111">1</span></span>  <br/> | <span data-ttu-id="02de4-112">Прямой</span><span class="sxs-lookup"><span data-stu-id="02de4-112">Straight</span></span>  <br/> |<span data-ttu-id="02de4-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="02de4-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="02de4-114">2</span><span class="sxs-lookup"><span data-stu-id="02de4-114">2</span></span>  <br/> | <span data-ttu-id="02de4-115">Круглая</span><span class="sxs-lookup"><span data-stu-id="02de4-115">Curved</span></span>  <br/> |<span data-ttu-id="02de4-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="02de4-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02de4-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="02de4-117">Remarks</span></span>

<span data-ttu-id="02de4-118">Чтобы получить ссылку на ячейку ConLineRouteExt по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="02de4-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02de4-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="02de4-119">Cell name:</span></span>  <br/> | <span data-ttu-id="02de4-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="02de4-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="02de4-121">Для получения ссылки на ячейки ConLineRouteExt по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="02de4-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02de4-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="02de4-122">Section index:</span></span>  <br/> |<span data-ttu-id="02de4-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02de4-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="02de4-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="02de4-124">Row index:</span></span>  <br/> |<span data-ttu-id="02de4-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="02de4-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="02de4-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="02de4-126">Cell index:</span></span>  <br/> |<span data-ttu-id="02de4-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="02de4-127">**visSLOLineRouteExt**</span></span> <br/> |
   

