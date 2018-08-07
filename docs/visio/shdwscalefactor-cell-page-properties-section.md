---
title: Ячейка ShdwScaleFactor (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Указывает процент для увеличения или уменьшения тени фигуры.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814835"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="beadd-103">Ячейка ShdwScaleFactor (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="beadd-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="beadd-104">Указывает процент для увеличения или уменьшения тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="beadd-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="beadd-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="beadd-105">Remarks</span></span>

<span data-ttu-id="beadd-106">Каждый теневой имеет расположении тенью ПИН-кода, то есть точку на тени, соответствующий фигуры ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="beadd-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="beadd-107">К примеру Если фигуры ПИН-код находится в центр фигуры, расположение тенью ПИН-код будет точка в центре тени.</span><span class="sxs-lookup"><span data-stu-id="beadd-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="beadd-108">При применении масштаба для простого тени, масштаб по центру расположении тенью ПИН-кода; При применении масштаба наклон тени, увеличения применяются наклона.</span><span class="sxs-lookup"><span data-stu-id="beadd-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="beadd-109">Этот процент используется, когда тип тени для фигуры задано значение по умолчанию для страницы (ShapeShdwType ячейки равно ** visFSTPageDefault **).</span><span class="sxs-lookup"><span data-stu-id="beadd-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals ** visFSTPageDefault ** ).</span></span> 
  
<span data-ttu-id="beadd-110">Чтобы задать это поведение для отдельных фигуры, используйте ShapeShdwScaleFactor ячейки в разделе формат заполните поля.</span><span class="sxs-lookup"><span data-stu-id="beadd-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="beadd-111">Это значение соответствует значению в поле **Масштаб** на вкладке **теней** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="beadd-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="beadd-112">Чтобы получить ссылку на ячейку ShdwScaleFactor по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="beadd-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="beadd-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="beadd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="beadd-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="beadd-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="beadd-115">Для получения ссылки на ячейки ShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="beadd-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="beadd-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="beadd-116">Section index:</span></span>  <br/> |<span data-ttu-id="beadd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="beadd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="beadd-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="beadd-118">Row index:</span></span>  <br/> |<span data-ttu-id="beadd-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="beadd-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="beadd-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="beadd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="beadd-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="beadd-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

