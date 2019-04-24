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
description: Определяет, будет ли страница печататься по книжной или альбомной ориентации.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315185"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="5c3c5-103">PrintPageOrientation Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5c3c5-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="5c3c5-104">Определяет, будет ли страница печататься по книжной или альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="5c3c5-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="5c3c5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-105">**Value**</span></span>|<span data-ttu-id="5c3c5-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-106">**Orientation**</span></span>|<span data-ttu-id="5c3c5-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5c3c5-108">нуль</span><span class="sxs-lookup"><span data-stu-id="5c3c5-108">0</span></span>  <br/> | <span data-ttu-id="5c3c5-109">То же, что принтер</span><span class="sxs-lookup"><span data-stu-id="5c3c5-109">Same as printer</span></span>  <br/> |<span data-ttu-id="5c3c5-110">**Висппосамеаспринтер**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="5c3c5-111">1,1</span><span class="sxs-lookup"><span data-stu-id="5c3c5-111">1</span></span>  <br/> | <span data-ttu-id="5c3c5-112">Ориентацию</span><span class="sxs-lookup"><span data-stu-id="5c3c5-112">Portrait</span></span>  <br/> |<span data-ttu-id="5c3c5-113">**Висппопортраит**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="5c3c5-114">2</span><span class="sxs-lookup"><span data-stu-id="5c3c5-114">2</span></span>  <br/> |<span data-ttu-id="5c3c5-115">Вдоль</span><span class="sxs-lookup"><span data-stu-id="5c3c5-115">Landscape</span></span>  <br/> |<span data-ttu-id="5c3c5-116">**Виспполандскапе**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c3c5-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c3c5-117">Remarks</span></span>

<span data-ttu-id="5c3c5-118">При вставке в документ новых страниц этот параметр по умолчанию устанавливается на активной странице.</span><span class="sxs-lookup"><span data-stu-id="5c3c5-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="5c3c5-119">Чтобы получить ссылку на ячейку PrintPageOrientation по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c3c5-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-120">Cell name:</span></span>  <br/> | <span data-ttu-id="5c3c5-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="5c3c5-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="5c3c5-122">Чтобы получить ссылку на ячейку PrintPageOrientation по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c3c5-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-123">Section index:</span></span>  <br/> |<span data-ttu-id="5c3c5-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5c3c5-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-125">Row index:</span></span>  <br/> |<span data-ttu-id="5c3c5-126">**Висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="5c3c5-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5c3c5-127">Cell index:</span></span>  <br/> |<span data-ttu-id="5c3c5-128">**Виспринтпропертиеспажеориентатион**</span><span class="sxs-lookup"><span data-stu-id="5c3c5-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

