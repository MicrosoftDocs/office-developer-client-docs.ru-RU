---
title: ShapeSplit Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Указывает, может ли эта фигура разделять фигуры, которые можно разделить.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423561"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="eb3da-103">ShapeSplit Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="eb3da-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="eb3da-104">Указывает, может ли эта фигура разделять фигуры, которые можно разделить.</span><span class="sxs-lookup"><span data-stu-id="eb3da-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="eb3da-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="eb3da-105">**Value**</span></span>|<span data-ttu-id="eb3da-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb3da-106">**Description**</span></span>|<span data-ttu-id="eb3da-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="eb3da-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="eb3da-108">0</span><span class="sxs-lookup"><span data-stu-id="eb3da-108">0</span></span>  <br/> | <span data-ttu-id="eb3da-109">Не разрешите этой фигуре разделять другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb3da-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="eb3da-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="eb3da-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="eb3da-111">1 </span><span class="sxs-lookup"><span data-stu-id="eb3da-111">1</span></span>  <br/> | <span data-ttu-id="eb3da-112">Разрешите этой фигуре разделять другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb3da-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="eb3da-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="eb3da-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb3da-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb3da-114">Remarks</span></span>

<span data-ttu-id="eb3da-115">Фигура, которая может разделить другие фигуры, должна быть двух- или 1-D-фигурой.</span><span class="sxs-lookup"><span data-stu-id="eb3da-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="eb3da-116">Автоматическое разделение фигур включено и отключено на трех разных уровнях: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb3da-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="eb3da-117">По умолчанию разделение включено на уровне приложения и страницы; для фигур он зависит от типа рисования.</span><span class="sxs-lookup"><span data-stu-id="eb3da-117">By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="eb3da-118">Чтобы включить или отключить разделение на уровне  приложения, используйте параметр разделения соединители Enable на вкладке "Дополнительные  параметры" диалогового окна "Параметры **Visio"** (щелкните вкладку "Файл", щелкните "Параметры" и выберите  "Дополнительные"). </span><span class="sxs-lookup"><span data-stu-id="eb3da-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="eb3da-119">Чтобы включить или отключить разделение на странице, см. ячейку PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="eb3da-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="eb3da-120">Чтобы 1-D фигура была разделена, см. ячейку ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="eb3da-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="eb3da-121">Чтобы получить ссылку на ячейку ShapeSplit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="eb3da-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb3da-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb3da-122">Cell name:</span></span>  <br/> | <span data-ttu-id="eb3da-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="eb3da-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="eb3da-124">Чтобы получить ссылку на ячейку ShapeSplit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eb3da-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb3da-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eb3da-125">Section index:</span></span>  <br/> |<span data-ttu-id="eb3da-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb3da-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb3da-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eb3da-127">Row index:</span></span>  <br/> |<span data-ttu-id="eb3da-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="eb3da-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="eb3da-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb3da-129">Cell index:</span></span>  <br/> |<span data-ttu-id="eb3da-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="eb3da-130">**visSLOSplit**</span></span> <br/> |
   

