---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Содержит ссылку на геометрию пути, с которым связан образ.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425514"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="9a774-103">ClippingPath Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="9a774-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="9a774-104">Содержит ссылку на геометрию пути, с которым связан образ.</span><span class="sxs-lookup"><span data-stu-id="9a774-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9a774-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a774-105">Remarks</span></span>

<span data-ttu-id="9a774-106">Если ячейка **ClippingPath** указывает на действительный путь, изображение обрезается таким образом, чтобы изображение отображалось в пределах пути.</span><span class="sxs-lookup"><span data-stu-id="9a774-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="9a774-107">Если ячейка **ClippingPath** пустая или содержит недопустимый элемент, изображение будет визуализировано с помощью прямоугольного клипа с использованием значений Scale и offset.</span><span class="sxs-lookup"><span data-stu-id="9a774-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9a774-108">Только пути, определенные в разделе [Geometry](geometry-section.md) в таблице свойств фигуры, являются допустимыми записями для ячейки **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="9a774-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="9a774-109">Для определения обтравочного контура изображения нельзя использовать ссылки на несколько страниц.</span><span class="sxs-lookup"><span data-stu-id="9a774-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="9a774-110">Чтобы получить ссылку на ячейку **ClippingPath** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="9a774-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a774-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9a774-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9a774-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="9a774-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="9a774-113">Чтобы получить ссылку на ячейку **ClippingPath** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9a774-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a774-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9a774-114">Section index:</span></span>  <br/> |<span data-ttu-id="9a774-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9a774-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9a774-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9a774-116">Row index:</span></span>  <br/> |<span data-ttu-id="9a774-117">**Висровфореигн**</span><span class="sxs-lookup"><span data-stu-id="9a774-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="9a774-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9a774-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9a774-119">**Висфргнимгклиппингпас**</span><span class="sxs-lookup"><span data-stu-id="9a774-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="9a774-120">Пример</span><span class="sxs-lookup"><span data-stu-id="9a774-120">Example</span></span>

<span data-ttu-id="9a774-121">Можно изменить границу фигуры изображения на овал, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9a774-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="9a774-122">Вставка рисунка на полотно.</span><span class="sxs-lookup"><span data-stu-id="9a774-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="9a774-123">Щелкните рисунок правой кнопкой мыши и выберите пункт **Показать таблицу свойств фигуры**.</span><span class="sxs-lookup"><span data-stu-id="9a774-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="9a774-124">Щелкните правой кнопкой мыши в любом месте таблицы свойств фигуры и выберите команду **Вставить раздел**.</span><span class="sxs-lookup"><span data-stu-id="9a774-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="9a774-125">В диалоговом окне **Вставка раздела** выберите **геометрия** , а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9a774-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="9a774-126">В разделе новый геометрический раздел (например, "Geometry2") удалите все строки, кроме одной.</span><span class="sxs-lookup"><span data-stu-id="9a774-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="9a774-127">Щелкните правой кнопкой мыши оставшуюся строку и выберите команду **изменить тип строки**.</span><span class="sxs-lookup"><span data-stu-id="9a774-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="9a774-128">В диалоговом окне **изменение типа строки** выберите **многоточие** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9a774-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="9a774-129">В разделе **внешнЕе изображение** Задайте формулу для ячейки **ClippingPath** `="Geometry2.Path"` и примите формулу.</span><span class="sxs-lookup"><span data-stu-id="9a774-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

