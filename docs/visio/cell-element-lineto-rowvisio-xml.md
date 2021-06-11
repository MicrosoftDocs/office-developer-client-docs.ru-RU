---
title: Элемент Cell (LineTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Содержит x-или y-координаты конечной вершины сегмента прямой линии.
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539511"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="20914-103">Элемент Cell (LineTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="20914-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="20914-104">Содержит x-или y-координаты конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="20914-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20914-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="20914-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20914-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="20914-106">**Element type**</span></span> <br/> |[<span data-ttu-id="20914-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="20914-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="20914-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="20914-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="20914-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="20914-109">**Schema file**</span></span> <br/> |<span data-ttu-id="20914-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="20914-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="20914-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="20914-111">**Document parts**</span></span> <br/> |<span data-ttu-id="20914-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="20914-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20914-113">Определение</span><span class="sxs-lookup"><span data-stu-id="20914-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20914-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="20914-114">Elements and attributes</span></span>

<span data-ttu-id="20914-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="20914-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="20914-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="20914-116">Parent elements</span></span>

|<span data-ttu-id="20914-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20914-117">**Element**</span></span>|<span data-ttu-id="20914-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="20914-118">**Type**</span></span>|<span data-ttu-id="20914-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20914-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20914-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="20914-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="20914-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="20914-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20914-122">Содержит x-или y-координаты конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="20914-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20914-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="20914-123">Child elements</span></span>

|<span data-ttu-id="20914-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="20914-124">**Element**</span></span>|<span data-ttu-id="20914-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="20914-125">**Type**</span></span>|<span data-ttu-id="20914-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20914-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20914-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="20914-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20914-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="20914-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20914-129">Указывает ссылку на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="20914-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="20914-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="20914-130">Attributes</span></span>

|<span data-ttu-id="20914-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="20914-131">**Attribute**</span></span>|<span data-ttu-id="20914-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="20914-132">**Type**</span></span>|<span data-ttu-id="20914-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="20914-133">**Required**</span></span>|<span data-ttu-id="20914-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20914-134">**Description**</span></span>|<span data-ttu-id="20914-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="20914-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20914-136">E</span><span class="sxs-lookup"><span data-stu-id="20914-136">E</span></span>  <br/> |<span data-ttu-id="20914-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20914-137">xsd:string</span></span>  <br/> |<span data-ttu-id="20914-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="20914-138">optional</span></span>  <br/> |<span data-ttu-id="20914-139">Указывает, что формула оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="20914-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="20914-140">Значение **E —** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="20914-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="20914-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="20914-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="20914-142">F</span><span class="sxs-lookup"><span data-stu-id="20914-142">F</span></span>  <br/> |<span data-ttu-id="20914-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20914-143">xsd:string</span></span>  <br/> |<span data-ttu-id="20914-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="20914-144">optional</span></span>  <br/> | <span data-ttu-id="20914-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="20914-145">Represents the element's formula.</span></span> <span data-ttu-id="20914-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="20914-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="20914-147">"(некоторые формулы)", если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="20914-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="20914-148">`No Formula` если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="20914-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="20914-149">`Inh` если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="20914-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="20914-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="20914-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="20914-151">Нет</span><span class="sxs-lookup"><span data-stu-id="20914-151">N</span></span>  <br/> |<span data-ttu-id="20914-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20914-152">xsd:string</span></span>  <br/> |<span data-ttu-id="20914-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="20914-153">required</span></span>  <br/> |<span data-ttu-id="20914-154">Представляет имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="20914-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="20914-155">Имя ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="20914-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="20914-156">См. раздел Замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="20914-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="20914-157">U</span><span class="sxs-lookup"><span data-stu-id="20914-157">U</span></span>  <br/> |<span data-ttu-id="20914-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20914-158">xsd:string</span></span>  <br/> |<span data-ttu-id="20914-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="20914-159">optional</span></span>  <br/> |<span data-ttu-id="20914-160">Представляет единицу измерения, по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="20914-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="20914-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="20914-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="20914-162">V</span><span class="sxs-lookup"><span data-stu-id="20914-162">V</span></span>  <br/> |<span data-ttu-id="20914-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20914-163">xsd:string</span></span>  <br/> |<span data-ttu-id="20914-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="20914-164">optional</span></span>  <br/> |<span data-ttu-id="20914-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="20914-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="20914-166">Значение ячейки ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="20914-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20914-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="20914-167">Remarks</span></span>

<span data-ttu-id="20914-168">Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="20914-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="20914-169">Обратитесь к приведенной ниже таблице, чтобы определить значения атрибута **N,** разрешенные для этого элемента **Cell.**</span><span class="sxs-lookup"><span data-stu-id="20914-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="20914-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="20914-170">**Value**</span></span>|<span data-ttu-id="20914-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20914-171">**Description**</span></span>|<span data-ttu-id="20914-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="20914-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20914-173">X</span><span class="sxs-lookup"><span data-stu-id="20914-173">X</span></span>  <br/> |<span data-ttu-id="20914-174">X-координата конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="20914-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="20914-175">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="20914-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="20914-176">Да</span><span class="sxs-lookup"><span data-stu-id="20914-176">Y</span></span>  <br/> |<span data-ttu-id="20914-177">Y-координата конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="20914-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="20914-178">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="20914-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

