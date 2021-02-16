---
title: PlaceDepth Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Определяет метод, с помощью которого анализировался рисунок перед созданием макета, и определяет тип макета.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432039"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="3912e-103">PlaceDepth Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="3912e-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="3912e-104">Определяет метод, с помощью которого анализировался рисунок перед созданием макета, и определяет тип макета.</span><span class="sxs-lookup"><span data-stu-id="3912e-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="3912e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3912e-105">**Value**</span></span>|<span data-ttu-id="3912e-106">**Глубина размещения для вертикальных и горизонтальных макетов**</span><span class="sxs-lookup"><span data-stu-id="3912e-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="3912e-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="3912e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3912e-108">0</span><span class="sxs-lookup"><span data-stu-id="3912e-108">0</span></span>  <br/> | <span data-ttu-id="3912e-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3912e-109">Page default</span></span>  <br/> |<span data-ttu-id="3912e-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="3912e-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="3912e-111">1 </span><span class="sxs-lookup"><span data-stu-id="3912e-111">1</span></span>  <br/> | <span data-ttu-id="3912e-112">Средняя</span><span class="sxs-lookup"><span data-stu-id="3912e-112">Medium</span></span>  <br/> |<span data-ttu-id="3912e-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="3912e-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="3912e-114">2 </span><span class="sxs-lookup"><span data-stu-id="3912e-114">2</span></span>  <br/> | <span data-ttu-id="3912e-115">Deep</span><span class="sxs-lookup"><span data-stu-id="3912e-115">Deep</span></span>  <br/> |<span data-ttu-id="3912e-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="3912e-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="3912e-117">3 </span><span class="sxs-lookup"><span data-stu-id="3912e-117">3</span></span>  <br/> | <span data-ttu-id="3912e-118">Поверхностное</span><span class="sxs-lookup"><span data-stu-id="3912e-118">Shallow</span></span>  <br/> |<span data-ttu-id="3912e-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="3912e-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3912e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3912e-120">Remarks</span></span>

<span data-ttu-id="3912e-121">Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3912e-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3912e-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3912e-122">Cell name:</span></span>  <br/> | <span data-ttu-id="3912e-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="3912e-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="3912e-124">Чтобы получить ссылку на ячейку PlaceDepth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3912e-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3912e-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3912e-125">Section index:</span></span>  <br/> |<span data-ttu-id="3912e-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3912e-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3912e-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3912e-127">Row index:</span></span>  <br/> |<span data-ttu-id="3912e-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="3912e-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="3912e-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3912e-129">Cell index:</span></span>  <br/> |<span data-ttu-id="3912e-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="3912e-130">**visPLOPlaceDepth**</span></span> <br/> |
   

