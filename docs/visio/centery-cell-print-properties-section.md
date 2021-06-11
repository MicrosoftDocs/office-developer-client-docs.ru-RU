---
title: CenterY Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Определяет, по центру ли страница рисования вертикально на странице принтера.
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437436"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="f145c-103">CenterY Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="f145c-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="f145c-104">Определяет, по центру ли страница рисования вертикально на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="f145c-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="f145c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f145c-105">**Value**</span></span>|<span data-ttu-id="f145c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f145c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f145c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f145c-107">TRUE</span></span>  <br/> | <span data-ttu-id="f145c-108">Центр страницы рисования вертикально на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="f145c-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="f145c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f145c-109">FALSE</span></span>  <br/> | <span data-ttu-id="f145c-110">Не центрить страницу рисования вертикально на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f145c-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f145c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f145c-111">Remarks</span></span>

<span data-ttu-id="f145c-112">По умолчанию страницы рисования оправданы в верхней и левой части страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="f145c-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="f145c-113">Настройка ячеек CenterX и CenterY в TRUE помещает страницу рисования в центре страницы принтера (или страниц, когда это необходимо).</span><span class="sxs-lookup"><span data-stu-id="f145c-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="f145c-114">Чтобы получить ссылку на ячейку CenterY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f145c-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f145c-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f145c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="f145c-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="f145c-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="f145c-117">Чтобы получить ссылку на ячейку CenterY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f145c-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f145c-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f145c-118">Section index:</span></span>  <br/> |<span data-ttu-id="f145c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f145c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f145c-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f145c-120">Row index:</span></span>  <br/> |<span data-ttu-id="f145c-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f145c-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f145c-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f145c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f145c-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="f145c-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

