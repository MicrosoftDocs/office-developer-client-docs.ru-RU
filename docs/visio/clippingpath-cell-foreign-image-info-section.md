---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Содержит ссылку на геометрию пути, который связан с изображением.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425514"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="e39d7-103">ClippingPath Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="e39d7-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="e39d7-104">Содержит ссылку на геометрию пути, который связан с изображением.</span><span class="sxs-lookup"><span data-stu-id="e39d7-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e39d7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e39d7-105">Remarks</span></span>

<span data-ttu-id="e39d7-106">Если **ячейка ClippingPath** указывает на допустимый путь, изображение обрезается таким образом, чтобы изображение отрисовылось внутри пути.</span><span class="sxs-lookup"><span data-stu-id="e39d7-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="e39d7-107">Если **ячейка ClippingPath** пуста или содержит недействительный вход, изображение будет отрисовывалось прямоугольным клипом с использованием значений масштабирования и смещения.</span><span class="sxs-lookup"><span data-stu-id="e39d7-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e39d7-108">Допустимы только пути, определенные разделом [Геометрия](geometry-section.md) в shapeSheet изображения, для ячейки **ClippingPath.**</span><span class="sxs-lookup"><span data-stu-id="e39d7-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="e39d7-109">Ссылки на перекрестный лист нельзя использовать для определения пути обрезки изображений.</span><span class="sxs-lookup"><span data-stu-id="e39d7-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="e39d7-110">Чтобы получить ссылку на ячейку **ClippingPath** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e39d7-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e39d7-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e39d7-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e39d7-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="e39d7-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="e39d7-113">Чтобы получить ссылку на ячейку **ClippingPath** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e39d7-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e39d7-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e39d7-114">Section index:</span></span>  <br/> |<span data-ttu-id="e39d7-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e39d7-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e39d7-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e39d7-116">Row index:</span></span>  <br/> |<span data-ttu-id="e39d7-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="e39d7-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="e39d7-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e39d7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e39d7-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="e39d7-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="e39d7-120">Пример</span><span class="sxs-lookup"><span data-stu-id="e39d7-120">Example</span></span>

<span data-ttu-id="e39d7-121">Вы можете изменить очертания изображения на овал, делая следующее:</span><span class="sxs-lookup"><span data-stu-id="e39d7-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="e39d7-122">Вставьте изображение на рисунок холста.</span><span class="sxs-lookup"><span data-stu-id="e39d7-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="e39d7-123">Щелкните правой кнопкой мыши изображение, а затем **выберите Show ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="e39d7-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="e39d7-124">Щелкните правой кнопкой мыши в любом месте таблицы ShapeSheet и выберите **раздел Вставки**.</span><span class="sxs-lookup"><span data-stu-id="e39d7-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="e39d7-125">В **диалоговом окне Вставить** раздел выберите **геометрию** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="e39d7-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="e39d7-126">В новом разделе Геометрия (например, "Geometry2") удалите все строки, кроме одной строки.</span><span class="sxs-lookup"><span data-stu-id="e39d7-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="e39d7-127">Щелкните правой кнопкой мыши оставшиеся строки и нажмите **кнопку Изменить строку типа**.</span><span class="sxs-lookup"><span data-stu-id="e39d7-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="e39d7-128">В **диалоговом окне Тип** строки изменения выберите **Ellipse** и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="e39d7-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="e39d7-129">В разделе **Foreign Image** установите формулу ячейки **ClippingPath** и  `="Geometry2.Path"` примите ее.</span><span class="sxs-lookup"><span data-stu-id="e39d7-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

