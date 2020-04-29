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
description: Указывает, можно ли разделить эту одномерное фигуру.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427075"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="5640f-103">ShapeSplittable Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="5640f-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5640f-104">Указывает, можно ли разделить эту одномерное фигуру.</span><span class="sxs-lookup"><span data-stu-id="5640f-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="5640f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5640f-105">**Value**</span></span>|<span data-ttu-id="5640f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5640f-106">**Description**</span></span>|<span data-ttu-id="5640f-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="5640f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5640f-108">нуль</span><span class="sxs-lookup"><span data-stu-id="5640f-108">0</span></span>  <br/> | <span data-ttu-id="5640f-109">Не разрешать разделение этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="5640f-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5640f-110">**висслосплиттабленоне**</span><span class="sxs-lookup"><span data-stu-id="5640f-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="5640f-111">1,1</span><span class="sxs-lookup"><span data-stu-id="5640f-111">1</span></span>  <br/> | <span data-ttu-id="5640f-112">Разрешите разделение этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="5640f-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5640f-113">**висслосплиттаблеаллов**</span><span class="sxs-lookup"><span data-stu-id="5640f-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5640f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5640f-114">Remarks</span></span>

<span data-ttu-id="5640f-115">Поведение по умолчанию для соединителей и других одномерной фигуры зависит от типа рисунка.</span><span class="sxs-lookup"><span data-stu-id="5640f-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="5640f-116">Автоматическое разбиение на фигуры включено и отключено на трех разных уровнях: приложение, страница и фигура.</span><span class="sxs-lookup"><span data-stu-id="5640f-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="5640f-117">По умолчанию разбивка включена на уровне приложения и на уровне страниц.</span><span class="sxs-lookup"><span data-stu-id="5640f-117">By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="5640f-118">Чтобы включить или отключить разбиение на уровне приложения, используйте параметр **включить разделение соединителей** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , выберите пункт **Параметры**и нажмите кнопку **Дополнительно** ).</span><span class="sxs-lookup"><span data-stu-id="5640f-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="5640f-119">Чтобы включить или отключить разделение на странице, просмотрите ячейку [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="5640f-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5640f-120">Чтобы фигура могла разбивать фигуры сплиттабле, представленные в ячейке [ShapeSplit](shapesplit-cell-shape-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="5640f-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5640f-121">Чтобы получить ссылку на ячейку ShapeSplittable по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5640f-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5640f-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5640f-122">Cell name:</span></span>  <br/> | <span data-ttu-id="5640f-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="5640f-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="5640f-124">Чтобы получить ссылку на ячейку ShapeSplittable по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5640f-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5640f-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5640f-125">Section index:</span></span>  <br/> |<span data-ttu-id="5640f-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5640f-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5640f-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5640f-127">Row index:</span></span>  <br/> |<span data-ttu-id="5640f-128">**висровшапелайаут**</span><span class="sxs-lookup"><span data-stu-id="5640f-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="5640f-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5640f-129">Cell index:</span></span>  <br/> |<span data-ttu-id="5640f-130">**висслосплиттабле**</span><span class="sxs-lookup"><span data-stu-id="5640f-130">**visSLOSplittable**</span></span> <br/> |
   

