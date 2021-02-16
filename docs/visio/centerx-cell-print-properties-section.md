---
title: CenterX Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Определяет, находится ли страница рисования по горизонтали на странице принтера.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418080"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="00d59-103">CenterX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="00d59-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="00d59-104">Определяет, находится ли страница рисования по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="00d59-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="00d59-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="00d59-105">**Value**</span></span>|<span data-ttu-id="00d59-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00d59-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="00d59-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="00d59-107">TRUE</span></span>  <br/> | <span data-ttu-id="00d59-108">Центр страницы рисования по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="00d59-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="00d59-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="00d59-109">FALSE</span></span>  <br/> | <span data-ttu-id="00d59-110">Не нарисуя страницу рисования по горизонтали на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="00d59-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00d59-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="00d59-111">Remarks</span></span>

<span data-ttu-id="00d59-112">По умолчанию страницы рисования имеют верхней и левой стороны страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="00d59-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="00d59-113">При установке для ячеек CenterX и CenterY в true страница рисования помещается в центр страницы принтера (или страницы, когда требуется установка плитки).</span><span class="sxs-lookup"><span data-stu-id="00d59-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="00d59-114">Чтобы получить ссылку на ячейку CenterX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="00d59-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00d59-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="00d59-115">Cell name:</span></span>  <br/> | <span data-ttu-id="00d59-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="00d59-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="00d59-117">Чтобы получить ссылку на ячейку CenterX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="00d59-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00d59-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="00d59-118">Section index:</span></span>  <br/> |<span data-ttu-id="00d59-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00d59-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="00d59-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="00d59-120">Row index:</span></span>  <br/> |<span data-ttu-id="00d59-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="00d59-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="00d59-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="00d59-122">Cell index:</span></span>  <br/> |<span data-ttu-id="00d59-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="00d59-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

