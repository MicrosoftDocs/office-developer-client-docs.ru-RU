---
title: Элемент ячейки (строка ArcTo) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Содержит x координата по оси y и галстук дугу.
ms.openlocfilehash: a51cf775f787a34aa8f5de6f6cf90ffc230f3500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813320"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="369cf-103">Элемент ячейки (строка ArcTo) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="369cf-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="369cf-104">Содержит x координата по оси y и галстук дугу.</span><span class="sxs-lookup"><span data-stu-id="369cf-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="369cf-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="369cf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="369cf-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="369cf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="369cf-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="369cf-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="369cf-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="369cf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="369cf-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="369cf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="369cf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="369cf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="369cf-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="369cf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="369cf-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="369cf-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="369cf-113">Определение</span><span class="sxs-lookup"><span data-stu-id="369cf-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="369cf-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="369cf-114">Elements and attributes</span></span>

<span data-ttu-id="369cf-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="369cf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="369cf-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="369cf-116">Parent elements</span></span>

|<span data-ttu-id="369cf-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="369cf-117">**Element**</span></span>|<span data-ttu-id="369cf-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="369cf-118">**Type**</span></span>|<span data-ttu-id="369cf-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="369cf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="369cf-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="369cf-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="369cf-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="369cf-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="369cf-122">Содержит координаты x и y и галстук дугу.</span><span class="sxs-lookup"><span data-stu-id="369cf-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="369cf-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="369cf-123">Child elements</span></span>

|<span data-ttu-id="369cf-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="369cf-124">**Element**</span></span>|<span data-ttu-id="369cf-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="369cf-125">**Type**</span></span>|<span data-ttu-id="369cf-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="369cf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="369cf-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="369cf-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="369cf-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="369cf-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="369cf-129">Содержит x координата по оси y и галстук дугу.</span><span class="sxs-lookup"><span data-stu-id="369cf-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="369cf-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="369cf-130">Attributes</span></span>

|<span data-ttu-id="369cf-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="369cf-131">**Attribute**</span></span>|<span data-ttu-id="369cf-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="369cf-132">**Type**</span></span>|<span data-ttu-id="369cf-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="369cf-133">**Required**</span></span>|<span data-ttu-id="369cf-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="369cf-134">**Description**</span></span>|<span data-ttu-id="369cf-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="369cf-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="369cf-136">E</span><span class="sxs-lookup"><span data-stu-id="369cf-136">E</span></span>  <br/> |<span data-ttu-id="369cf-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="369cf-137">xsd:string</span></span>  <br/> |<span data-ttu-id="369cf-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="369cf-138">optional</span></span>  <br/> |<span data-ttu-id="369cf-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="369cf-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="369cf-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="369cf-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="369cf-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="369cf-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="369cf-142">F</span><span class="sxs-lookup"><span data-stu-id="369cf-142">F</span></span>  <br/> |<span data-ttu-id="369cf-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="369cf-143">xsd:string</span></span>  <br/> |<span data-ttu-id="369cf-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="369cf-144">optional</span></span>  <br/> | <span data-ttu-id="369cf-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="369cf-145">Represents the element's formula.</span></span> <span data-ttu-id="369cf-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="369cf-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="369cf-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="369cf-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="369cf-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="369cf-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="369cf-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="369cf-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="369cf-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="369cf-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="369cf-151">N</span><span class="sxs-lookup"><span data-stu-id="369cf-151">N</span></span>  <br/> |<span data-ttu-id="369cf-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="369cf-152">xsd:string</span></span>  <br/> |<span data-ttu-id="369cf-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="369cf-153">required</span></span>  <br/> |<span data-ttu-id="369cf-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="369cf-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="369cf-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="369cf-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="369cf-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="369cf-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="369cf-157">U</span><span class="sxs-lookup"><span data-stu-id="369cf-157">U</span></span>  <br/> |<span data-ttu-id="369cf-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="369cf-158">xsd:string</span></span>  <br/> |<span data-ttu-id="369cf-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="369cf-159">optional</span></span>  <br/> |<span data-ttu-id="369cf-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="369cf-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="369cf-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="369cf-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="369cf-162">V</span><span class="sxs-lookup"><span data-stu-id="369cf-162">V</span></span>  <br/> |<span data-ttu-id="369cf-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="369cf-163">xsd:string</span></span>  <br/> |<span data-ttu-id="369cf-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="369cf-164">optional</span></span>  <br/> |<span data-ttu-id="369cf-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="369cf-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="369cf-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="369cf-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="369cf-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="369cf-167">Remarks</span></span>

<span data-ttu-id="369cf-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="369cf-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="369cf-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="369cf-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="369cf-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="369cf-170">**Value**</span></span>|<span data-ttu-id="369cf-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="369cf-171">**Description**</span></span>|<span data-ttu-id="369cf-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="369cf-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="369cf-173">A</span><span class="sxs-lookup"><span data-stu-id="369cf-173">A</span></span>  <br/> |<span data-ttu-id="369cf-174">Расстояние от среднего дуги по центру его кабеля.</span><span class="sxs-lookup"><span data-stu-id="369cf-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="369cf-175">Строка ArcTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="369cf-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="369cf-176">X </span><span class="sxs-lookup"><span data-stu-id="369cf-176">X</span></span>  <br/> |<span data-ttu-id="369cf-177">X координата конца вершины дугу.</span><span class="sxs-lookup"><span data-stu-id="369cf-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="369cf-178">Строка ArcTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="369cf-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="369cf-179">Да</span><span class="sxs-lookup"><span data-stu-id="369cf-179">Y</span></span>  <br/> |<span data-ttu-id="369cf-180">Окончания вершина дуги по оси y.</span><span class="sxs-lookup"><span data-stu-id="369cf-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="369cf-181">Строка ArcTo (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="369cf-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

