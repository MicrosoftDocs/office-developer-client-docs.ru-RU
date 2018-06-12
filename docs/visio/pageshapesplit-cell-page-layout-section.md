---
title: Ячейка PageShapeSplit (раздел макет страницы)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Указывает, может ли автоматически разделение фигур на странице.
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814353"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="c53bc-103">Ячейка PageShapeSplit (раздел макет страницы)</span><span class="sxs-lookup"><span data-stu-id="c53bc-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="c53bc-104">Указывает, может ли автоматически разделение фигур на странице.</span><span class="sxs-lookup"><span data-stu-id="c53bc-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="c53bc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c53bc-105">**Value**</span></span>|<span data-ttu-id="c53bc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c53bc-106">**Description**</span></span>|<span data-ttu-id="c53bc-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="c53bc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c53bc-108">0</span><span class="sxs-lookup"><span data-stu-id="c53bc-108">0</span></span>  <br/> |<span data-ttu-id="c53bc-109">Не разрешать разделение автоматического фигуры.</span><span class="sxs-lookup"><span data-stu-id="c53bc-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="c53bc-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="c53bc-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="c53bc-111">1</span><span class="sxs-lookup"><span data-stu-id="c53bc-111">1</span></span>  <br/> |<span data-ttu-id="c53bc-112">Разрешить автоматическое фигуры разделение (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c53bc-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="c53bc-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="c53bc-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c53bc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c53bc-114">Remarks</span></span>

<span data-ttu-id="c53bc-115">Автоматическое разделение фигур включена и отключена три уровня: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="c53bc-115">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="c53bc-116">По умолчанию разделение включена на уровне приложения и страницы.</span><span class="sxs-lookup"><span data-stu-id="c53bc-116">By default, splitting is enabled at the application and page levels.</span></span> <span data-ttu-id="c53bc-117">Значение по умолчанию для фигур зависит от типа документа.</span><span class="sxs-lookup"><span data-stu-id="c53bc-117">The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="c53bc-118">Чтобы включить или отключить разделение на уровне приложения, используйте параметр **включить разделение соединительной линии** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (нажмите кнопку **Office** , выберите команду **Параметры** в **Visio** а затем щелкните **Дополнительно** ).</span><span class="sxs-lookup"><span data-stu-id="c53bc-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="c53bc-119">Чтобы включить или отключить разделение на уровне фигур, обратитесь к разделу ячейки ShapeSplit и ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="c53bc-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="c53bc-120">Чтобы получить ссылку на ячейку PageShapeSplit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c53bc-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c53bc-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c53bc-121">Cell name:</span></span>  <br/> |<span data-ttu-id="c53bc-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="c53bc-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="c53bc-123">Для получения ссылки на ячейки PageShapeSplit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c53bc-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c53bc-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c53bc-124">Section index:</span></span>  <br/> |<span data-ttu-id="c53bc-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c53bc-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c53bc-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c53bc-126">Row index:</span></span>  <br/> |<span data-ttu-id="c53bc-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c53bc-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="c53bc-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c53bc-128">Cell index:</span></span>  <br/> |<span data-ttu-id="c53bc-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="c53bc-129">**visPLOSplit**</span></span> <br/> |
   

