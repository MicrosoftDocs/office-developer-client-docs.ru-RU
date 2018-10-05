---
title: Элемент ячейки (строка SplineKnot) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: Содержит x - или y координаты точки управления сплайн или число узлов сплайна.
ms.openlocfilehash: 1f2ddbcf7b750f2c2de983e16861070c7305fc3a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395121"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="c7692-103">Элемент ячейки (строка SplineKnot) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c7692-103">Cell element (SplineKnot Row) ('Visio XML')</span></span>

<span data-ttu-id="c7692-104">Содержит x - или y координаты точки управления сплайн или число узлов сплайна.</span><span class="sxs-lookup"><span data-stu-id="c7692-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7692-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c7692-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7692-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c7692-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c7692-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c7692-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c7692-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c7692-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c7692-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c7692-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c7692-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c7692-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c7692-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c7692-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c7692-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="c7692-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c7692-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c7692-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c7692-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c7692-114">Elements and attributes</span></span>

<span data-ttu-id="c7692-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c7692-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c7692-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c7692-116">Parent elements</span></span>

|<span data-ttu-id="c7692-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c7692-117">**Element**</span></span>|<span data-ttu-id="c7692-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c7692-118">**Type**</span></span>|<span data-ttu-id="c7692-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7692-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c7692-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="c7692-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c7692-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="c7692-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c7692-122">Содержит x - или y координаты точки управления сплайн или число узлов сплайна.</span><span class="sxs-lookup"><span data-stu-id="c7692-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c7692-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c7692-123">Child elements</span></span>

|<span data-ttu-id="c7692-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c7692-124">**Element**</span></span>|<span data-ttu-id="c7692-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c7692-125">**Type**</span></span>|<span data-ttu-id="c7692-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7692-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c7692-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c7692-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c7692-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c7692-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c7692-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="c7692-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c7692-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c7692-130">Attributes</span></span>

|<span data-ttu-id="c7692-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c7692-131">**Attribute**</span></span>|<span data-ttu-id="c7692-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c7692-132">**Type**</span></span>|<span data-ttu-id="c7692-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c7692-133">**Required**</span></span>|<span data-ttu-id="c7692-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7692-134">**Description**</span></span>|<span data-ttu-id="c7692-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c7692-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c7692-136">E</span><span class="sxs-lookup"><span data-stu-id="c7692-136">E</span></span>  <br/> |<span data-ttu-id="c7692-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="c7692-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c7692-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c7692-138">optional</span></span>  <br/> |<span data-ttu-id="c7692-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7692-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c7692-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="c7692-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c7692-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c7692-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c7692-142">F</span><span class="sxs-lookup"><span data-stu-id="c7692-142">F</span></span>  <br/> |<span data-ttu-id="c7692-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="c7692-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c7692-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="c7692-144">optional</span></span>  <br/> | <span data-ttu-id="c7692-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="c7692-145">Represents the element's formula.</span></span> <span data-ttu-id="c7692-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="c7692-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c7692-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="c7692-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c7692-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="c7692-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c7692-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="c7692-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c7692-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="c7692-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="c7692-151">N</span><span class="sxs-lookup"><span data-stu-id="c7692-151">N</span></span>  <br/> |<span data-ttu-id="c7692-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="c7692-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c7692-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c7692-153">required</span></span>  <br/> |<span data-ttu-id="c7692-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7692-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c7692-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7692-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c7692-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="c7692-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c7692-157">U</span><span class="sxs-lookup"><span data-stu-id="c7692-157">U</span></span>  <br/> |<span data-ttu-id="c7692-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="c7692-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c7692-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="c7692-159">optional</span></span>  <br/> |<span data-ttu-id="c7692-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="c7692-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c7692-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="c7692-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c7692-162">V</span><span class="sxs-lookup"><span data-stu-id="c7692-162">V</span></span>  <br/> |<span data-ttu-id="c7692-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="c7692-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c7692-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="c7692-164">optional</span></span>  <br/> |<span data-ttu-id="c7692-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="c7692-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c7692-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7692-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7692-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7692-167">Remarks</span></span>

<span data-ttu-id="c7692-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7692-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c7692-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="c7692-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c7692-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c7692-170">**Value**</span></span>|<span data-ttu-id="c7692-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7692-171">**Description**</span></span>|<span data-ttu-id="c7692-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="c7692-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7692-173">X </span><span class="sxs-lookup"><span data-stu-id="c7692-173">X</span></span>  <br/> |<span data-ttu-id="c7692-174">X координата точки управления.</span><span class="sxs-lookup"><span data-stu-id="c7692-174">The x-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="c7692-175">Строка SplineKnot (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="c7692-175">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="c7692-176">Да</span><span class="sxs-lookup"><span data-stu-id="c7692-176">Y</span></span>  <br/> |<span data-ttu-id="c7692-177">Контрольная точка по оси y.</span><span class="sxs-lookup"><span data-stu-id="c7692-177">The y-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="c7692-178">Строка SplineKnot (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="c7692-178">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="c7692-179">A</span><span class="sxs-lookup"><span data-stu-id="c7692-179">A</span></span>  <br/> |<span data-ttu-id="c7692-180">Один из узлов сплайна (кроме последней или первых двух).</span><span class="sxs-lookup"><span data-stu-id="c7692-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |[<span data-ttu-id="c7692-181">Строка SplineKnot (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="c7692-181">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
   

