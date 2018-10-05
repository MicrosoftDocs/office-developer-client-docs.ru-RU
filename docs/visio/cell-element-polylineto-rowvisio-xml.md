---
title: Элемент ячейки (строка PolyLineTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит x или y координаты точки ломаной или формулы ломаной.
ms.openlocfilehash: 7a27cc5a4c2b6c9833263a28bbcadc40f08d8e70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398656"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="7daf8-103">Элемент ячейки (строка PolyLineTo) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7daf8-103">Cell element (PolyLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="7daf8-104">Содержит x или y координаты точки ломаной или формулы ломаной.</span><span class="sxs-lookup"><span data-stu-id="7daf8-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7daf8-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7daf8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7daf8-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7daf8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7daf8-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7daf8-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7daf8-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7daf8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7daf8-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7daf8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7daf8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7daf8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7daf8-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7daf8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7daf8-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="7daf8-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7daf8-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7daf8-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7daf8-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7daf8-114">Elements and attributes</span></span>

<span data-ttu-id="7daf8-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7daf8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7daf8-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7daf8-116">Parent elements</span></span>

|<span data-ttu-id="7daf8-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7daf8-117">**Element**</span></span>|<span data-ttu-id="7daf8-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7daf8-118">**Type**</span></span>|<span data-ttu-id="7daf8-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7daf8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7daf8-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="7daf8-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7daf8-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="7daf8-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7daf8-122">Содержит x или y координаты точки ломаной или формулы ломаной.</span><span class="sxs-lookup"><span data-stu-id="7daf8-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7daf8-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7daf8-123">Child elements</span></span>

|<span data-ttu-id="7daf8-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7daf8-124">**Element**</span></span>|<span data-ttu-id="7daf8-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7daf8-125">**Type**</span></span>|<span data-ttu-id="7daf8-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7daf8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7daf8-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="7daf8-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7daf8-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="7daf8-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7daf8-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="7daf8-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7daf8-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7daf8-130">Attributes</span></span>

|<span data-ttu-id="7daf8-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7daf8-131">**Attribute**</span></span>|<span data-ttu-id="7daf8-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7daf8-132">**Type**</span></span>|<span data-ttu-id="7daf8-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7daf8-133">**Required**</span></span>|<span data-ttu-id="7daf8-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7daf8-134">**Description**</span></span>|<span data-ttu-id="7daf8-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7daf8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7daf8-136">E</span><span class="sxs-lookup"><span data-stu-id="7daf8-136">E</span></span>  <br/> |<span data-ttu-id="7daf8-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7daf8-137">xsd:string</span></span>  <br/> |<span data-ttu-id="7daf8-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="7daf8-138">optional</span></span>  <br/> |<span data-ttu-id="7daf8-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="7daf8-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="7daf8-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="7daf8-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="7daf8-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7daf8-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="7daf8-142">F</span><span class="sxs-lookup"><span data-stu-id="7daf8-142">F</span></span>  <br/> |<span data-ttu-id="7daf8-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7daf8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="7daf8-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="7daf8-144">optional</span></span>  <br/> | <span data-ttu-id="7daf8-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="7daf8-145">Represents the element's formula.</span></span> <span data-ttu-id="7daf8-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="7daf8-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="7daf8-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="7daf8-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="7daf8-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="7daf8-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="7daf8-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="7daf8-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="7daf8-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="7daf8-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="7daf8-151">N</span><span class="sxs-lookup"><span data-stu-id="7daf8-151">N</span></span>  <br/> |<span data-ttu-id="7daf8-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7daf8-152">xsd:string</span></span>  <br/> |<span data-ttu-id="7daf8-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7daf8-153">required</span></span>  <br/> |<span data-ttu-id="7daf8-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="7daf8-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="7daf8-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="7daf8-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="7daf8-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="7daf8-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="7daf8-157">U</span><span class="sxs-lookup"><span data-stu-id="7daf8-157">U</span></span>  <br/> |<span data-ttu-id="7daf8-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7daf8-158">xsd:string</span></span>  <br/> |<span data-ttu-id="7daf8-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="7daf8-159">optional</span></span>  <br/> |<span data-ttu-id="7daf8-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="7daf8-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="7daf8-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="7daf8-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="7daf8-162">V</span><span class="sxs-lookup"><span data-stu-id="7daf8-162">V</span></span>  <br/> |<span data-ttu-id="7daf8-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7daf8-163">xsd:string</span></span>  <br/> |<span data-ttu-id="7daf8-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="7daf8-164">optional</span></span>  <br/> |<span data-ttu-id="7daf8-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="7daf8-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="7daf8-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="7daf8-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7daf8-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="7daf8-167">Remarks</span></span>

<span data-ttu-id="7daf8-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="7daf8-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="7daf8-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="7daf8-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="7daf8-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7daf8-170">**Value**</span></span>|<span data-ttu-id="7daf8-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7daf8-171">**Description**</span></span>|<span data-ttu-id="7daf8-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="7daf8-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7daf8-173">X </span><span class="sxs-lookup"><span data-stu-id="7daf8-173">X</span></span>  <br/> |<span data-ttu-id="7daf8-174">X координата конца вершины ломаной.</span><span class="sxs-lookup"><span data-stu-id="7daf8-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="7daf8-175">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="7daf8-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="7daf8-176">Да</span><span class="sxs-lookup"><span data-stu-id="7daf8-176">Y</span></span>  <br/> |<span data-ttu-id="7daf8-177">Конечный вершины ломаной по оси y.</span><span class="sxs-lookup"><span data-stu-id="7daf8-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="7daf8-178">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="7daf8-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="7daf8-179">A</span><span class="sxs-lookup"><span data-stu-id="7daf8-179">A</span></span>  <br/> |<span data-ttu-id="7daf8-180">Формула ломаной.</span><span class="sxs-lookup"><span data-stu-id="7daf8-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="7daf8-181">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="7daf8-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

