---
title: Ячейка ShapeSplit (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Указывает, будет ли эта фигура разделять фигуры, которые можно разбить таблицу.
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814805"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="a30ac-103">Ячейка ShapeSplit (раздел "Макет фигуры")</span><span class="sxs-lookup"><span data-stu-id="a30ac-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="a30ac-104">Указывает, будет ли эта фигура разделять фигуры, которые можно разбить таблицу.</span><span class="sxs-lookup"><span data-stu-id="a30ac-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="a30ac-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a30ac-105">**Value**</span></span>|<span data-ttu-id="a30ac-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a30ac-106">**Description**</span></span>|<span data-ttu-id="a30ac-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="a30ac-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a30ac-108">0</span><span class="sxs-lookup"><span data-stu-id="a30ac-108">0</span></span>  <br/> | <span data-ttu-id="a30ac-109">Не разрешать этой фигуры для разделения другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="a30ac-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="a30ac-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="a30ac-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="a30ac-111">1</span><span class="sxs-lookup"><span data-stu-id="a30ac-111">1</span></span>  <br/> | <span data-ttu-id="a30ac-112">Разрешить этой фигуры для разделения другие фигуры.</span><span class="sxs-lookup"><span data-stu-id="a30ac-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="a30ac-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="a30ac-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a30ac-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a30ac-114">Remarks</span></span>

<span data-ttu-id="a30ac-115">Фигура, который можно разделить другие фигуры должен быть плоских фигур или 1 D размещаемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="a30ac-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="a30ac-116">Автоматическое разделение фигур включена и отключена три уровня: приложения, страницы и фигуры.</span><span class="sxs-lookup"><span data-stu-id="a30ac-116">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape.</span></span> <span data-ttu-id="a30ac-117">По умолчанию разделение включена на приложения и уровне страницы; для фигур он изменяется в соответствии с тип графического.</span><span class="sxs-lookup"><span data-stu-id="a30ac-117">By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="a30ac-118">Чтобы включить или отключить разделение на уровне приложения, используйте параметр **включить разделение соединительной линии** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , выберите пункт **Параметры**и нажмите кнопку ** Расширенный**).</span><span class="sxs-lookup"><span data-stu-id="a30ac-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="a30ac-119">Чтобы включить или отключить разбиение на страницы, обратитесь к разделу PageShapeSplit ячейки.</span><span class="sxs-lookup"><span data-stu-id="a30ac-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="a30ac-120">Чтобы вызвать одномерной фигуры иметь возможность разделения, обратитесь к разделу ячейки ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="a30ac-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="a30ac-121">Чтобы получить ссылку на ячейку ShapeSplit по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="a30ac-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a30ac-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a30ac-122">Cell name:</span></span>  <br/> | <span data-ttu-id="a30ac-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="a30ac-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="a30ac-124">Для получения ссылки на ячейки ShapeSplit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a30ac-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a30ac-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a30ac-125">Section index:</span></span>  <br/> |<span data-ttu-id="a30ac-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a30ac-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a30ac-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a30ac-127">Row index:</span></span>  <br/> |<span data-ttu-id="a30ac-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="a30ac-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="a30ac-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a30ac-129">Cell index:</span></span>  <br/> |<span data-ttu-id="a30ac-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="a30ac-130">**visSLOSplit**</span></span> <br/> |
   

