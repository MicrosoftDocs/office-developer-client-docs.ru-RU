---
title: Ячейка PlaceDepth (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Определяет способ, с помощью которого выполняется анализ перед созданием макет документа и определяет тип макета.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814362"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="da506-103">Ячейка PlaceDepth (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="da506-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="da506-104">Определяет способ, с помощью которого выполняется анализ перед созданием макет документа и определяет тип макета.</span><span class="sxs-lookup"><span data-stu-id="da506-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="da506-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="da506-105">**Value**</span></span>|<span data-ttu-id="da506-106">**Размещение глубины вертикальных и горизонтальных макетов страниц**</span><span class="sxs-lookup"><span data-stu-id="da506-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="da506-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="da506-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="da506-108">0</span><span class="sxs-lookup"><span data-stu-id="da506-108">0</span></span>  <br/> | <span data-ttu-id="da506-109">Страница по умолчанию</span><span class="sxs-lookup"><span data-stu-id="da506-109">Page default</span></span>  <br/> |<span data-ttu-id="da506-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="da506-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="da506-111">1</span><span class="sxs-lookup"><span data-stu-id="da506-111">1</span></span>  <br/> | <span data-ttu-id="da506-112">Средний</span><span class="sxs-lookup"><span data-stu-id="da506-112">Medium</span></span>  <br/> |<span data-ttu-id="da506-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="da506-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="da506-114">2</span><span class="sxs-lookup"><span data-stu-id="da506-114">2</span></span>  <br/> | <span data-ttu-id="da506-115">Глубокое</span><span class="sxs-lookup"><span data-stu-id="da506-115">Deep</span></span>  <br/> |<span data-ttu-id="da506-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="da506-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="da506-117">3</span><span class="sxs-lookup"><span data-stu-id="da506-117">3</span></span>  <br/> | <span data-ttu-id="da506-118">Неполная</span><span class="sxs-lookup"><span data-stu-id="da506-118">Shallow</span></span>  <br/> |<span data-ttu-id="da506-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="da506-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da506-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="da506-120">Remarks</span></span>

<span data-ttu-id="da506-121">Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="da506-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="da506-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="da506-122">Cell name:</span></span>  <br/> | <span data-ttu-id="da506-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="da506-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="da506-124">Для получения ссылки на ячейки PlaceDepth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="da506-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="da506-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="da506-125">Section index:</span></span>  <br/> |<span data-ttu-id="da506-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="da506-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="da506-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="da506-127">Row index:</span></span>  <br/> |<span data-ttu-id="da506-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="da506-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="da506-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="da506-129">Cell index:</span></span>  <br/> |<span data-ttu-id="da506-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="da506-130">**visPLOPlaceDepth**</span></span> <br/> |
   

