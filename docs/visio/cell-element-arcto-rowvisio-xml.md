---
title: Элемент Cell (ArcTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Содержит координаты x, координаты y или лук круговой дуги.
ms.openlocfilehash: 6d744366cda7db0f3950ed0962c7ba5bd01b8e36
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538825"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="8c44d-103">Элемент Cell (ArcTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8c44d-103">Cell element (ArcTo Row) (Visio XML)</span></span>

<span data-ttu-id="8c44d-104">Содержит координаты x, координаты y или лук круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="8c44d-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c44d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8c44d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c44d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8c44d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8c44d-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8c44d-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8c44d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8c44d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8c44d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8c44d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8c44d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8c44d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8c44d-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="8c44d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8c44d-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="8c44d-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c44d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8c44d-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8c44d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c44d-114">Elements and attributes</span></span>

<span data-ttu-id="8c44d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8c44d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8c44d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8c44d-116">Parent elements</span></span>

|<span data-ttu-id="8c44d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8c44d-117">**Element**</span></span>|<span data-ttu-id="8c44d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8c44d-118">**Type**</span></span>|<span data-ttu-id="8c44d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c44d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c44d-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="8c44d-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8c44d-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="8c44d-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8c44d-122">Содержит x- и y-координаты и нос круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="8c44d-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c44d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8c44d-123">Child elements</span></span>

|<span data-ttu-id="8c44d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8c44d-124">**Element**</span></span>|<span data-ttu-id="8c44d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8c44d-125">**Type**</span></span>|<span data-ttu-id="8c44d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c44d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c44d-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="8c44d-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c44d-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="8c44d-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8c44d-129">Содержит координаты x, координаты y или лук круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="8c44d-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8c44d-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c44d-130">Attributes</span></span>

|<span data-ttu-id="8c44d-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8c44d-131">**Attribute**</span></span>|<span data-ttu-id="8c44d-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8c44d-132">**Type**</span></span>|<span data-ttu-id="8c44d-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8c44d-133">**Required**</span></span>|<span data-ttu-id="8c44d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c44d-134">**Description**</span></span>|<span data-ttu-id="8c44d-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8c44d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8c44d-136">E</span><span class="sxs-lookup"><span data-stu-id="8c44d-136">E</span></span>  <br/> |<span data-ttu-id="8c44d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8c44d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8c44d-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="8c44d-138">optional</span></span>  <br/> |<span data-ttu-id="8c44d-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="8c44d-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="8c44d-140">Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="8c44d-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="8c44d-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8c44d-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="8c44d-142">F</span><span class="sxs-lookup"><span data-stu-id="8c44d-142">F</span></span>  <br/> |<span data-ttu-id="8c44d-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8c44d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8c44d-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="8c44d-144">optional</span></span>  <br/> | <span data-ttu-id="8c44d-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="8c44d-145">Represents the element's formula.</span></span> <span data-ttu-id="8c44d-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="8c44d-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="8c44d-147">"(некоторые формулы)", если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="8c44d-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="8c44d-148">`No Formula` если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="8c44d-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="8c44d-149">`Inh` если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="8c44d-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="8c44d-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="8c44d-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="8c44d-151">Нет</span><span class="sxs-lookup"><span data-stu-id="8c44d-151">N</span></span>  <br/> |<span data-ttu-id="8c44d-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8c44d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8c44d-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8c44d-153">required</span></span>  <br/> |<span data-ttu-id="8c44d-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8c44d-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="8c44d-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8c44d-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="8c44d-156">См. раздел Замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="8c44d-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="8c44d-157">U</span><span class="sxs-lookup"><span data-stu-id="8c44d-157">U</span></span>  <br/> |<span data-ttu-id="8c44d-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8c44d-158">xsd:string</span></span>  <br/> |<span data-ttu-id="8c44d-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="8c44d-159">optional</span></span>  <br/> |<span data-ttu-id="8c44d-160">Представляет единицу измерения, по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="8c44d-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="8c44d-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="8c44d-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="8c44d-162">V</span><span class="sxs-lookup"><span data-stu-id="8c44d-162">V</span></span>  <br/> |<span data-ttu-id="8c44d-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8c44d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8c44d-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="8c44d-164">optional</span></span>  <br/> |<span data-ttu-id="8c44d-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="8c44d-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="8c44d-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8c44d-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c44d-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c44d-167">Remarks</span></span>

<span data-ttu-id="8c44d-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8c44d-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="8c44d-169">Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.**</span><span class="sxs-lookup"><span data-stu-id="8c44d-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="8c44d-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8c44d-170">**Value**</span></span>|<span data-ttu-id="8c44d-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c44d-171">**Description**</span></span>|<span data-ttu-id="8c44d-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="8c44d-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c44d-173">A</span><span class="sxs-lookup"><span data-stu-id="8c44d-173">A</span></span>  <br/> |<span data-ttu-id="8c44d-174">Расстояние от середины дуги до середины аккорда.</span><span class="sxs-lookup"><span data-stu-id="8c44d-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="8c44d-175">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="8c44d-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="8c44d-176">X</span><span class="sxs-lookup"><span data-stu-id="8c44d-176">X</span></span>  <br/> |<span data-ttu-id="8c44d-177">X-координата конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="8c44d-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="8c44d-178">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="8c44d-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="8c44d-179">Да</span><span class="sxs-lookup"><span data-stu-id="8c44d-179">Y</span></span>  <br/> |<span data-ttu-id="8c44d-180">Y-координата конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="8c44d-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="8c44d-181">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="8c44d-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

