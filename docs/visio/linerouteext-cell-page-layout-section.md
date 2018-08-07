---
title: Ячейка LineRouteExt (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Определяет вид по умолчанию для всех соединителей на странице документа.
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814101"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="666df-103">Ячейка LineRouteExt (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="666df-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="666df-104">Определяет вид по умолчанию для всех соединителей на странице документа.</span><span class="sxs-lookup"><span data-stu-id="666df-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="666df-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="666df-105">**Value**</span></span>|<span data-ttu-id="666df-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="666df-106">**Description**</span></span>|<span data-ttu-id="666df-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="666df-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="666df-108">0</span><span class="sxs-lookup"><span data-stu-id="666df-108">0</span></span>  <br/> | <span data-ttu-id="666df-109">По умолчанию (обычный)</span><span class="sxs-lookup"><span data-stu-id="666df-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="666df-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="666df-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="666df-111">1</span><span class="sxs-lookup"><span data-stu-id="666df-111">1</span></span>  <br/> | <span data-ttu-id="666df-112">Прямой</span><span class="sxs-lookup"><span data-stu-id="666df-112">Straight</span></span>  <br/> |<span data-ttu-id="666df-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="666df-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="666df-114">2</span><span class="sxs-lookup"><span data-stu-id="666df-114">2</span></span>  <br/> | <span data-ttu-id="666df-115">Круглая</span><span class="sxs-lookup"><span data-stu-id="666df-115">Curved</span></span>  <br/> |<span data-ttu-id="666df-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="666df-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="666df-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="666df-117">Remarks</span></span>

<span data-ttu-id="666df-118">Чтобы получить ссылку на ячейку LineRouteExt по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="666df-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="666df-119">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="666df-119">Cell name:</span></span>  <br/> | <span data-ttu-id="666df-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="666df-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="666df-121">Для получения ссылки на ячейки LineRouteExt по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="666df-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="666df-122">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="666df-122">Section index:</span></span>  <br/> |<span data-ttu-id="666df-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="666df-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="666df-124">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="666df-124">Row index:</span></span>  <br/> |<span data-ttu-id="666df-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="666df-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="666df-126">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="666df-126">Cell index:</span></span>  <br/> |<span data-ttu-id="666df-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="666df-127">**visPLOLineRouteExt**</span></span> <br/> |
   

