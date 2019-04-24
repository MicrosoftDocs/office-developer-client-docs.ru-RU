---
title: Элемент Cell (строка строка ArcTo) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: Содержит координату x, координату по оси y или дугу круговой дуги.
ms.openlocfilehash: 709251c40299425d59df97fc0c48901bb0204167
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356136"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="043b2-103">Элемент Cell (строка строка ArcTo) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="043b2-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="043b2-104">Содержит координату x, координату по оси y или дугу круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="043b2-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="043b2-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="043b2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="043b2-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="043b2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="043b2-107">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="043b2-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="043b2-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="043b2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="043b2-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="043b2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="043b2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="043b2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="043b2-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="043b2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="043b2-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="043b2-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="043b2-113">Определение</span><span class="sxs-lookup"><span data-stu-id="043b2-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="043b2-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="043b2-114">Elements and attributes</span></span>

<span data-ttu-id="043b2-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="043b2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="043b2-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="043b2-116">Parent elements</span></span>

|<span data-ttu-id="043b2-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="043b2-117">**Element**</span></span>|<span data-ttu-id="043b2-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="043b2-118">**Type**</span></span>|<span data-ttu-id="043b2-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043b2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="043b2-120">Элемент Row (геометрия)</span><span class="sxs-lookup"><span data-stu-id="043b2-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="043b2-121">Аркто_типе</span><span class="sxs-lookup"><span data-stu-id="043b2-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="043b2-122">Содержит координаты x и y, а также арксинус круга.</span><span class="sxs-lookup"><span data-stu-id="043b2-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="043b2-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="043b2-123">Child elements</span></span>

|<span data-ttu-id="043b2-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="043b2-124">**Element**</span></span>|<span data-ttu-id="043b2-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="043b2-125">**Type**</span></span>|<span data-ttu-id="043b2-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043b2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="043b2-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="043b2-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="043b2-128">Рефби_типе</span><span class="sxs-lookup"><span data-stu-id="043b2-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="043b2-129">Содержит координату x, координату по оси y или дугу круговой дуги.</span><span class="sxs-lookup"><span data-stu-id="043b2-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="043b2-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="043b2-130">Attributes</span></span>

|<span data-ttu-id="043b2-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="043b2-131">**Attribute**</span></span>|<span data-ttu-id="043b2-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="043b2-132">**Type**</span></span>|<span data-ttu-id="043b2-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="043b2-133">**Required**</span></span>|<span data-ttu-id="043b2-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043b2-134">**Description**</span></span>|<span data-ttu-id="043b2-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="043b2-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="043b2-136">E</span><span class="sxs-lookup"><span data-stu-id="043b2-136">E</span></span>  <br/> |<span data-ttu-id="043b2-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="043b2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="043b2-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="043b2-138">optional</span></span>  <br/> |<span data-ttu-id="043b2-139">Указывает, что формула возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="043b2-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="043b2-140">Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="043b2-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="043b2-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="043b2-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="043b2-142">F</span><span class="sxs-lookup"><span data-stu-id="043b2-142">F</span></span>  <br/> |<span data-ttu-id="043b2-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="043b2-143">xsd:string</span></span>  <br/> |<span data-ttu-id="043b2-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="043b2-144">optional</span></span>  <br/> | <span data-ttu-id="043b2-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="043b2-145">Represents the element's formula.</span></span> <span data-ttu-id="043b2-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="043b2-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="043b2-147">' (формула) ', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="043b2-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="043b2-148">`No Formula`Если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="043b2-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="043b2-149">`Inh`, если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="043b2-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="043b2-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="043b2-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="043b2-151">N</span><span class="sxs-lookup"><span data-stu-id="043b2-151">N</span></span>  <br/> |<span data-ttu-id="043b2-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="043b2-152">xsd:string</span></span>  <br/> |<span data-ttu-id="043b2-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="043b2-153">required</span></span>  <br/> |<span data-ttu-id="043b2-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="043b2-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="043b2-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="043b2-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="043b2-156">Ознакомьтесь с разделом "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="043b2-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="043b2-157">U</span><span class="sxs-lookup"><span data-stu-id="043b2-157">U</span></span>  <br/> |<span data-ttu-id="043b2-158">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="043b2-158">xsd:string</span></span>  <br/> |<span data-ttu-id="043b2-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="043b2-159">optional</span></span>  <br/> |<span data-ttu-id="043b2-160">Представляет единицу измерения. значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="043b2-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="043b2-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="043b2-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="043b2-162">V</span><span class="sxs-lookup"><span data-stu-id="043b2-162">V</span></span>  <br/> |<span data-ttu-id="043b2-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="043b2-163">xsd:string</span></span>  <br/> |<span data-ttu-id="043b2-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="043b2-164">optional</span></span>  <br/> |<span data-ttu-id="043b2-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="043b2-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="043b2-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="043b2-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="043b2-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="043b2-167">Remarks</span></span>

<span data-ttu-id="043b2-168">Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="043b2-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="043b2-169">Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="043b2-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="043b2-170">**Value**</span><span class="sxs-lookup"><span data-stu-id="043b2-170">**Value**</span></span>|<span data-ttu-id="043b2-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043b2-171">**Description**</span></span>|<span data-ttu-id="043b2-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="043b2-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="043b2-173">А</span><span class="sxs-lookup"><span data-stu-id="043b2-173">A</span></span>  <br/> |<span data-ttu-id="043b2-174">Расстояние от средней дуги до средней точки аккорда.</span><span class="sxs-lookup"><span data-stu-id="043b2-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |[<span data-ttu-id="043b2-175">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="043b2-175">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="043b2-176">X</span><span class="sxs-lookup"><span data-stu-id="043b2-176">X</span></span>  <br/> |<span data-ttu-id="043b2-177">Координата x конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="043b2-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="043b2-178">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="043b2-178">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
|<span data-ttu-id="043b2-179">Да</span><span class="sxs-lookup"><span data-stu-id="043b2-179">Y</span></span>  <br/> |<span data-ttu-id="043b2-180">Координата y конечной вершины дуги.</span><span class="sxs-lookup"><span data-stu-id="043b2-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |[<span data-ttu-id="043b2-181">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="043b2-181">ArcTo Row (Geometry Section)</span></span>](arcto-row-geometry-section.md) <br/> |
   

