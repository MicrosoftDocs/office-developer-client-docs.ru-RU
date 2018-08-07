---
title: Ячейка PrintPageOrientation (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Определяет, будет ли страницы при печати книжная или альбомная ориентация.
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814492"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="143ba-103">Ячейка PrintPageOrientation (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="143ba-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="143ba-104">Определяет, будет ли страницы при печати книжная или альбомная ориентация.</span><span class="sxs-lookup"><span data-stu-id="143ba-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="143ba-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="143ba-105">**Value**</span></span>|<span data-ttu-id="143ba-106">**Ориентация**</span><span class="sxs-lookup"><span data-stu-id="143ba-106">**Orientation**</span></span>|<span data-ttu-id="143ba-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="143ba-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="143ba-108">0</span><span class="sxs-lookup"><span data-stu-id="143ba-108">0</span></span>  <br/> | <span data-ttu-id="143ba-109">То же, что принтера</span><span class="sxs-lookup"><span data-stu-id="143ba-109">Same as printer</span></span>  <br/> |<span data-ttu-id="143ba-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="143ba-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="143ba-111">1</span><span class="sxs-lookup"><span data-stu-id="143ba-111">1</span></span>  <br/> | <span data-ttu-id="143ba-112">Книжная</span><span class="sxs-lookup"><span data-stu-id="143ba-112">Portrait</span></span>  <br/> |<span data-ttu-id="143ba-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="143ba-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="143ba-114">2</span><span class="sxs-lookup"><span data-stu-id="143ba-114">2</span></span>  <br/> |<span data-ttu-id="143ba-115">Альбомная</span><span class="sxs-lookup"><span data-stu-id="143ba-115">Landscape</span></span>  <br/> |<span data-ttu-id="143ba-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="143ba-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="143ba-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="143ba-117">Remarks</span></span>

<span data-ttu-id="143ba-118">При добавлении новых страниц в документе, этот параметр по умолчанию параметр на активной странице.</span><span class="sxs-lookup"><span data-stu-id="143ba-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="143ba-119">Чтобы получить ссылку на ячейку PrintPageOrientation по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="143ba-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="143ba-120">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="143ba-120">Cell name:</span></span>  <br/> | <span data-ttu-id="143ba-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="143ba-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="143ba-122">Для получения ссылки на ячейки PrintPageOrientation по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="143ba-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="143ba-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="143ba-123">Section index:</span></span>  <br/> |<span data-ttu-id="143ba-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="143ba-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="143ba-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="143ba-125">Row index:</span></span>  <br/> |<span data-ttu-id="143ba-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="143ba-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="143ba-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="143ba-127">Cell index:</span></span>  <br/> |<span data-ttu-id="143ba-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="143ba-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

