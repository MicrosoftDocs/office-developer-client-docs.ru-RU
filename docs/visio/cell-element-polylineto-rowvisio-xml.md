---
title: Элемент Cell (строка PolyLineTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит координаты X или Y последней точки многолинейной или многолинейной формулы.
ms.openlocfilehash: b85784a41f4192895f17390f5473757c4bb09166
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539462"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="f7a19-103">Элемент Cell (строка PolyLineTo) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f7a19-103">Cell element (PolyLineTo Row) (Visio XML)</span></span>

<span data-ttu-id="f7a19-104">Содержит координаты X или Y последней точки многолинейной или многолинейной формулы.</span><span class="sxs-lookup"><span data-stu-id="f7a19-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7a19-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f7a19-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7a19-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f7a19-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f7a19-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f7a19-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f7a19-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f7a19-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f7a19-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f7a19-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f7a19-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f7a19-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f7a19-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f7a19-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f7a19-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="f7a19-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f7a19-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f7a19-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f7a19-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f7a19-114">Elements and attributes</span></span>

<span data-ttu-id="f7a19-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f7a19-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f7a19-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f7a19-116">Parent elements</span></span>

|<span data-ttu-id="f7a19-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f7a19-117">**Element**</span></span>|<span data-ttu-id="f7a19-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f7a19-118">**Type**</span></span>|<span data-ttu-id="f7a19-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7a19-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7a19-120">Элемент Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="f7a19-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f7a19-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="f7a19-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7a19-122">Содержит координаты X или Y последней точки многолинейной или многолинейной формулы.</span><span class="sxs-lookup"><span data-stu-id="f7a19-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7a19-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f7a19-123">Child elements</span></span>

|<span data-ttu-id="f7a19-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f7a19-124">**Element**</span></span>|<span data-ttu-id="f7a19-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f7a19-125">**Type**</span></span>|<span data-ttu-id="f7a19-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7a19-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7a19-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="f7a19-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7a19-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="f7a19-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7a19-129">Указывает ссылку на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="f7a19-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f7a19-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f7a19-130">Attributes</span></span>

|<span data-ttu-id="f7a19-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f7a19-131">**Attribute**</span></span>|<span data-ttu-id="f7a19-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f7a19-132">**Type**</span></span>|<span data-ttu-id="f7a19-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f7a19-133">**Required**</span></span>|<span data-ttu-id="f7a19-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7a19-134">**Description**</span></span>|<span data-ttu-id="f7a19-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f7a19-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f7a19-136">E</span><span class="sxs-lookup"><span data-stu-id="f7a19-136">E</span></span>  <br/> |<span data-ttu-id="f7a19-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f7a19-137">xsd:string</span></span>  <br/> |<span data-ttu-id="f7a19-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f7a19-138">optional</span></span>  <br/> |<span data-ttu-id="f7a19-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="f7a19-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="f7a19-140">Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="f7a19-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="f7a19-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f7a19-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="f7a19-142">F</span><span class="sxs-lookup"><span data-stu-id="f7a19-142">F</span></span>  <br/> |<span data-ttu-id="f7a19-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f7a19-143">xsd:string</span></span>  <br/> |<span data-ttu-id="f7a19-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="f7a19-144">optional</span></span>  <br/> | <span data-ttu-id="f7a19-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="f7a19-145">Represents the element's formula.</span></span> <span data-ttu-id="f7a19-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="f7a19-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="f7a19-147">'(some formula)', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="f7a19-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="f7a19-148">`No Formula` если формула удалена или заблокирована локально</span><span class="sxs-lookup"><span data-stu-id="f7a19-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="f7a19-149">`Inh` если формула унаследована.</span><span class="sxs-lookup"><span data-stu-id="f7a19-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="f7a19-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="f7a19-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="f7a19-151">N</span><span class="sxs-lookup"><span data-stu-id="f7a19-151">N</span></span>  <br/> |<span data-ttu-id="f7a19-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f7a19-152">xsd:string</span></span>  <br/> |<span data-ttu-id="f7a19-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f7a19-153">required</span></span>  <br/> |<span data-ttu-id="f7a19-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f7a19-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="f7a19-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f7a19-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="f7a19-156">См. раздел "Замечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="f7a19-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="f7a19-157">U</span><span class="sxs-lookup"><span data-stu-id="f7a19-157">U</span></span>  <br/> |<span data-ttu-id="f7a19-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f7a19-158">xsd:string</span></span>  <br/> |<span data-ttu-id="f7a19-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="f7a19-159">optional</span></span>  <br/> |<span data-ttu-id="f7a19-160">Представляет единицу измерения, значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="f7a19-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="f7a19-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="f7a19-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="f7a19-162">V</span><span class="sxs-lookup"><span data-stu-id="f7a19-162">V</span></span>  <br/> |<span data-ttu-id="f7a19-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f7a19-163">xsd:string</span></span>  <br/> |<span data-ttu-id="f7a19-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="f7a19-164">optional</span></span>  <br/> |<span data-ttu-id="f7a19-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="f7a19-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="f7a19-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f7a19-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7a19-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7a19-167">Remarks</span></span>

<span data-ttu-id="f7a19-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f7a19-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="f7a19-169">Чтобы определить значения атрибута **N,** допустимого для этого элемента Cell, обратитесь к таблице **ниже.**</span><span class="sxs-lookup"><span data-stu-id="f7a19-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="f7a19-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f7a19-170">**Value**</span></span>|<span data-ttu-id="f7a19-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7a19-171">**Description**</span></span>|<span data-ttu-id="f7a19-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="f7a19-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a19-173">X</span><span class="sxs-lookup"><span data-stu-id="f7a19-173">X</span></span>  <br/> |<span data-ttu-id="f7a19-174">X-координата конечной вершины многолинейной линии.</span><span class="sxs-lookup"><span data-stu-id="f7a19-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="f7a19-175">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f7a19-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="f7a19-176">Да</span><span class="sxs-lookup"><span data-stu-id="f7a19-176">Y</span></span>  <br/> |<span data-ttu-id="f7a19-177">Y-координата конечной вершины многолинейной линии.</span><span class="sxs-lookup"><span data-stu-id="f7a19-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="f7a19-178">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f7a19-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="f7a19-179">A</span><span class="sxs-lookup"><span data-stu-id="f7a19-179">A</span></span>  <br/> |<span data-ttu-id="f7a19-180">Многолинейная формула.</span><span class="sxs-lookup"><span data-stu-id="f7a19-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="f7a19-181">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f7a19-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

