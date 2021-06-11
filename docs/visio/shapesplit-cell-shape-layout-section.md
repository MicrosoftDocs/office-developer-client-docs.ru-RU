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
description: Указывает, может ли эта фигура разделить фигуры, которые можно разделить.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423561"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="51cc7-103">ShapeSplit Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="51cc7-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="51cc7-104">Указывает, может ли эта фигура разделить фигуры, которые можно разделить.</span><span class="sxs-lookup"><span data-stu-id="51cc7-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="51cc7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="51cc7-105">**Value**</span></span>|<span data-ttu-id="51cc7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51cc7-106">**Description**</span></span>|<span data-ttu-id="51cc7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="51cc7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="51cc7-108">0</span><span class="sxs-lookup"><span data-stu-id="51cc7-108">0</span></span>  <br/> | <span data-ttu-id="51cc7-109">Не позволяйте этой фигуре разделять другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="51cc7-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="51cc7-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="51cc7-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="51cc7-111">1</span><span class="sxs-lookup"><span data-stu-id="51cc7-111">1</span></span>  <br/> | <span data-ttu-id="51cc7-112">Разрешить эту фигуру разделить другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="51cc7-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="51cc7-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="51cc7-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51cc7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="51cc7-114">Remarks</span></span>

<span data-ttu-id="51cc7-115">Фигура, которая может разделить другие фигуры, должна быть либо двухдюймовой, либо 1-D-фигурой.</span><span class="sxs-lookup"><span data-stu-id="51cc7-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="51cc7-116">Автоматическое разделение фигур включено и отключено на трех различных уровнях: приложения, страницы и формы.</span><span class="sxs-lookup"><span data-stu-id="51cc7-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="51cc7-117">По умолчанию разделение включено на уровне приложения и страницы; для фигур он зависит от типа рисования.</span><span class="sxs-lookup"><span data-stu-id="51cc7-117">By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="51cc7-118">Чтобы включить или отключить разделение на уровне  приложения, воспользуйтесь параметром разделения соединители Enable на вкладке **Advanced** диалогового окна **Visio Options** (щелкните вкладку **Файл,** щелкните Параметры **и** нажмите кнопку **Advanced).**</span><span class="sxs-lookup"><span data-stu-id="51cc7-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="51cc7-119">Чтобы включить или отключить разделение на странице, см. ячейку PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="51cc7-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="51cc7-120">Чтобы 1-D форма была разделена, см. в разделе ShapeSplittable cell.</span><span class="sxs-lookup"><span data-stu-id="51cc7-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="51cc7-121">Чтобы получить ссылку на ячейку ShapeSplit по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="51cc7-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51cc7-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="51cc7-122">Cell name:</span></span>  <br/> | <span data-ttu-id="51cc7-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="51cc7-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="51cc7-124">Чтобы получить ссылку на ячейку ShapeSplit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="51cc7-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51cc7-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="51cc7-125">Section index:</span></span>  <br/> |<span data-ttu-id="51cc7-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51cc7-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51cc7-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="51cc7-127">Row index:</span></span>  <br/> |<span data-ttu-id="51cc7-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="51cc7-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="51cc7-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="51cc7-129">Cell index:</span></span>  <br/> |<span data-ttu-id="51cc7-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="51cc7-130">**visSLOSplit**</span></span> <br/> |
   

