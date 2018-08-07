---
title: Ячейка ClippingPath (раздел "Сведения о внешнем изображении")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Содержит ссылку на геометрии путь, заключенное изображения.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813385"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="fceae-103">Ячейка ClippingPath (раздел "Сведения о внешнем изображении")</span><span class="sxs-lookup"><span data-stu-id="fceae-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="fceae-104">Содержит ссылку на геометрии путь, заключенное изображения.</span><span class="sxs-lookup"><span data-stu-id="fceae-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fceae-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="fceae-105">Remarks</span></span>

<span data-ttu-id="fceae-106">Если ячейка **ClippingPath** указывает допустимый путь, изображение обрезается, чтобы изображения отображается в пути.</span><span class="sxs-lookup"><span data-stu-id="fceae-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="fceae-107">Если ячейка **ClippingPath** пуст или содержит недопустимый запись, изображения будет отображаться с прямоугольной картинок, с помощью значения масштабирования и смещение.</span><span class="sxs-lookup"><span data-stu-id="fceae-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fceae-108">Только пути, определенные в раздел [геометрии](geometry-section.md) в таблице свойств фигуры изображения, вводимых в ячейке **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="fceae-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="fceae-109">Ссылки на разных листах не может использоваться для определения пути отсечения изображения.</span><span class="sxs-lookup"><span data-stu-id="fceae-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="fceae-110">Для получения ссылки на ячейки **ClippingPath** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="fceae-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fceae-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fceae-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fceae-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="fceae-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="fceae-113">Для получения ссылки на ячейки **ClippingPath** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fceae-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fceae-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fceae-114">Section index:</span></span>  <br/> |<span data-ttu-id="fceae-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fceae-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fceae-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fceae-116">Row index:</span></span>  <br/> |<span data-ttu-id="fceae-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="fceae-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="fceae-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fceae-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fceae-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="fceae-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="fceae-120">Пример</span><span class="sxs-lookup"><span data-stu-id="fceae-120">Example</span></span>

<span data-ttu-id="fceae-121">Можно переместить ограничивающего фигуры изображение овала, выполнив следующие:</span><span class="sxs-lookup"><span data-stu-id="fceae-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="fceae-122">Вставьте рисунок на полотно.</span><span class="sxs-lookup"><span data-stu-id="fceae-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="fceae-123">Щелкните правой кнопкой мыши изображение и выберите пункт **Показать таблицу свойств фигуры**.</span><span class="sxs-lookup"><span data-stu-id="fceae-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="fceae-124">Щелкните правой кнопкой мыши в таблице свойств фигуры и выберите **Вставить раздел**.</span><span class="sxs-lookup"><span data-stu-id="fceae-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="fceae-125">В диалоговом окне **Вставить раздел,** выберите **геометрии** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fceae-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="fceae-126">Удалите только один строку, в новый раздел геометрии (например, «Geometry2»).</span><span class="sxs-lookup"><span data-stu-id="fceae-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="fceae-127">Щелкните правой кнопкой мыши оставшиеся строки и нажмите кнопку **Изменить тип строки**.</span><span class="sxs-lookup"><span data-stu-id="fceae-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="fceae-128">В диалоговом окне **Изменение типа строки** выберите **эллипс** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fceae-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="fceae-129">В разделе **Внешний рисунок** задать формулу для ячейки **ClippingPath** для `="Geometry2.Path"` и примите формулу.</span><span class="sxs-lookup"><span data-stu-id="fceae-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

