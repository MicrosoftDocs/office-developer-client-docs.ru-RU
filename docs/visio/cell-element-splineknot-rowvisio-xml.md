---
title: Элемент Cell (строка SplineKnot) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: Содержит координаты X или Y для точки управления сплайна или загона сплайна.
ms.openlocfilehash: 4eb6e2ce47adae20738c0d210ad2dc30f362200d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539371"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="ca929-103">Элемент Cell (строка SplineKnot) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ca929-103">Cell element (SplineKnot Row) (Visio XML)</span></span>

<span data-ttu-id="ca929-104">Содержит координаты X или Y для точки управления сплайна или загона сплайна.</span><span class="sxs-lookup"><span data-stu-id="ca929-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca929-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ca929-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca929-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ca929-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ca929-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ca929-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ca929-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ca929-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ca929-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ca929-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ca929-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ca929-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ca929-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ca929-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ca929-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="ca929-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca929-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ca929-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca929-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca929-114">Elements and attributes</span></span>

<span data-ttu-id="ca929-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ca929-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ca929-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ca929-116">Parent elements</span></span>

|<span data-ttu-id="ca929-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca929-117">**Element**</span></span>|<span data-ttu-id="ca929-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca929-118">**Type**</span></span>|<span data-ttu-id="ca929-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca929-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca929-120">Элемент Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="ca929-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ca929-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="ca929-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ca929-122">Содержит координаты X или Y для точки управления сплайна или загона сплайна.</span><span class="sxs-lookup"><span data-stu-id="ca929-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca929-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ca929-123">Child elements</span></span>

|<span data-ttu-id="ca929-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca929-124">**Element**</span></span>|<span data-ttu-id="ca929-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca929-125">**Type**</span></span>|<span data-ttu-id="ca929-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca929-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca929-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="ca929-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ca929-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ca929-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ca929-129">Указывает ссылку на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="ca929-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ca929-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca929-130">Attributes</span></span>

|<span data-ttu-id="ca929-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ca929-131">**Attribute**</span></span>|<span data-ttu-id="ca929-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca929-132">**Type**</span></span>|<span data-ttu-id="ca929-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ca929-133">**Required**</span></span>|<span data-ttu-id="ca929-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca929-134">**Description**</span></span>|<span data-ttu-id="ca929-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ca929-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca929-136">E</span><span class="sxs-lookup"><span data-stu-id="ca929-136">E</span></span>  <br/> |<span data-ttu-id="ca929-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca929-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ca929-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca929-138">optional</span></span>  <br/> |<span data-ttu-id="ca929-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="ca929-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="ca929-140">Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="ca929-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="ca929-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ca929-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="ca929-142">F</span><span class="sxs-lookup"><span data-stu-id="ca929-142">F</span></span>  <br/> |<span data-ttu-id="ca929-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca929-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ca929-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca929-144">optional</span></span>  <br/> | <span data-ttu-id="ca929-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="ca929-145">Represents the element's formula.</span></span> <span data-ttu-id="ca929-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="ca929-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="ca929-147">'(some formula)', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="ca929-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="ca929-148">`No Formula` если формула удалена или заблокирована локально</span><span class="sxs-lookup"><span data-stu-id="ca929-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="ca929-149">`Inh` если формула унаследована.</span><span class="sxs-lookup"><span data-stu-id="ca929-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="ca929-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="ca929-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="ca929-151">N</span><span class="sxs-lookup"><span data-stu-id="ca929-151">N</span></span>  <br/> |<span data-ttu-id="ca929-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca929-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ca929-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca929-153">required</span></span>  <br/> |<span data-ttu-id="ca929-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca929-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="ca929-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca929-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="ca929-156">См. раздел "Замечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="ca929-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="ca929-157">U</span><span class="sxs-lookup"><span data-stu-id="ca929-157">U</span></span>  <br/> |<span data-ttu-id="ca929-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca929-158">xsd:string</span></span>  <br/> |<span data-ttu-id="ca929-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca929-159">optional</span></span>  <br/> |<span data-ttu-id="ca929-160">Представляет единицу измерения, значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="ca929-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="ca929-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="ca929-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="ca929-162">V</span><span class="sxs-lookup"><span data-stu-id="ca929-162">V</span></span>  <br/> |<span data-ttu-id="ca929-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca929-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ca929-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca929-164">optional</span></span>  <br/> |<span data-ttu-id="ca929-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="ca929-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="ca929-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca929-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca929-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca929-167">Remarks</span></span>

<span data-ttu-id="ca929-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ca929-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="ca929-169">Чтобы определить значения атрибута **N,** допустимого для этого элемента **Cell,** обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ca929-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="ca929-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ca929-170">**Value**</span></span>|<span data-ttu-id="ca929-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca929-171">**Description**</span></span>|<span data-ttu-id="ca929-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="ca929-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca929-173">X</span><span class="sxs-lookup"><span data-stu-id="ca929-173">X</span></span>  <br/> |<span data-ttu-id="ca929-174">X-координата контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="ca929-174">The x-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="ca929-175">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="ca929-175">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="ca929-176">Да</span><span class="sxs-lookup"><span data-stu-id="ca929-176">Y</span></span>  <br/> |<span data-ttu-id="ca929-177">Y-координата контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="ca929-177">The y-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="ca929-178">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="ca929-178">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="ca929-179">A</span><span class="sxs-lookup"><span data-stu-id="ca929-179">A</span></span>  <br/> |<span data-ttu-id="ca929-180">Одна из подмайок сплайна (кроме последней или первой).</span><span class="sxs-lookup"><span data-stu-id="ca929-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |[<span data-ttu-id="ca929-181">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="ca929-181">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
   

