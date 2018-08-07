---
title: Элемент ячейки (строка RelLineTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: Содержит x- или y координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 73930b15a62a483b38da4791511f735ac81bb1a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813366"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="ffdf3-103">Элемент ячейки (строка RelLineTo) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ffdf3-103">Cell element (RelLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="ffdf3-104">Содержит x- или y координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffdf3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ffdf3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffdf3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ffdf3-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ffdf3-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ffdf3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ffdf3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ffdf3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ffdf3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ffdf3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ffdf3-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="ffdf3-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ffdf3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ffdf3-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ffdf3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ffdf3-114">Elements and attributes</span></span>

<span data-ttu-id="ffdf3-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ffdf3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ffdf3-116">Parent elements</span></span>

|<span data-ttu-id="ffdf3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-117">**Element**</span></span>|<span data-ttu-id="ffdf3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-118">**Type**</span></span>|<span data-ttu-id="ffdf3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ffdf3-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="ffdf3-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ffdf3-121">RelLineTo_Type</span><span class="sxs-lookup"><span data-stu-id="ffdf3-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ffdf3-122">Содержит x- или y координаты окончания вершины отрезка прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ffdf3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ffdf3-123">Child elements</span></span>

|<span data-ttu-id="ffdf3-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-124">**Element**</span></span>|<span data-ttu-id="ffdf3-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-125">**Type**</span></span>|<span data-ttu-id="ffdf3-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ffdf3-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="ffdf3-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ffdf3-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ffdf3-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ffdf3-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ffdf3-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ffdf3-130">Attributes</span></span>

|<span data-ttu-id="ffdf3-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-131">**Attribute**</span></span>|<span data-ttu-id="ffdf3-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-132">**Type**</span></span>|<span data-ttu-id="ffdf3-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-133">**Required**</span></span>|<span data-ttu-id="ffdf3-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-134">**Description**</span></span>|<span data-ttu-id="ffdf3-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ffdf3-136">E</span><span class="sxs-lookup"><span data-stu-id="ffdf3-136">E</span></span>  <br/> |<span data-ttu-id="ffdf3-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ffdf3-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ffdf3-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ffdf3-138">optional</span></span>  <br/> |<span data-ttu-id="ffdf3-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="ffdf3-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="ffdf3-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="ffdf3-142">F</span><span class="sxs-lookup"><span data-stu-id="ffdf3-142">F</span></span>  <br/> |<span data-ttu-id="ffdf3-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ffdf3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ffdf3-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="ffdf3-144">optional</span></span>  <br/> | <span data-ttu-id="ffdf3-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-145">Represents the element's formula.</span></span> <span data-ttu-id="ffdf3-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="ffdf3-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="ffdf3-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="ffdf3-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="ffdf3-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="ffdf3-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="ffdf3-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="ffdf3-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="ffdf3-151">N</span><span class="sxs-lookup"><span data-stu-id="ffdf3-151">N</span></span>  <br/> |<span data-ttu-id="ffdf3-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ffdf3-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ffdf3-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ffdf3-153">required</span></span>  <br/> |<span data-ttu-id="ffdf3-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="ffdf3-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="ffdf3-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="ffdf3-157">U</span><span class="sxs-lookup"><span data-stu-id="ffdf3-157">U</span></span>  <br/> |<span data-ttu-id="ffdf3-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ffdf3-158">xsd:string</span></span>  <br/> |<span data-ttu-id="ffdf3-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="ffdf3-159">optional</span></span>  <br/> |<span data-ttu-id="ffdf3-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="ffdf3-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="ffdf3-162">V</span><span class="sxs-lookup"><span data-stu-id="ffdf3-162">V</span></span>  <br/> |<span data-ttu-id="ffdf3-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ffdf3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ffdf3-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="ffdf3-164">optional</span></span>  <br/> |<span data-ttu-id="ffdf3-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="ffdf3-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffdf3-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="ffdf3-167">Remarks</span></span>

<span data-ttu-id="ffdf3-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="ffdf3-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="ffdf3-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="ffdf3-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-170">**Value**</span></span>|<span data-ttu-id="ffdf3-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-171">**Description**</span></span>|<span data-ttu-id="ffdf3-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="ffdf3-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ffdf3-173">X </span><span class="sxs-lookup"><span data-stu-id="ffdf3-173">X</span></span>  <br/> |<span data-ttu-id="ffdf3-174">X координата конца вершины сегмента прямой ширине фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |[<span data-ttu-id="ffdf3-175">Строка RelLineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="ffdf3-175">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="ffdf3-176">Да</span><span class="sxs-lookup"><span data-stu-id="ffdf3-176">Y</span></span>  <br/> |<span data-ttu-id="ffdf3-177">Координата конца вершины сегмента прямой высоте фигуры.</span><span class="sxs-lookup"><span data-stu-id="ffdf3-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |[<span data-ttu-id="ffdf3-178">Строка RelLineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="ffdf3-178">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
   

