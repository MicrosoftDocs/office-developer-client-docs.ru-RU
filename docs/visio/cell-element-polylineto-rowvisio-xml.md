---
title: Элемент Cell (PolyLineTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит x или y-координаты последней точки полилиновой или полилиновой формулы.
ms.openlocfilehash: b85784a41f4192895f17390f5473757c4bb09166
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539462"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="c5557-103">Элемент Cell (PolyLineTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5557-103">Cell element (PolyLineTo Row) (Visio XML)</span></span>

<span data-ttu-id="c5557-104">Содержит x или y-координаты последней точки полилиновой или полилиновой формулы.</span><span class="sxs-lookup"><span data-stu-id="c5557-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5557-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c5557-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5557-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c5557-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5557-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c5557-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5557-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c5557-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5557-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c5557-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5557-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5557-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5557-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c5557-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c5557-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c5557-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5557-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c5557-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5557-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5557-114">Elements and attributes</span></span>

<span data-ttu-id="c5557-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c5557-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5557-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c5557-116">Parent elements</span></span>

|<span data-ttu-id="c5557-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5557-117">**Element**</span></span>|<span data-ttu-id="c5557-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5557-118">**Type**</span></span>|<span data-ttu-id="c5557-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5557-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5557-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="c5557-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c5557-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="c5557-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5557-122">Содержит x или y-координаты последней точки полилиновой или полилиновой формулы.</span><span class="sxs-lookup"><span data-stu-id="c5557-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5557-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c5557-123">Child elements</span></span>

|<span data-ttu-id="c5557-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5557-124">**Element**</span></span>|<span data-ttu-id="c5557-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5557-125">**Type**</span></span>|<span data-ttu-id="c5557-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5557-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5557-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c5557-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c5557-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c5557-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5557-129">Указывает ссылку на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="c5557-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c5557-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5557-130">Attributes</span></span>

|<span data-ttu-id="c5557-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c5557-131">**Attribute**</span></span>|<span data-ttu-id="c5557-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5557-132">**Type**</span></span>|<span data-ttu-id="c5557-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c5557-133">**Required**</span></span>|<span data-ttu-id="c5557-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5557-134">**Description**</span></span>|<span data-ttu-id="c5557-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c5557-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5557-136">E</span><span class="sxs-lookup"><span data-stu-id="c5557-136">E</span></span>  <br/> |<span data-ttu-id="c5557-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5557-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c5557-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5557-138">optional</span></span>  <br/> |<span data-ttu-id="c5557-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="c5557-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c5557-140">Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="c5557-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c5557-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c5557-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c5557-142">F</span><span class="sxs-lookup"><span data-stu-id="c5557-142">F</span></span>  <br/> |<span data-ttu-id="c5557-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5557-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c5557-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5557-144">optional</span></span>  <br/> | <span data-ttu-id="c5557-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="c5557-145">Represents the element's formula.</span></span> <span data-ttu-id="c5557-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="c5557-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c5557-147">"(некоторые формулы)", если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="c5557-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c5557-148">`No Formula` если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="c5557-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c5557-149">`Inh` если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="c5557-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c5557-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="c5557-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="c5557-151">Нет</span><span class="sxs-lookup"><span data-stu-id="c5557-151">N</span></span>  <br/> |<span data-ttu-id="c5557-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5557-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c5557-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c5557-153">required</span></span>  <br/> |<span data-ttu-id="c5557-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c5557-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c5557-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c5557-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c5557-156">См. раздел Замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="c5557-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c5557-157">U</span><span class="sxs-lookup"><span data-stu-id="c5557-157">U</span></span>  <br/> |<span data-ttu-id="c5557-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5557-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c5557-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5557-159">optional</span></span>  <br/> |<span data-ttu-id="c5557-160">Представляет единицу измерения, по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="c5557-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c5557-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="c5557-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c5557-162">V</span><span class="sxs-lookup"><span data-stu-id="c5557-162">V</span></span>  <br/> |<span data-ttu-id="c5557-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5557-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c5557-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5557-164">optional</span></span>  <br/> |<span data-ttu-id="c5557-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="c5557-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c5557-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c5557-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5557-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5557-167">Remarks</span></span>

<span data-ttu-id="c5557-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c5557-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c5557-169">Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.**</span><span class="sxs-lookup"><span data-stu-id="c5557-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c5557-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c5557-170">**Value**</span></span>|<span data-ttu-id="c5557-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5557-171">**Description**</span></span>|<span data-ttu-id="c5557-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="c5557-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5557-173">X</span><span class="sxs-lookup"><span data-stu-id="c5557-173">X</span></span>  <br/> |<span data-ttu-id="c5557-174">X-координата конечной вершины полилина.</span><span class="sxs-lookup"><span data-stu-id="c5557-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="c5557-175">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c5557-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="c5557-176">Да</span><span class="sxs-lookup"><span data-stu-id="c5557-176">Y</span></span>  <br/> |<span data-ttu-id="c5557-177">Y-координата конечной вершины полилиновой линии.</span><span class="sxs-lookup"><span data-stu-id="c5557-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="c5557-178">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c5557-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="c5557-179">A</span><span class="sxs-lookup"><span data-stu-id="c5557-179">A</span></span>  <br/> |<span data-ttu-id="c5557-180">Формула полилинов.</span><span class="sxs-lookup"><span data-stu-id="c5557-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="c5557-181">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c5557-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

