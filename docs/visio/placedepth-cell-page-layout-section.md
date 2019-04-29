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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432039"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="22131-103">PlaceDepth Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="22131-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="22131-104">Определяет метод, с помощью которого анализируется документ перед созданием макета, и определяет тип макета.</span><span class="sxs-lookup"><span data-stu-id="22131-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="22131-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="22131-105">**Value**</span></span>|<span data-ttu-id="22131-106">**Глубина размещения для вертикальных и горизонтальных макетов**</span><span class="sxs-lookup"><span data-stu-id="22131-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="22131-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="22131-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="22131-108">нуль</span><span class="sxs-lookup"><span data-stu-id="22131-108">0</span></span>  <br/> | <span data-ttu-id="22131-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="22131-109">Page default</span></span>  <br/> |<span data-ttu-id="22131-110">**Висплоплацедепсдефаулт**</span><span class="sxs-lookup"><span data-stu-id="22131-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="22131-111">1,1</span><span class="sxs-lookup"><span data-stu-id="22131-111">1</span></span>  <br/> | <span data-ttu-id="22131-112">Средняя</span><span class="sxs-lookup"><span data-stu-id="22131-112">Medium</span></span>  <br/> |<span data-ttu-id="22131-113">**Висплоплацедепсмедиум**</span><span class="sxs-lookup"><span data-stu-id="22131-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="22131-114">2</span><span class="sxs-lookup"><span data-stu-id="22131-114">2</span></span>  <br/> | <span data-ttu-id="22131-115">Углублен</span><span class="sxs-lookup"><span data-stu-id="22131-115">Deep</span></span>  <br/> |<span data-ttu-id="22131-116">**Висплоплацедепсдип**</span><span class="sxs-lookup"><span data-stu-id="22131-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="22131-117">4</span><span class="sxs-lookup"><span data-stu-id="22131-117">3</span></span>  <br/> | <span data-ttu-id="22131-118">Поверхност</span><span class="sxs-lookup"><span data-stu-id="22131-118">Shallow</span></span>  <br/> |<span data-ttu-id="22131-119">**Висплоплацедепсшаллов**</span><span class="sxs-lookup"><span data-stu-id="22131-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22131-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="22131-120">Remarks</span></span>

<span data-ttu-id="22131-121">Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="22131-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22131-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="22131-122">Cell name:</span></span>  <br/> | <span data-ttu-id="22131-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="22131-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="22131-124">Чтобы получить ссылку на ячейку PlaceDepth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="22131-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22131-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="22131-125">Section index:</span></span>  <br/> |<span data-ttu-id="22131-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="22131-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="22131-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="22131-127">Row index:</span></span>  <br/> |<span data-ttu-id="22131-128">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="22131-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="22131-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="22131-129">Cell index:</span></span>  <br/> |<span data-ttu-id="22131-130">**Висплоплацедепс**</span><span class="sxs-lookup"><span data-stu-id="22131-130">**visPLOPlaceDepth**</span></span> <br/> |
   

