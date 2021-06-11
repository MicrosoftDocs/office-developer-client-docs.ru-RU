---
title: Элемент Cell (SplineKnot Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: Содержит x или y-координаты для точки управления spline или узла spline.
ms.openlocfilehash: 4eb6e2ce47adae20738c0d210ad2dc30f362200d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539371"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="d8c48-103">Элемент Cell (SplineKnot Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d8c48-103">Cell element (SplineKnot Row) (Visio XML)</span></span>

<span data-ttu-id="d8c48-104">Содержит x или y-координаты для точки управления spline или узла spline.</span><span class="sxs-lookup"><span data-stu-id="d8c48-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8c48-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d8c48-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8c48-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d8c48-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d8c48-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d8c48-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d8c48-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d8c48-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d8c48-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d8c48-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d8c48-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d8c48-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d8c48-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="d8c48-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d8c48-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="d8c48-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8c48-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d8c48-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8c48-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8c48-114">Elements and attributes</span></span>

<span data-ttu-id="d8c48-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d8c48-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d8c48-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d8c48-116">Parent elements</span></span>

|<span data-ttu-id="d8c48-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d8c48-117">**Element**</span></span>|<span data-ttu-id="d8c48-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d8c48-118">**Type**</span></span>|<span data-ttu-id="d8c48-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8c48-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8c48-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="d8c48-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d8c48-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="d8c48-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8c48-122">Содержит x или y-координаты для точки управления spline или узла spline.</span><span class="sxs-lookup"><span data-stu-id="d8c48-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8c48-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8c48-123">Child elements</span></span>

|<span data-ttu-id="d8c48-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d8c48-124">**Element**</span></span>|<span data-ttu-id="d8c48-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d8c48-125">**Type**</span></span>|<span data-ttu-id="d8c48-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8c48-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8c48-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="d8c48-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8c48-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="d8c48-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8c48-129">Указывает ссылку на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="d8c48-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d8c48-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8c48-130">Attributes</span></span>

|<span data-ttu-id="d8c48-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d8c48-131">**Attribute**</span></span>|<span data-ttu-id="d8c48-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d8c48-132">**Type**</span></span>|<span data-ttu-id="d8c48-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d8c48-133">**Required**</span></span>|<span data-ttu-id="d8c48-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8c48-134">**Description**</span></span>|<span data-ttu-id="d8c48-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d8c48-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8c48-136">E</span><span class="sxs-lookup"><span data-stu-id="d8c48-136">E</span></span>  <br/> |<span data-ttu-id="d8c48-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c48-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c48-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d8c48-138">optional</span></span>  <br/> |<span data-ttu-id="d8c48-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="d8c48-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="d8c48-140">Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="d8c48-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="d8c48-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d8c48-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="d8c48-142">F</span><span class="sxs-lookup"><span data-stu-id="d8c48-142">F</span></span>  <br/> |<span data-ttu-id="d8c48-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c48-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c48-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="d8c48-144">optional</span></span>  <br/> | <span data-ttu-id="d8c48-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="d8c48-145">Represents the element's formula.</span></span> <span data-ttu-id="d8c48-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="d8c48-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="d8c48-147">"(некоторые формулы)", если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="d8c48-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="d8c48-148">`No Formula` если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="d8c48-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="d8c48-149">`Inh` если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="d8c48-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="d8c48-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="d8c48-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="d8c48-151">Нет</span><span class="sxs-lookup"><span data-stu-id="d8c48-151">N</span></span>  <br/> |<span data-ttu-id="d8c48-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c48-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c48-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d8c48-153">required</span></span>  <br/> |<span data-ttu-id="d8c48-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d8c48-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="d8c48-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d8c48-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="d8c48-156">См. раздел Замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="d8c48-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="d8c48-157">U</span><span class="sxs-lookup"><span data-stu-id="d8c48-157">U</span></span>  <br/> |<span data-ttu-id="d8c48-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c48-158">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c48-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="d8c48-159">optional</span></span>  <br/> |<span data-ttu-id="d8c48-160">Представляет единицу измерения, по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="d8c48-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="d8c48-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="d8c48-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="d8c48-162">V</span><span class="sxs-lookup"><span data-stu-id="d8c48-162">V</span></span>  <br/> |<span data-ttu-id="d8c48-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d8c48-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d8c48-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="d8c48-164">optional</span></span>  <br/> |<span data-ttu-id="d8c48-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="d8c48-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="d8c48-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d8c48-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8c48-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8c48-167">Remarks</span></span>

<span data-ttu-id="d8c48-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d8c48-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="d8c48-169">Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.**</span><span class="sxs-lookup"><span data-stu-id="d8c48-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="d8c48-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d8c48-170">**Value**</span></span>|<span data-ttu-id="d8c48-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8c48-171">**Description**</span></span>|<span data-ttu-id="d8c48-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="d8c48-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8c48-173">X</span><span class="sxs-lookup"><span data-stu-id="d8c48-173">X</span></span>  <br/> |<span data-ttu-id="d8c48-174">X-координата точки управления.</span><span class="sxs-lookup"><span data-stu-id="d8c48-174">The x-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="d8c48-175">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d8c48-175">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="d8c48-176">Да</span><span class="sxs-lookup"><span data-stu-id="d8c48-176">Y</span></span>  <br/> |<span data-ttu-id="d8c48-177">Y-координата точки управления.</span><span class="sxs-lookup"><span data-stu-id="d8c48-177">The y-coordinate of a control point.</span></span>  <br/> |[<span data-ttu-id="d8c48-178">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d8c48-178">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
|<span data-ttu-id="d8c48-179">A</span><span class="sxs-lookup"><span data-stu-id="d8c48-179">A</span></span>  <br/> |<span data-ttu-id="d8c48-180">Один из узлов spline (кроме последнего или первых двух).</span><span class="sxs-lookup"><span data-stu-id="d8c48-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |[<span data-ttu-id="d8c48-181">SplineKnot Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d8c48-181">SplineKnot Row (Geometry Section)</span></span>](splineknot-row-geometry-section.md) <br/> |
   

