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
description: Определяет метод, с помощью которого анализируется документ перед созданием макета, и определяет тип макета.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346797"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="e092f-103">PlaceDepth Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e092f-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="e092f-104">Определяет метод, с помощью которого анализируется документ перед созданием макета, и определяет тип макета.</span><span class="sxs-lookup"><span data-stu-id="e092f-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="e092f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e092f-105">**Value**</span></span>|<span data-ttu-id="e092f-106">**Глубина размещения для вертикальных и горизонтальных макетов**</span><span class="sxs-lookup"><span data-stu-id="e092f-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="e092f-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e092f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e092f-108">нуль</span><span class="sxs-lookup"><span data-stu-id="e092f-108">0</span></span>  <br/> | <span data-ttu-id="e092f-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e092f-109">Page default</span></span>  <br/> |<span data-ttu-id="e092f-110">**Висплоплацедепсдефаулт**</span><span class="sxs-lookup"><span data-stu-id="e092f-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="e092f-111">1,1</span><span class="sxs-lookup"><span data-stu-id="e092f-111">1</span></span>  <br/> | <span data-ttu-id="e092f-112">Средние</span><span class="sxs-lookup"><span data-stu-id="e092f-112">Medium</span></span>  <br/> |<span data-ttu-id="e092f-113">**Висплоплацедепсмедиум**</span><span class="sxs-lookup"><span data-stu-id="e092f-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="e092f-114">2</span><span class="sxs-lookup"><span data-stu-id="e092f-114">2</span></span>  <br/> | <span data-ttu-id="e092f-115">Углублен</span><span class="sxs-lookup"><span data-stu-id="e092f-115">Deep</span></span>  <br/> |<span data-ttu-id="e092f-116">**Висплоплацедепсдип**</span><span class="sxs-lookup"><span data-stu-id="e092f-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="e092f-117">4</span><span class="sxs-lookup"><span data-stu-id="e092f-117">3</span></span>  <br/> | <span data-ttu-id="e092f-118">Поверхност</span><span class="sxs-lookup"><span data-stu-id="e092f-118">Shallow</span></span>  <br/> |<span data-ttu-id="e092f-119">**Висплоплацедепсшаллов**</span><span class="sxs-lookup"><span data-stu-id="e092f-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e092f-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e092f-120">Remarks</span></span>

<span data-ttu-id="e092f-121">Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="e092f-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e092f-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e092f-122">Cell name:</span></span>  <br/> | <span data-ttu-id="e092f-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="e092f-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="e092f-124">Чтобы получить ссылку на ячейку PlaceDepth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e092f-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e092f-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e092f-125">Section index:</span></span>  <br/> |<span data-ttu-id="e092f-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e092f-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e092f-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e092f-127">Row index:</span></span>  <br/> |<span data-ttu-id="e092f-128">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="e092f-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e092f-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e092f-129">Cell index:</span></span>  <br/> |<span data-ttu-id="e092f-130">**Висплоплацедепс**</span><span class="sxs-lookup"><span data-stu-id="e092f-130">**visPLOPlaceDepth**</span></span> <br/> |
   

