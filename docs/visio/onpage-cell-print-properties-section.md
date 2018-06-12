---
title: Ячейка OnPage (печати Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Указывает, печатается ли документ на определенное число страниц принтера.
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814313"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="68dc7-103">Ячейка OnPage (печати Properties Section)</span><span class="sxs-lookup"><span data-stu-id="68dc7-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="68dc7-104">Указывает, печатается ли документ на определенное число страниц принтера.</span><span class="sxs-lookup"><span data-stu-id="68dc7-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="68dc7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="68dc7-105">**Value**</span></span>|<span data-ttu-id="68dc7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68dc7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68dc7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="68dc7-107">TRUE</span></span>  <br/> |<span data-ttu-id="68dc7-108">Размещения страницы документа на определенное число печатных страниц.</span><span class="sxs-lookup"><span data-stu-id="68dc7-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="68dc7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="68dc7-109">FALSE</span></span>  <br/> |<span data-ttu-id="68dc7-110">Не соответствуют страницу документа для определенных количество печатных страниц (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="68dc7-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68dc7-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="68dc7-111">Remarks</span></span>

<span data-ttu-id="68dc7-112">Если ячейка OnPage задано значение TRUE, Microsoft Visio использует ячейки PagesX и PagesY для определения количество печатных страниц для размещения документа.</span><span class="sxs-lookup"><span data-stu-id="68dc7-112">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing.</span></span> <span data-ttu-id="68dc7-113">Значения в ячейках ScaleX и ScaleY игнорируются.</span><span class="sxs-lookup"><span data-stu-id="68dc7-113">Values in the ScaleX and ScaleY cells are ignored.</span></span> <span data-ttu-id="68dc7-114">Это можно оценить как параметр «autoscale».</span><span class="sxs-lookup"><span data-stu-id="68dc7-114">This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="68dc7-115">Это значение соответствует параметру **по размеру** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="68dc7-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="68dc7-116">Для получения ссылки на ячейки OnPage по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="68dc7-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68dc7-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="68dc7-117">Cell name:</span></span>  <br/> |<span data-ttu-id="68dc7-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="68dc7-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="68dc7-119">Для получения ссылки на ячейки OnPage по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="68dc7-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68dc7-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="68dc7-120">Section index:</span></span>  <br/> |<span data-ttu-id="68dc7-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68dc7-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="68dc7-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="68dc7-122">Row index:</span></span>  <br/> |<span data-ttu-id="68dc7-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="68dc7-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="68dc7-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="68dc7-124">Cell index:</span></span>  <br/> |<span data-ttu-id="68dc7-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="68dc7-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

