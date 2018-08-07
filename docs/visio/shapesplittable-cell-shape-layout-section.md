---
title: Ячейка ShapeSplittable (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Указывает, будет ли этот одномерной фигуры можно разделить.
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814812"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="5f752-103">Ячейка ShapeSplittable (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="5f752-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5f752-104">Указывает, будет ли этот одномерной фигуры можно разделить.</span><span class="sxs-lookup"><span data-stu-id="5f752-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="5f752-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5f752-105">**Value**</span></span>|<span data-ttu-id="5f752-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5f752-106">**Description**</span></span>|<span data-ttu-id="5f752-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="5f752-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5f752-108">0</span><span class="sxs-lookup"><span data-stu-id="5f752-108">0</span></span>  <br/> | <span data-ttu-id="5f752-109">Не разрешать этой фигуры для разделения.</span><span class="sxs-lookup"><span data-stu-id="5f752-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5f752-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="5f752-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="5f752-111">1</span><span class="sxs-lookup"><span data-stu-id="5f752-111">1</span></span>  <br/> | <span data-ttu-id="5f752-112">Разрешить этой фигуры для разделения.</span><span class="sxs-lookup"><span data-stu-id="5f752-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5f752-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="5f752-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f752-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f752-114">Remarks</span></span>

<span data-ttu-id="5f752-115">Поведение по умолчанию для соединителей и другие фигуры 1 D изменяется в соответствии с тип графического.</span><span class="sxs-lookup"><span data-stu-id="5f752-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="5f752-116">Автоматическое разделение фигур включена и отключена три уровня: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="5f752-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="5f752-117">По умолчанию разделение включена на уровне приложения и уровни страниц.</span><span class="sxs-lookup"><span data-stu-id="5f752-117">By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="5f752-118">Чтобы включить или отключить разделение на уровне приложения, используйте параметр **включить разделение соединительной линии** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , выберите пункт **Параметры**и нажмите кнопку ** Расширенный** ).</span><span class="sxs-lookup"><span data-stu-id="5f752-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="5f752-119">Чтобы включить или отключить разбиение на страницы, обратитесь к разделу [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) ячейки.</span><span class="sxs-lookup"><span data-stu-id="5f752-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5f752-120">Чтобы фигуры должны иметь возможность разделение 1 D возможность разделения фигур, видеть [ShapeSplit](shapesplit-cell-shape-layout-section.md) ячейки.</span><span class="sxs-lookup"><span data-stu-id="5f752-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5f752-121">Чтобы получить ссылку на ячейку ShapeSplittable по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="5f752-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f752-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5f752-122">Cell name:</span></span>  <br/> | <span data-ttu-id="5f752-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="5f752-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="5f752-124">Для получения ссылки на ячейки ShapeSplittable по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5f752-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5f752-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5f752-125">Section index:</span></span>  <br/> |<span data-ttu-id="5f752-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f752-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5f752-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5f752-127">Row index:</span></span>  <br/> |<span data-ttu-id="5f752-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="5f752-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="5f752-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5f752-129">Cell index:</span></span>  <br/> |<span data-ttu-id="5f752-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="5f752-130">**visSLOSplittable**</span></span> <br/> |
   

