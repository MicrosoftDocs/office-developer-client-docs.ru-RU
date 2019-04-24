---
title: Элемент Cell (строка строка rellineto) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: Содержит координаты x или y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.
ms.openlocfilehash: 63c9b2b87363ee798adc98eeeb780a30035a95e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339762"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="d48dd-103">Элемент Cell (строка строка rellineto) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d48dd-103">Cell element (RelLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="d48dd-104">Содержит координаты x или y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d48dd-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d48dd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d48dd-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d48dd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d48dd-107">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="d48dd-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d48dd-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d48dd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d48dd-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d48dd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d48dd-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d48dd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d48dd-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d48dd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d48dd-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="d48dd-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d48dd-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d48dd-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d48dd-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d48dd-114">Elements and attributes</span></span>

<span data-ttu-id="d48dd-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d48dd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d48dd-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d48dd-116">Parent elements</span></span>

|<span data-ttu-id="d48dd-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d48dd-117">**Element**</span></span>|<span data-ttu-id="d48dd-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d48dd-118">**Type**</span></span>|<span data-ttu-id="d48dd-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d48dd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d48dd-120">Элемент Row (геометрия)</span><span class="sxs-lookup"><span data-stu-id="d48dd-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d48dd-121">Реллинето_типе</span><span class="sxs-lookup"><span data-stu-id="d48dd-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d48dd-122">Содержит координаты x или y конечной вершины сегмента прямой линии относительно ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d48dd-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d48dd-123">Child elements</span></span>

|<span data-ttu-id="d48dd-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d48dd-124">**Element**</span></span>|<span data-ttu-id="d48dd-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d48dd-125">**Type**</span></span>|<span data-ttu-id="d48dd-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d48dd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d48dd-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="d48dd-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d48dd-128">Рефби_типе</span><span class="sxs-lookup"><span data-stu-id="d48dd-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d48dd-129">Указывает ссылку на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="d48dd-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d48dd-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d48dd-130">Attributes</span></span>

|<span data-ttu-id="d48dd-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d48dd-131">**Attribute**</span></span>|<span data-ttu-id="d48dd-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d48dd-132">**Type**</span></span>|<span data-ttu-id="d48dd-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d48dd-133">**Required**</span></span>|<span data-ttu-id="d48dd-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d48dd-134">**Description**</span></span>|<span data-ttu-id="d48dd-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d48dd-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d48dd-136">E</span><span class="sxs-lookup"><span data-stu-id="d48dd-136">E</span></span>  <br/> |<span data-ttu-id="d48dd-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d48dd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d48dd-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d48dd-138">optional</span></span>  <br/> |<span data-ttu-id="d48dd-139">Указывает, что формула возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d48dd-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="d48dd-140">Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="d48dd-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="d48dd-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d48dd-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="d48dd-142">F</span><span class="sxs-lookup"><span data-stu-id="d48dd-142">F</span></span>  <br/> |<span data-ttu-id="d48dd-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d48dd-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d48dd-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="d48dd-144">optional</span></span>  <br/> | <span data-ttu-id="d48dd-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="d48dd-145">Represents the element's formula.</span></span> <span data-ttu-id="d48dd-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="d48dd-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="d48dd-147">' (формула) ', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="d48dd-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="d48dd-148">`No Formula`Если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="d48dd-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="d48dd-149">`Inh`, если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="d48dd-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="d48dd-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="d48dd-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="d48dd-151">N</span><span class="sxs-lookup"><span data-stu-id="d48dd-151">N</span></span>  <br/> |<span data-ttu-id="d48dd-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d48dd-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d48dd-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d48dd-153">required</span></span>  <br/> |<span data-ttu-id="d48dd-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="d48dd-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="d48dd-156">Ознакомьтесь с разделом "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="d48dd-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="d48dd-157">U</span><span class="sxs-lookup"><span data-stu-id="d48dd-157">U</span></span>  <br/> |<span data-ttu-id="d48dd-158">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d48dd-158">xsd:string</span></span>  <br/> |<span data-ttu-id="d48dd-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="d48dd-159">optional</span></span>  <br/> |<span data-ttu-id="d48dd-160">Представляет единицу измерения. значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="d48dd-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="d48dd-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="d48dd-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="d48dd-162">V</span><span class="sxs-lookup"><span data-stu-id="d48dd-162">V</span></span>  <br/> |<span data-ttu-id="d48dd-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d48dd-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d48dd-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="d48dd-164">optional</span></span>  <br/> |<span data-ttu-id="d48dd-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="d48dd-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="d48dd-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d48dd-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d48dd-167">Remarks</span></span>

<span data-ttu-id="d48dd-168">Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="d48dd-169">Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d48dd-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="d48dd-170">**Value**</span><span class="sxs-lookup"><span data-stu-id="d48dd-170">**Value**</span></span>|<span data-ttu-id="d48dd-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d48dd-171">**Description**</span></span>|<span data-ttu-id="d48dd-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="d48dd-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d48dd-173">X</span><span class="sxs-lookup"><span data-stu-id="d48dd-173">X</span></span>  <br/> |<span data-ttu-id="d48dd-174">Координата x конечной вершины сегмента прямой линии относительно ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |[<span data-ttu-id="d48dd-175">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d48dd-175">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="d48dd-176">Да</span><span class="sxs-lookup"><span data-stu-id="d48dd-176">Y</span></span>  <br/> |<span data-ttu-id="d48dd-177">Координата y конечной вершины сегмента прямой линии относительно высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="d48dd-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |[<span data-ttu-id="d48dd-178">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d48dd-178">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
   

