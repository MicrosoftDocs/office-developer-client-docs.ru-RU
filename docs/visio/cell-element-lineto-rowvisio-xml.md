---
title: Элемент ячейки (LineTo строка) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Содержит x- или y координаты окончания вершины прямой сегмент.
ms.openlocfilehash: 284b315c156fed8ea3592d2c6825ff6b4bf4c279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813337"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="e71a5-103">Элемент ячейки (LineTo строка) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e71a5-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="e71a5-104">Содержит x- или y координаты окончания вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="e71a5-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e71a5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e71a5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e71a5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e71a5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e71a5-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e71a5-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e71a5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e71a5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e71a5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e71a5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e71a5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e71a5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e71a5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e71a5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e71a5-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="e71a5-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e71a5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e71a5-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e71a5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e71a5-114">Elements and attributes</span></span>

<span data-ttu-id="e71a5-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="e71a5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e71a5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e71a5-116">Parent elements</span></span>

|<span data-ttu-id="e71a5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e71a5-117">**Element**</span></span>|<span data-ttu-id="e71a5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e71a5-118">**Type**</span></span>|<span data-ttu-id="e71a5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e71a5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e71a5-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="e71a5-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e71a5-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="e71a5-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e71a5-122">Содержит x- или y координаты окончания вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="e71a5-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e71a5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e71a5-123">Child elements</span></span>

|<span data-ttu-id="e71a5-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e71a5-124">**Element**</span></span>|<span data-ttu-id="e71a5-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e71a5-125">**Type**</span></span>|<span data-ttu-id="e71a5-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e71a5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e71a5-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e71a5-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e71a5-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e71a5-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e71a5-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="e71a5-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e71a5-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e71a5-130">Attributes</span></span>

|<span data-ttu-id="e71a5-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e71a5-131">**Attribute**</span></span>|<span data-ttu-id="e71a5-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e71a5-132">**Type**</span></span>|<span data-ttu-id="e71a5-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="e71a5-133">**Required**</span></span>|<span data-ttu-id="e71a5-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e71a5-134">**Description**</span></span>|<span data-ttu-id="e71a5-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e71a5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e71a5-136">E</span><span class="sxs-lookup"><span data-stu-id="e71a5-136">E</span></span>  <br/> |<span data-ttu-id="e71a5-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e71a5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e71a5-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e71a5-138">optional</span></span>  <br/> |<span data-ttu-id="e71a5-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="e71a5-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e71a5-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="e71a5-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e71a5-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e71a5-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e71a5-142">F</span><span class="sxs-lookup"><span data-stu-id="e71a5-142">F</span></span>  <br/> |<span data-ttu-id="e71a5-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e71a5-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e71a5-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="e71a5-144">optional</span></span>  <br/> | <span data-ttu-id="e71a5-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="e71a5-145">Represents the element's formula.</span></span> <span data-ttu-id="e71a5-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="e71a5-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e71a5-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="e71a5-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e71a5-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="e71a5-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e71a5-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="e71a5-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e71a5-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="e71a5-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e71a5-151">N</span><span class="sxs-lookup"><span data-stu-id="e71a5-151">N</span></span>  <br/> |<span data-ttu-id="e71a5-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e71a5-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e71a5-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e71a5-153">required</span></span>  <br/> |<span data-ttu-id="e71a5-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="e71a5-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e71a5-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="e71a5-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e71a5-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="e71a5-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e71a5-157">U</span><span class="sxs-lookup"><span data-stu-id="e71a5-157">U</span></span>  <br/> |<span data-ttu-id="e71a5-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e71a5-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e71a5-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="e71a5-159">optional</span></span>  <br/> |<span data-ttu-id="e71a5-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="e71a5-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e71a5-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="e71a5-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e71a5-162">V</span><span class="sxs-lookup"><span data-stu-id="e71a5-162">V</span></span>  <br/> |<span data-ttu-id="e71a5-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e71a5-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e71a5-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="e71a5-164">optional</span></span>  <br/> |<span data-ttu-id="e71a5-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="e71a5-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e71a5-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="e71a5-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e71a5-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="e71a5-167">Remarks</span></span>

<span data-ttu-id="e71a5-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="e71a5-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e71a5-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="e71a5-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e71a5-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e71a5-170">**Value**</span></span>|<span data-ttu-id="e71a5-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e71a5-171">**Description**</span></span>|<span data-ttu-id="e71a5-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="e71a5-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e71a5-173">X </span><span class="sxs-lookup"><span data-stu-id="e71a5-173">X</span></span>  <br/> |<span data-ttu-id="e71a5-174">X координата конца вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="e71a5-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="e71a5-175">Строка LineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="e71a5-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="e71a5-176">Да</span><span class="sxs-lookup"><span data-stu-id="e71a5-176">Y</span></span>  <br/> |<span data-ttu-id="e71a5-177">Координата конца вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="e71a5-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="e71a5-178">Строка LineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="e71a5-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

