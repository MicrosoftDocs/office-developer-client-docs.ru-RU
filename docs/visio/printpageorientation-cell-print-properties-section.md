---
title: PrintPageOrientation Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Определяет, печатается ли страница с помощью кантной или альбомной ориентации.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434867"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="24242-103">PrintPageOrientation Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="24242-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="24242-104">Определяет, печатается ли страница с помощью кантной или альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="24242-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="24242-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="24242-105">**Value**</span></span>|<span data-ttu-id="24242-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="24242-106">**Orientation**</span></span>|<span data-ttu-id="24242-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="24242-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="24242-108">0</span><span class="sxs-lookup"><span data-stu-id="24242-108">0</span></span>  <br/> | <span data-ttu-id="24242-109">То же, что и принтер</span><span class="sxs-lookup"><span data-stu-id="24242-109">Same as printer</span></span>  <br/> |<span data-ttu-id="24242-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="24242-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="24242-111">1 </span><span class="sxs-lookup"><span data-stu-id="24242-111">1</span></span>  <br/> | <span data-ttu-id="24242-112">Кивная</span><span class="sxs-lookup"><span data-stu-id="24242-112">Portrait</span></span>  <br/> |<span data-ttu-id="24242-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="24242-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="24242-114">2 </span><span class="sxs-lookup"><span data-stu-id="24242-114">2</span></span>  <br/> |<span data-ttu-id="24242-115">Альбомная</span><span class="sxs-lookup"><span data-stu-id="24242-115">Landscape</span></span>  <br/> |<span data-ttu-id="24242-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="24242-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24242-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="24242-117">Remarks</span></span>

<span data-ttu-id="24242-118">При вставке новых страниц в документ этот параметр по умолчанию заводится на активной странице.</span><span class="sxs-lookup"><span data-stu-id="24242-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="24242-119">Чтобы получить ссылку на ячейку PrintPageOrientation по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="24242-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24242-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="24242-120">Cell name:</span></span>  <br/> | <span data-ttu-id="24242-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="24242-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="24242-122">Чтобы получить ссылку на ячейку PrintPageOrientation по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="24242-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24242-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="24242-123">Section index:</span></span>  <br/> |<span data-ttu-id="24242-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24242-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="24242-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="24242-125">Row index:</span></span>  <br/> |<span data-ttu-id="24242-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="24242-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="24242-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="24242-127">Cell index:</span></span>  <br/> |<span data-ttu-id="24242-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="24242-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

