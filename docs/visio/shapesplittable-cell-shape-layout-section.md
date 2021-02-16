---
title: ShapeSplittable Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Указывает, можно ли разделить эту 1-D-фигуру.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427075"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="1e857-103">ShapeSplittable Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="1e857-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="1e857-104">Указывает, можно ли разделить эту 1-D-фигуру.</span><span class="sxs-lookup"><span data-stu-id="1e857-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="1e857-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1e857-105">**Value**</span></span>|<span data-ttu-id="1e857-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1e857-106">**Description**</span></span>|<span data-ttu-id="1e857-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="1e857-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1e857-108">0</span><span class="sxs-lookup"><span data-stu-id="1e857-108">0</span></span>  <br/> | <span data-ttu-id="1e857-109">Не разрешите разделять эту фигуру.</span><span class="sxs-lookup"><span data-stu-id="1e857-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="1e857-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="1e857-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="1e857-111">1 </span><span class="sxs-lookup"><span data-stu-id="1e857-111">1</span></span>  <br/> | <span data-ttu-id="1e857-112">Разрешить разделение фигуры.</span><span class="sxs-lookup"><span data-stu-id="1e857-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="1e857-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="1e857-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e857-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e857-114">Remarks</span></span>

<span data-ttu-id="1e857-115">Поведение по умолчанию для соединители и других 1-D фигур зависит от типа рисования.</span><span class="sxs-lookup"><span data-stu-id="1e857-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="1e857-116">Автоматическое разделение фигур включено и отключено на трех разных уровнях: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="1e857-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="1e857-117">По умолчанию разделение включено на уровне приложения и страницы.</span><span class="sxs-lookup"><span data-stu-id="1e857-117">By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="1e857-118">Чтобы включить или отключить разделение на уровне приложения, используйте параметр разделения  соединители enable на вкладке "Дополнительные  параметры" диалогового окна "Параметры **Visio"** (щелкните вкладку "Файл", выберите "Параметры" и нажмите кнопку  "Дополнительные"). </span><span class="sxs-lookup"><span data-stu-id="1e857-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="1e857-119">Чтобы включить или отключить разделение на странице, см. [ячейку PageShapeSplit.](pageshapesplit-cell-page-layout-section.md)</span><span class="sxs-lookup"><span data-stu-id="1e857-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="1e857-120">Чтобы фигура смогла разделить разделенные фигуры, см. в [ячейке ShapeSplit.](shapesplit-cell-shape-layout-section.md)</span><span class="sxs-lookup"><span data-stu-id="1e857-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="1e857-121">Чтобы получить ссылку на ячейку ShapeSplittable по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="1e857-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e857-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="1e857-122">Cell name:</span></span>  <br/> | <span data-ttu-id="1e857-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="1e857-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="1e857-124">Чтобы получить ссылку на ячейку ShapeSplittable по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="1e857-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e857-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1e857-125">Section index:</span></span>  <br/> |<span data-ttu-id="1e857-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1e857-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1e857-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1e857-127">Row index:</span></span>  <br/> |<span data-ttu-id="1e857-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="1e857-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="1e857-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1e857-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1e857-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="1e857-130">**visSLOSplittable**</span></span> <br/> |
   

