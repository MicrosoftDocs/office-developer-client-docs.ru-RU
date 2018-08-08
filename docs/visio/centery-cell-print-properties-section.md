---
title: Ячейка CenterY (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Определяет, будет ли страницы рисунка центру по по вертикали на странице принтера.
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813397"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="e619b-103">Ячейка CenterY (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="e619b-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="e619b-104">Определяет, будет ли страницы рисунка центру по по вертикали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="e619b-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="e619b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e619b-105">**Value**</span></span>|<span data-ttu-id="e619b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e619b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e619b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e619b-107">TRUE</span></span>  <br/> | <span data-ttu-id="e619b-108">Центр страницы рисунка по вертикали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="e619b-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="e619b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e619b-109">FALSE</span></span>  <br/> | <span data-ttu-id="e619b-110">Не центрирования страницы рисунка по вертикали на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e619b-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e619b-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="e619b-111">Remarks</span></span>

<span data-ttu-id="e619b-112">По умолчанию страниц документа краю верхней и левой части страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="e619b-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="e619b-113">Установка ячейки CenterX и CenterY TRUE местах на странице документа в центре страницы принтера (или страниц при необходимости заполнения).</span><span class="sxs-lookup"><span data-stu-id="e619b-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="e619b-114">Для получения ссылки на ячейки координат центра по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e619b-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e619b-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e619b-115">Cell name:</span></span>  <br/> | <span data-ttu-id="e619b-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="e619b-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="e619b-117">Для получения ссылки на ячейки координат центра по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e619b-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e619b-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e619b-118">Section index:</span></span>  <br/> |<span data-ttu-id="e619b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e619b-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e619b-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e619b-120">Row index:</span></span>  <br/> |<span data-ttu-id="e619b-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e619b-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="e619b-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e619b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e619b-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="e619b-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

