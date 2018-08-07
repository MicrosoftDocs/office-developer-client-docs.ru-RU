---
title: Ячейка CenterX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Определяет, будет ли страницы рисунка центру по по горизонтали на странице принтера.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813378"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="d2e19-103">Ячейка CenterX (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="d2e19-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="d2e19-104">Определяет, будет ли страницы рисунка центру по по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="d2e19-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="d2e19-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d2e19-105">**Value**</span></span>|<span data-ttu-id="d2e19-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d2e19-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d2e19-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d2e19-107">TRUE</span></span>  <br/> | <span data-ttu-id="d2e19-108">Центр страницы рисунка по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="d2e19-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="d2e19-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d2e19-109">FALSE</span></span>  <br/> | <span data-ttu-id="d2e19-110">Не центрирования страницы рисунка по горизонтали на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d2e19-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e19-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2e19-111">Remarks</span></span>

<span data-ttu-id="d2e19-112">По умолчанию страниц документа краю верхней и левой части страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="d2e19-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="d2e19-113">Установка ячейки CenterX и CenterY TRUE местах на странице документа в центре страницы принтера (или страниц при необходимости заполнения).</span><span class="sxs-lookup"><span data-stu-id="d2e19-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="d2e19-114">Чтобы получить ссылку на ячейку CenterX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d2e19-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2e19-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d2e19-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d2e19-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="d2e19-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="d2e19-117">Для получения ссылки на ячейки CenterX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d2e19-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2e19-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d2e19-118">Section index:</span></span>  <br/> |<span data-ttu-id="d2e19-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2e19-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2e19-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d2e19-120">Row index:</span></span>  <br/> |<span data-ttu-id="d2e19-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d2e19-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d2e19-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d2e19-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d2e19-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="d2e19-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

