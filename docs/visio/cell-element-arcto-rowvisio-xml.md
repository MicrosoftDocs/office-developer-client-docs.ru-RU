---
title: Элемент Cell (строка ArcTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Содержит координату x, координату y или лук цикловой дуги.
ms.openlocfilehash: 6d744366cda7db0f3950ed0962c7ba5bd01b8e36
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538825"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="e9b0e-103">Элемент Cell (строка ArcTo) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e9b0e-103">Cell element (ArcTo Row) (Visio XML)</span></span>

<span data-ttu-id="e9b0e-104">Содержит координату x, координату Y или яс цикловой дуги.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9b0e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9b0e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9b0e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e9b0e-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e9b0e-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e9b0e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e9b0e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e9b0e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e9b0e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e9b0e-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e9b0e-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="e9b0e-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9b0e-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e9b0e-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e9b0e-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9b0e-114">Elements and attributes</span></span>

<span data-ttu-id="e9b0e-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e9b0e-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e9b0e-116">Parent elements</span></span>

|<span data-ttu-id="e9b0e-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-117">**Element**</span></span>|<span data-ttu-id="e9b0e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-118">**Type**</span></span>|<span data-ttu-id="e9b0e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9b0e-120">Элемент Row (Geometry)</span><span class="sxs-lookup"><span data-stu-id="e9b0e-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e9b0e-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="e9b0e-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9b0e-122">Содержит координаты x и y и лук цикловой дуги.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e9b0e-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e9b0e-123">Child elements</span></span>

|<span data-ttu-id="e9b0e-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-124">**Element**</span></span>|<span data-ttu-id="e9b0e-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-125">**Type**</span></span>|<span data-ttu-id="e9b0e-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9b0e-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e9b0e-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9b0e-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e9b0e-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9b0e-129">Содержит координату x, координату y или лук цикловой дуги.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e9b0e-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9b0e-130">Attributes</span></span>

|<span data-ttu-id="e9b0e-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-131">**Attribute**</span></span>|<span data-ttu-id="e9b0e-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-132">**Type**</span></span>|<span data-ttu-id="e9b0e-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-133">**Required**</span></span>|<span data-ttu-id="e9b0e-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-134">**Description**</span></span>|<span data-ttu-id="e9b0e-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9b0e-136">E</span><span class="sxs-lookup"><span data-stu-id="e9b0e-136">E</span></span>  <br/> |<span data-ttu-id="e9b0e-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9b0e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e9b0e-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9b0e-138">optional</span></span>  <br/> |<span data-ttu-id="e9b0e-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e9b0e-140">Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e9b0e-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e9b0e-142">F</span><span class="sxs-lookup"><span data-stu-id="e9b0e-142">F</span></span>  <br/> |<span data-ttu-id="e9b0e-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9b0e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e9b0e-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9b0e-144">optional</span></span>  <br/> | <span data-ttu-id="e9b0e-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-145">Represents the element's formula.</span></span> <span data-ttu-id="e9b0e-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="e9b0e-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e9b0e-147">'(some formula)', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="e9b0e-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e9b0e-148">`No Formula` если формула удалена или заблокирована локально</span><span class="sxs-lookup"><span data-stu-id="e9b0e-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e9b0e-149">`Inh` если формула унаследована.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e9b0e-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e9b0e-151">N</span><span class="sxs-lookup"><span data-stu-id="e9b0e-151">N</span></span>  <br/> |<span data-ttu-id="e9b0e-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9b0e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e9b0e-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9b0e-153">required</span></span>  <br/> |<span data-ttu-id="e9b0e-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e9b0e-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e9b0e-156">См. раздел "Замечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e9b0e-157">U</span><span class="sxs-lookup"><span data-stu-id="e9b0e-157">U</span></span>  <br/> |<span data-ttu-id="e9b0e-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9b0e-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e9b0e-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9b0e-159">optional</span></span>  <br/> |<span data-ttu-id="e9b0e-160">Представляет единицу измерения, значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e9b0e-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e9b0e-162">V</span><span class="sxs-lookup"><span data-stu-id="e9b0e-162">V</span></span>  <br/> |<span data-ttu-id="e9b0e-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9b0e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e9b0e-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9b0e-164">optional</span></span>  <br/> |<span data-ttu-id="e9b0e-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e9b0e-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9b0e-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9b0e-167">Remarks</span></span>

<span data-ttu-id="e9b0e-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e9b0e-169">Чтобы определить значения атрибута **N,** допустимого для этого элемента Cell, обратитесь к таблице **ниже.**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e9b0e-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-170">**Value**</span></span>|<span data-ttu-id="e9b0e-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-171">**Description**</span></span>|<span data-ttu-id="e9b0e-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="e9b0e-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e9b0e-173">A</span><span class="sxs-lookup"><span data-stu-id="e9b0e-173">A</span></span>  <br/> |<span data-ttu-id="e9b0e-174">Расстояние от средней точки дуги до средней точки ее разоряемой.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="e9b0e-175">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e9b0e-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e9b0e-176">X</span><span class="sxs-lookup"><span data-stu-id="e9b0e-176">X</span></span>  <br/> |<span data-ttu-id="e9b0e-177">X-координата конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="e9b0e-178">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e9b0e-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e9b0e-179">Да</span><span class="sxs-lookup"><span data-stu-id="e9b0e-179">Y</span></span>  <br/> |<span data-ttu-id="e9b0e-180">Y-координата конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="e9b0e-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="e9b0e-181">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e9b0e-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

