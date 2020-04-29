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
description: Указывает процентное отношение для увеличения или уменьшения тени фигуры.
ms.openlocfilehash: 9175e9a1148779524fdce96ff18eac22fe8dd421
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429007"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="9efe9-103">ShdwScaleFactor Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9efe9-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="9efe9-104">Указывает процентное отношение для увеличения или уменьшения тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="9efe9-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9efe9-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="9efe9-105">Remarks</span></span>

<span data-ttu-id="9efe9-106">Каждая теневая копия имеет затененный ПИН-код, указывающий на тень, соответствующую ПИН-коду фигуры.</span><span class="sxs-lookup"><span data-stu-id="9efe9-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="9efe9-107">Например, если ПИН-код фигуры находится в центре фигуры, то затененное расположение ПИН-кода будет точкой в центре тени.</span><span class="sxs-lookup"><span data-stu-id="9efe9-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="9efe9-108">При применении масштаба к простым теням, увеличение выравнивается по центру в затененном расположении; При применении масштаба к теням теней наклон применяется при увеличении наклона.</span><span class="sxs-lookup"><span data-stu-id="9efe9-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="9efe9-109">Этот процент используется, если для типа Shadow для фигуры задано значение по умолчанию (ячейка ShapeShdwType равно \* \* Висфстпажедефаулт \* \*).</span><span class="sxs-lookup"><span data-stu-id="9efe9-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals \*\* visFSTPageDefault \*\* ).</span></span> 
  
<span data-ttu-id="9efe9-110">Чтобы задать такое поведение для отдельной фигуры, используйте ячейку ShapeShdwScaleFactor в разделе Формат заливки.</span><span class="sxs-lookup"><span data-stu-id="9efe9-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="9efe9-111">Это значение соответствует значению в поле " **масштаб** " на вкладке " **тени** " диалогового окна " **Параметры страницы** " (на вкладке " **конструктор** " щелкните стрелку **настройки страницы** ).</span><span class="sxs-lookup"><span data-stu-id="9efe9-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="9efe9-112">Чтобы получить ссылку на ячейку ShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="9efe9-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9efe9-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9efe9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9efe9-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="9efe9-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="9efe9-115">Чтобы получить ссылку на ячейку ShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9efe9-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9efe9-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9efe9-116">Section index:</span></span>  <br/> |<span data-ttu-id="9efe9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9efe9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9efe9-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9efe9-118">Row index:</span></span>  <br/> |<span data-ttu-id="9efe9-119">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="9efe9-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="9efe9-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9efe9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9efe9-121">**виспажешдвскалефактор**</span><span class="sxs-lookup"><span data-stu-id="9efe9-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

