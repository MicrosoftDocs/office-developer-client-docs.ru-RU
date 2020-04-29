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
description: Определяет, будет ли страница документа выравниваться по горизонтали на странице принтера.
ms.openlocfilehash: 13b05ed71248a3f8fada947fca6b203c6ab19c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418080"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="3a7f6-103">CenterX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="3a7f6-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="3a7f6-104">Определяет, будет ли страница документа выравниваться по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="3a7f6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-105">**Value**</span></span>|<span data-ttu-id="3a7f6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3a7f6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3a7f6-107">TRUE</span></span>  <br/> | <span data-ttu-id="3a7f6-108">Разцентрирование страницы документа по горизонтали на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="3a7f6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3a7f6-109">FALSE</span></span>  <br/> | <span data-ttu-id="3a7f6-110">Не выравнивать страницу документа по горизонтали на странице принтера (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="3a7f6-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a7f6-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a7f6-111">Remarks</span></span>

<span data-ttu-id="3a7f6-112">По умолчанию страницы документа выравниваются по верхнему и левому краю страницы принтера.</span><span class="sxs-lookup"><span data-stu-id="3a7f6-112">By default, drawing pages are justified to the top and left of the printer page.</span></span> <span data-ttu-id="3a7f6-113">Установка для CenterX и центрированных ячеек значения TRUE поместит страницу документа в центре страницы принтера (или на страницах при необходимости заполнения).</span><span class="sxs-lookup"><span data-stu-id="3a7f6-113">Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="3a7f6-114">Чтобы получить ссылку на ячейку CenterX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a7f6-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3a7f6-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="3a7f6-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="3a7f6-117">Чтобы получить ссылку на ячейку CenterX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3a7f6-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-118">Section index:</span></span>  <br/> |<span data-ttu-id="3a7f6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3a7f6-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-120">Row index:</span></span>  <br/> |<span data-ttu-id="3a7f6-121">**висровпринтпропертиес**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="3a7f6-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3a7f6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3a7f6-123">**виспринтпропертиесцентеркс**</span><span class="sxs-lookup"><span data-stu-id="3a7f6-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

