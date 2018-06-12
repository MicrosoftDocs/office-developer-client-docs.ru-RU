---
title: Ширина ячеек (раздел Преобразование фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Содержит ширину выбранной фигуры в единицах документа. Формула для определения ширины одномерной фигуры — это:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815163"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="9dfc2-104">Ширина ячеек (раздел Преобразование фигуры)</span><span class="sxs-lookup"><span data-stu-id="9dfc2-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="9dfc2-105">Содержит ширину выбранной фигуры в единицах документа.</span><span class="sxs-lookup"><span data-stu-id="9dfc2-105">Contains the width of the selected shape in drawing units.</span></span> <span data-ttu-id="9dfc2-106">Формула для определения ширины одномерной фигуры — это:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-106">The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="9dfc2-107">= КОРЕНЬ ((EndX-BeginX) ^ 2 + (КонецY - НачалоY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="9dfc2-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9dfc2-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9dfc2-108">Remarks</span></span>

<span data-ttu-id="9dfc2-109">Для получения ссылки на ячейки ширины по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9dfc2-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9dfc2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="9dfc2-111">Width</span><span class="sxs-lookup"><span data-stu-id="9dfc2-111">Width</span></span>  <br/> |
   
<span data-ttu-id="9dfc2-112">Для получения ссылки на ячейки ширины по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9dfc2-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-113">Section index:</span></span>  <br/> |<span data-ttu-id="9dfc2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9dfc2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9dfc2-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-115">Row index:</span></span>  <br/> |<span data-ttu-id="9dfc2-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="9dfc2-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="9dfc2-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9dfc2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9dfc2-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="9dfc2-118">**visXFormWidth**</span></span> <br/> |
   

