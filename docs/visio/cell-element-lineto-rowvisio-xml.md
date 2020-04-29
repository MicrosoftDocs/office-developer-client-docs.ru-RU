---
title: Элемент Cell (строка LineTo) (XML в Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Содержит координаты x или y конечной вершины сегмента прямой линии.
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539511"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="0517f-103">Элемент Cell (строка LineTo) (XML в Visio)</span><span class="sxs-lookup"><span data-stu-id="0517f-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="0517f-104">Содержит координаты x или y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="0517f-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0517f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0517f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0517f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0517f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0517f-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0517f-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0517f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0517f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0517f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0517f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0517f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0517f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0517f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0517f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0517f-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="0517f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0517f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0517f-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0517f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0517f-114">Elements and attributes</span></span>

<span data-ttu-id="0517f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0517f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0517f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0517f-116">Parent elements</span></span>

|<span data-ttu-id="0517f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0517f-117">**Element**</span></span>|<span data-ttu-id="0517f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0517f-118">**Type**</span></span>|<span data-ttu-id="0517f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0517f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0517f-120">Элемент Row (геометрия)</span><span class="sxs-lookup"><span data-stu-id="0517f-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0517f-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="0517f-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0517f-122">Содержит координаты x или y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="0517f-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0517f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0517f-123">Child elements</span></span>

|<span data-ttu-id="0517f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0517f-124">**Element**</span></span>|<span data-ttu-id="0517f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0517f-125">**Type**</span></span>|<span data-ttu-id="0517f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0517f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0517f-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="0517f-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0517f-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0517f-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0517f-129">Указывает ссылку на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="0517f-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0517f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0517f-130">Attributes</span></span>

|<span data-ttu-id="0517f-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0517f-131">**Attribute**</span></span>|<span data-ttu-id="0517f-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0517f-132">**Type**</span></span>|<span data-ttu-id="0517f-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0517f-133">**Required**</span></span>|<span data-ttu-id="0517f-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0517f-134">**Description**</span></span>|<span data-ttu-id="0517f-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0517f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0517f-136">E</span><span class="sxs-lookup"><span data-stu-id="0517f-136">E</span></span>  <br/> |<span data-ttu-id="0517f-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0517f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0517f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0517f-138">optional</span></span>  <br/> |<span data-ttu-id="0517f-139">Указывает, что формула возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0517f-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="0517f-140">Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="0517f-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="0517f-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="0517f-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="0517f-142">F</span><span class="sxs-lookup"><span data-stu-id="0517f-142">F</span></span>  <br/> |<span data-ttu-id="0517f-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0517f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0517f-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="0517f-144">optional</span></span>  <br/> | <span data-ttu-id="0517f-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="0517f-145">Represents the element's formula.</span></span> <span data-ttu-id="0517f-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="0517f-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="0517f-147">' (формула) ', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="0517f-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="0517f-148">`No Formula`Если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="0517f-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="0517f-149">`Inh`, если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="0517f-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="0517f-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="0517f-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="0517f-151">N</span><span class="sxs-lookup"><span data-stu-id="0517f-151">N</span></span>  <br/> |<span data-ttu-id="0517f-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0517f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0517f-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0517f-153">required</span></span>  <br/> |<span data-ttu-id="0517f-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="0517f-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="0517f-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="0517f-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="0517f-156">Ознакомьтесь с разделом "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="0517f-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="0517f-157">U</span><span class="sxs-lookup"><span data-stu-id="0517f-157">U</span></span>  <br/> |<span data-ttu-id="0517f-158">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0517f-158">xsd:string</span></span>  <br/> |<span data-ttu-id="0517f-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="0517f-159">optional</span></span>  <br/> |<span data-ttu-id="0517f-160">Представляет единицу измерения. значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="0517f-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="0517f-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="0517f-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="0517f-162">V</span><span class="sxs-lookup"><span data-stu-id="0517f-162">V</span></span>  <br/> |<span data-ttu-id="0517f-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0517f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0517f-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="0517f-164">optional</span></span>  <br/> |<span data-ttu-id="0517f-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="0517f-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="0517f-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="0517f-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0517f-167">Примечания</span><span class="sxs-lookup"><span data-stu-id="0517f-167">Remarks</span></span>

<span data-ttu-id="0517f-168">Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="0517f-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="0517f-169">Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0517f-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="0517f-170">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0517f-170">**Value**</span></span>|<span data-ttu-id="0517f-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0517f-171">**Description**</span></span>|<span data-ttu-id="0517f-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="0517f-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0517f-173">X</span><span class="sxs-lookup"><span data-stu-id="0517f-173">X</span></span>  <br/> |<span data-ttu-id="0517f-174">Координата x конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="0517f-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="0517f-175">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="0517f-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="0517f-176">Да</span><span class="sxs-lookup"><span data-stu-id="0517f-176">Y</span></span>  <br/> |<span data-ttu-id="0517f-177">Координата y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="0517f-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="0517f-178">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="0517f-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

