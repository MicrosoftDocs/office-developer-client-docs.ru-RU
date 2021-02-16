---
title: PageShapeSplit Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Указывает, можно ли автоматически разделить фигуры на странице.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422021"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="e3404-103">PageShapeSplit Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e3404-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="e3404-104">Указывает, можно ли автоматически разделить фигуры на странице.</span><span class="sxs-lookup"><span data-stu-id="e3404-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="e3404-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e3404-105">**Value**</span></span>|<span data-ttu-id="e3404-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3404-106">**Description**</span></span>|<span data-ttu-id="e3404-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e3404-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3404-108">0</span><span class="sxs-lookup"><span data-stu-id="e3404-108">0</span></span>  <br/> |<span data-ttu-id="e3404-109">Не разрешите автоматическое разделение фигур.</span><span class="sxs-lookup"><span data-stu-id="e3404-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="e3404-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="e3404-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="e3404-111">1 </span><span class="sxs-lookup"><span data-stu-id="e3404-111">1</span></span>  <br/> |<span data-ttu-id="e3404-112">Разрешить автоматическое разделение фигур (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="e3404-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="e3404-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="e3404-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3404-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3404-114">Remarks</span></span>

<span data-ttu-id="e3404-115">Автоматическое разделение фигур включено и отключено на трех разных уровнях: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="e3404-115">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="e3404-116">По умолчанию разделение включено на уровнях приложения и страницы.</span><span class="sxs-lookup"><span data-stu-id="e3404-116">By default, splitting is enabled at the application and page levels.</span></span> <span data-ttu-id="e3404-117">Значение по умолчанию для фигур зависит от типа рисования.</span><span class="sxs-lookup"><span data-stu-id="e3404-117">The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="e3404-118">Чтобы включить или отключить разделение на уровне  приложения, используйте параметр разделения  соединители "Включить" на вкладке "Дополнительные параметры" в диалоговом окне "Параметры **Visio"** (нажмите кнопку **Office,** выберите "Параметры" на вкладке **Visio** и нажмите кнопку  "Дополнительные"). </span><span class="sxs-lookup"><span data-stu-id="e3404-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="e3404-119">Чтобы включить или отключить разделение на уровне фигуры, см. разделы ShapeSplit и ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="e3404-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="e3404-120">Чтобы получить ссылку на ячейку PageShapeSplit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e3404-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3404-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3404-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e3404-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="e3404-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="e3404-123">Чтобы получить ссылку на ячейку PageShapeSplit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e3404-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3404-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3404-124">Section index:</span></span>  <br/> |<span data-ttu-id="e3404-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3404-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e3404-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3404-126">Row index:</span></span>  <br/> |<span data-ttu-id="e3404-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e3404-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="e3404-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3404-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e3404-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="e3404-129">**visPLOSplit**</span></span> <br/> |
   

