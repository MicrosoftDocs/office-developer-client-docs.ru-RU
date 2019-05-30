---
title: Элемент Cell (строка для Microsoft LineTo) (XML в Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит координаты x или y последней точки ломаной линии или формулы ломаной линии.
ms.openlocfilehash: b85784a41f4192895f17390f5473757c4bb09166
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539462"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="c4524-103">Элемент Cell (строка для Microsoft LineTo) (XML в Visio)</span><span class="sxs-lookup"><span data-stu-id="c4524-103">Cell element (PolyLineTo Row) (Visio XML)</span></span>

<span data-ttu-id="c4524-104">Содержит координаты x или y последней точки ломаной линии или формулы ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c4524-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4524-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c4524-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4524-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c4524-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c4524-107">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="c4524-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c4524-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c4524-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c4524-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c4524-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c4524-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c4524-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c4524-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c4524-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c4524-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="c4524-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4524-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c4524-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c4524-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c4524-114">Elements and attributes</span></span>

<span data-ttu-id="c4524-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c4524-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c4524-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c4524-116">Parent elements</span></span>

|<span data-ttu-id="c4524-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c4524-117">**Element**</span></span>|<span data-ttu-id="c4524-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c4524-118">**Type**</span></span>|<span data-ttu-id="c4524-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4524-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4524-120">Элемент Row (геометрия)</span><span class="sxs-lookup"><span data-stu-id="c4524-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c4524-121">Полилинето_типе</span><span class="sxs-lookup"><span data-stu-id="c4524-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c4524-122">Содержит координаты x или y последней точки ломаной линии или формулы ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c4524-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4524-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c4524-123">Child elements</span></span>

|<span data-ttu-id="c4524-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c4524-124">**Element**</span></span>|<span data-ttu-id="c4524-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c4524-125">**Type**</span></span>|<span data-ttu-id="c4524-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4524-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4524-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c4524-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c4524-128">Рефби_типе</span><span class="sxs-lookup"><span data-stu-id="c4524-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c4524-129">Указывает ссылку на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="c4524-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c4524-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c4524-130">Attributes</span></span>

|<span data-ttu-id="c4524-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c4524-131">**Attribute**</span></span>|<span data-ttu-id="c4524-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c4524-132">**Type**</span></span>|<span data-ttu-id="c4524-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c4524-133">**Required**</span></span>|<span data-ttu-id="c4524-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4524-134">**Description**</span></span>|<span data-ttu-id="c4524-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c4524-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4524-136">E</span><span class="sxs-lookup"><span data-stu-id="c4524-136">E</span></span>  <br/> |<span data-ttu-id="c4524-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c4524-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c4524-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c4524-138">optional</span></span>  <br/> |<span data-ttu-id="c4524-139">Указывает, что формула возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c4524-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c4524-140">Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="c4524-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c4524-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c4524-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c4524-142">F</span><span class="sxs-lookup"><span data-stu-id="c4524-142">F</span></span>  <br/> |<span data-ttu-id="c4524-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c4524-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c4524-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="c4524-144">optional</span></span>  <br/> | <span data-ttu-id="c4524-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="c4524-145">Represents the element's formula.</span></span> <span data-ttu-id="c4524-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="c4524-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c4524-147">' (формула) ', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="c4524-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c4524-148">`No Formula`Если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="c4524-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c4524-149">`Inh`, если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="c4524-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c4524-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="c4524-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="c4524-151">N</span><span class="sxs-lookup"><span data-stu-id="c4524-151">N</span></span>  <br/> |<span data-ttu-id="c4524-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c4524-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c4524-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4524-153">required</span></span>  <br/> |<span data-ttu-id="c4524-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c4524-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c4524-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c4524-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c4524-156">Ознакомьтесь с разделом "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="c4524-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c4524-157">U</span><span class="sxs-lookup"><span data-stu-id="c4524-157">U</span></span>  <br/> |<span data-ttu-id="c4524-158">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c4524-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c4524-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="c4524-159">optional</span></span>  <br/> |<span data-ttu-id="c4524-160">Представляет единицу измерения. значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="c4524-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c4524-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="c4524-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c4524-162">V</span><span class="sxs-lookup"><span data-stu-id="c4524-162">V</span></span>  <br/> |<span data-ttu-id="c4524-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c4524-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c4524-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="c4524-164">optional</span></span>  <br/> |<span data-ttu-id="c4524-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="c4524-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c4524-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c4524-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4524-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4524-167">Remarks</span></span>

<span data-ttu-id="c4524-168">Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c4524-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c4524-169">Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c4524-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c4524-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c4524-170">**Value**</span></span>|<span data-ttu-id="c4524-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4524-171">**Description**</span></span>|<span data-ttu-id="c4524-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="c4524-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4524-173">X</span><span class="sxs-lookup"><span data-stu-id="c4524-173">X</span></span>  <br/> |<span data-ttu-id="c4524-174">Координата x конечной вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c4524-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="c4524-175">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c4524-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="c4524-176">Да</span><span class="sxs-lookup"><span data-stu-id="c4524-176">Y</span></span>  <br/> |<span data-ttu-id="c4524-177">Координата y конечной вершины ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c4524-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="c4524-178">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c4524-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="c4524-179">A</span><span class="sxs-lookup"><span data-stu-id="c4524-179">A</span></span>  <br/> |<span data-ttu-id="c4524-180">Формула ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="c4524-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="c4524-181">PolylineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c4524-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

