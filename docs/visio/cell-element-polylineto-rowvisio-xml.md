---
title: Элемент ячейки (строка PolyLineTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: Содержит x или y координаты точки ломаной или формулы ломаной.
ms.openlocfilehash: 485682b43db045893bfc968cfb0859cf8cb2ce2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813347"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="12b57-103">Элемент ячейки (строка PolyLineTo) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="12b57-103">Cell element (PolyLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="12b57-104">Содержит x или y координаты точки ломаной или формулы ломаной.</span><span class="sxs-lookup"><span data-stu-id="12b57-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12b57-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="12b57-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12b57-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="12b57-106">**Element type**</span></span> <br/> |[<span data-ttu-id="12b57-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="12b57-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="12b57-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="12b57-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="12b57-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="12b57-109">**Schema file**</span></span> <br/> |<span data-ttu-id="12b57-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="12b57-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="12b57-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="12b57-111">**Document parts**</span></span> <br/> |<span data-ttu-id="12b57-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="12b57-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="12b57-113">Определение</span><span class="sxs-lookup"><span data-stu-id="12b57-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="12b57-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="12b57-114">Elements and attributes</span></span>

<span data-ttu-id="12b57-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="12b57-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="12b57-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="12b57-116">Parent elements</span></span>

|<span data-ttu-id="12b57-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="12b57-117">**Element**</span></span>|<span data-ttu-id="12b57-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="12b57-118">**Type**</span></span>|<span data-ttu-id="12b57-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12b57-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="12b57-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="12b57-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="12b57-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="12b57-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="12b57-122">Содержит x или y координаты точки ломаной или формулы ломаной.</span><span class="sxs-lookup"><span data-stu-id="12b57-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="12b57-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="12b57-123">Child elements</span></span>

|<span data-ttu-id="12b57-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="12b57-124">**Element**</span></span>|<span data-ttu-id="12b57-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="12b57-125">**Type**</span></span>|<span data-ttu-id="12b57-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12b57-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="12b57-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="12b57-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="12b57-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="12b57-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="12b57-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="12b57-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="12b57-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12b57-130">Attributes</span></span>

|<span data-ttu-id="12b57-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="12b57-131">**Attribute**</span></span>|<span data-ttu-id="12b57-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="12b57-132">**Type**</span></span>|<span data-ttu-id="12b57-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="12b57-133">**Required**</span></span>|<span data-ttu-id="12b57-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12b57-134">**Description**</span></span>|<span data-ttu-id="12b57-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="12b57-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="12b57-136">E</span><span class="sxs-lookup"><span data-stu-id="12b57-136">E</span></span>  <br/> |<span data-ttu-id="12b57-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="12b57-137">xsd:string</span></span>  <br/> |<span data-ttu-id="12b57-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="12b57-138">optional</span></span>  <br/> |<span data-ttu-id="12b57-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="12b57-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="12b57-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="12b57-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="12b57-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="12b57-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="12b57-142">F</span><span class="sxs-lookup"><span data-stu-id="12b57-142">F</span></span>  <br/> |<span data-ttu-id="12b57-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="12b57-143">xsd:string</span></span>  <br/> |<span data-ttu-id="12b57-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="12b57-144">optional</span></span>  <br/> | <span data-ttu-id="12b57-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="12b57-145">Represents the element's formula.</span></span> <span data-ttu-id="12b57-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="12b57-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="12b57-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="12b57-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="12b57-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="12b57-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="12b57-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="12b57-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="12b57-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="12b57-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="12b57-151">N</span><span class="sxs-lookup"><span data-stu-id="12b57-151">N</span></span>  <br/> |<span data-ttu-id="12b57-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="12b57-152">xsd:string</span></span>  <br/> |<span data-ttu-id="12b57-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="12b57-153">required</span></span>  <br/> |<span data-ttu-id="12b57-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="12b57-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="12b57-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="12b57-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="12b57-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="12b57-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="12b57-157">U</span><span class="sxs-lookup"><span data-stu-id="12b57-157">U</span></span>  <br/> |<span data-ttu-id="12b57-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="12b57-158">xsd:string</span></span>  <br/> |<span data-ttu-id="12b57-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="12b57-159">optional</span></span>  <br/> |<span data-ttu-id="12b57-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="12b57-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="12b57-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="12b57-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="12b57-162">V</span><span class="sxs-lookup"><span data-stu-id="12b57-162">V</span></span>  <br/> |<span data-ttu-id="12b57-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="12b57-163">xsd:string</span></span>  <br/> |<span data-ttu-id="12b57-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="12b57-164">optional</span></span>  <br/> |<span data-ttu-id="12b57-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="12b57-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="12b57-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="12b57-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12b57-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="12b57-167">Remarks</span></span>

<span data-ttu-id="12b57-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="12b57-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="12b57-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="12b57-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="12b57-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="12b57-170">**Value**</span></span>|<span data-ttu-id="12b57-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12b57-171">**Description**</span></span>|<span data-ttu-id="12b57-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="12b57-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12b57-173">X </span><span class="sxs-lookup"><span data-stu-id="12b57-173">X</span></span>  <br/> |<span data-ttu-id="12b57-174">X координата конца вершины ломаной.</span><span class="sxs-lookup"><span data-stu-id="12b57-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="12b57-175">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="12b57-175">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="12b57-176">Да</span><span class="sxs-lookup"><span data-stu-id="12b57-176">Y</span></span>  <br/> |<span data-ttu-id="12b57-177">Конечный вершины ломаной по оси y.</span><span class="sxs-lookup"><span data-stu-id="12b57-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |[<span data-ttu-id="12b57-178">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="12b57-178">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="12b57-179">A</span><span class="sxs-lookup"><span data-stu-id="12b57-179">A</span></span>  <br/> |<span data-ttu-id="12b57-180">Формула ломаной.</span><span class="sxs-lookup"><span data-stu-id="12b57-180">The polyline formula.</span></span>  <br/> |[<span data-ttu-id="12b57-181">Строка PolylineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="12b57-181">PolylineTo Row (Geometry Section)</span></span>](polylineto-row-geometry-section.md) <br/> |
   

