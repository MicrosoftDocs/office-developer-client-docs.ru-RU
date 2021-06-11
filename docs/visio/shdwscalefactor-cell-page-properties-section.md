---
title: ShdwScaleFactor Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Указывает процент для увеличения или уменьшения тени фигуры.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429007"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="28d2f-103">ShdwScaleFactor Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="28d2f-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="28d2f-104">Указывает процент для увеличения или уменьшения тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="28d2f-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28d2f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="28d2f-105">Remarks</span></span>

<span data-ttu-id="28d2f-106">Каждая тень имеет затеняемое расположение пина, которое является точкой на тени, соответствующей пин-коду фигуры.</span><span class="sxs-lookup"><span data-stu-id="28d2f-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="28d2f-107">Например, если пин-код фигуры находится в центре фигуры, то затеняемое расположение пина будет точкой в центре тени.</span><span class="sxs-lookup"><span data-stu-id="28d2f-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="28d2f-108">При применении масштабирования к простым теням увеличение расположено в затененом расположении пин-кода; При применении масштабирования к косой тени в косом направлении применяется увеличение.</span><span class="sxs-lookup"><span data-stu-id="28d2f-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="28d2f-109">Этот процент используется, когда для типа теней для фигуры установлено значение Page Default (ячейка ShapeShdwType равна \*\* visFSTPageDefault \*\* ).</span><span class="sxs-lookup"><span data-stu-id="28d2f-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals \*\* visFSTPageDefault \*\* ).</span></span> 
  
<span data-ttu-id="28d2f-110">Чтобы настроить это поведение для отдельной фигуры, используйте ячейку ShapeShdwScaleFactor в разделе Формат заполнения.</span><span class="sxs-lookup"><span data-stu-id="28d2f-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="28d2f-111">Это значение соответствует значению в поле **Увеличение** на вкладке  **Shadows** в диалоговом окне Настройка страницы (на вкладке **Дизайн** щелкните стрелку **установки** страницы).</span><span class="sxs-lookup"><span data-stu-id="28d2f-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="28d2f-112">Чтобы получить ссылку на ячейку ShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="28d2f-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28d2f-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="28d2f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="28d2f-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="28d2f-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="28d2f-115">Чтобы получить ссылку на ячейку ShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="28d2f-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="28d2f-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="28d2f-116">Section index:</span></span>  <br/> |<span data-ttu-id="28d2f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="28d2f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="28d2f-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="28d2f-118">Row index:</span></span>  <br/> |<span data-ttu-id="28d2f-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="28d2f-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="28d2f-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="28d2f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="28d2f-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="28d2f-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

