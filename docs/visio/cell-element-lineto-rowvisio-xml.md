---
title: Элемент ячейки (LineTo строка) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Содержит x- или y координаты окончания вершины прямой сегмент.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386595"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="d98df-103">Элемент ячейки (LineTo строка) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d98df-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="d98df-104">Содержит x- или y координаты окончания вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="d98df-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d98df-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d98df-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d98df-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d98df-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d98df-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d98df-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d98df-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d98df-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d98df-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d98df-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d98df-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d98df-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d98df-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d98df-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d98df-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="d98df-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d98df-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d98df-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d98df-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d98df-114">Elements and attributes</span></span>

<span data-ttu-id="d98df-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d98df-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d98df-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d98df-116">Parent elements</span></span>

|<span data-ttu-id="d98df-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d98df-117">**Element**</span></span>|<span data-ttu-id="d98df-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d98df-118">**Type**</span></span>|<span data-ttu-id="d98df-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d98df-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d98df-120">Элемент Row (Геометрия)</span><span class="sxs-lookup"><span data-stu-id="d98df-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d98df-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="d98df-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d98df-122">Содержит x- или y координаты окончания вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="d98df-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d98df-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d98df-123">Child elements</span></span>

|<span data-ttu-id="d98df-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d98df-124">**Element**</span></span>|<span data-ttu-id="d98df-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d98df-125">**Type**</span></span>|<span data-ttu-id="d98df-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d98df-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d98df-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="d98df-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d98df-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="d98df-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d98df-129">Задает ссылку на странице документа.</span><span class="sxs-lookup"><span data-stu-id="d98df-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d98df-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d98df-130">Attributes</span></span>

|<span data-ttu-id="d98df-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d98df-131">**Attribute**</span></span>|<span data-ttu-id="d98df-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d98df-132">**Type**</span></span>|<span data-ttu-id="d98df-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d98df-133">**Required**</span></span>|<span data-ttu-id="d98df-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d98df-134">**Description**</span></span>|<span data-ttu-id="d98df-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d98df-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d98df-136">E</span><span class="sxs-lookup"><span data-stu-id="d98df-136">E</span></span>  <br/> |<span data-ttu-id="d98df-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d98df-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d98df-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d98df-138">optional</span></span>  <br/> |<span data-ttu-id="d98df-139">Указывает, что формулы оценивается как ошибка.</span><span class="sxs-lookup"><span data-stu-id="d98df-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="d98df-140">Значение **E** является текущим значением (строка сообщения об ошибке); значение атрибута **V** — это последний допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="d98df-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="d98df-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d98df-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="d98df-142">F</span><span class="sxs-lookup"><span data-stu-id="d98df-142">F</span></span>  <br/> |<span data-ttu-id="d98df-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d98df-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d98df-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="d98df-144">optional</span></span>  <br/> | <span data-ttu-id="d98df-145">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="d98df-145">Represents the element's formula.</span></span> <span data-ttu-id="d98df-146">Этот атрибут может содержать один из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="d98df-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="d98df-147">(Некоторые формулы) Если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="d98df-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="d98df-148">`No Formula`Если формула локально удален или заблокирован</span><span class="sxs-lookup"><span data-stu-id="d98df-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="d98df-149">`Inh`Если наследуется формулу.</span><span class="sxs-lookup"><span data-stu-id="d98df-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="d98df-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="d98df-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="d98df-151">N</span><span class="sxs-lookup"><span data-stu-id="d98df-151">N</span></span>  <br/> |<span data-ttu-id="d98df-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d98df-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d98df-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d98df-153">required</span></span>  <br/> |<span data-ttu-id="d98df-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d98df-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="d98df-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d98df-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="d98df-156">В разделе замечания ниже.</span><span class="sxs-lookup"><span data-stu-id="d98df-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="d98df-157">U</span><span class="sxs-lookup"><span data-stu-id="d98df-157">U</span></span>  <br/> |<span data-ttu-id="d98df-158">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d98df-158">xsd:string</span></span>  <br/> |<span data-ttu-id="d98df-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="d98df-159">optional</span></span>  <br/> |<span data-ttu-id="d98df-160">Представляет единицы измерения по умолчанию — это список Рассылки.</span><span class="sxs-lookup"><span data-stu-id="d98df-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="d98df-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="d98df-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="d98df-162">V</span><span class="sxs-lookup"><span data-stu-id="d98df-162">V</span></span>  <br/> |<span data-ttu-id="d98df-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d98df-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d98df-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="d98df-164">optional</span></span>  <br/> |<span data-ttu-id="d98df-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="d98df-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="d98df-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d98df-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d98df-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="d98df-167">Remarks</span></span>

<span data-ttu-id="d98df-168">Атрибут **N** этого элемента **ячейки** должен быть один из ограниченный набор значений, которые соответствуют ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="d98df-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="d98df-169">Обратитесь к таблице ниже для определения значений атрибутов **N** , разрешенных для этого элемента **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="d98df-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="d98df-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d98df-170">**Value**</span></span>|<span data-ttu-id="d98df-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d98df-171">**Description**</span></span>|<span data-ttu-id="d98df-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="d98df-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d98df-173">X </span><span class="sxs-lookup"><span data-stu-id="d98df-173">X</span></span>  <br/> |<span data-ttu-id="d98df-174">X координата конца вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="d98df-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="d98df-175">Строка LineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="d98df-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="d98df-176">Да</span><span class="sxs-lookup"><span data-stu-id="d98df-176">Y</span></span>  <br/> |<span data-ttu-id="d98df-177">Координата конца вершины прямой сегмент.</span><span class="sxs-lookup"><span data-stu-id="d98df-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="d98df-178">Строка LineTo (раздел "Геометрия")</span><span class="sxs-lookup"><span data-stu-id="d98df-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

