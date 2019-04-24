---
title: Элемент Cell (строка LineTo) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: Содержит координаты x или y конечной вершины сегмента прямой линии.
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318205"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="21e7b-103">Элемент Cell (строка LineTo) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="21e7b-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="21e7b-104">Содержит координаты x или y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="21e7b-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21e7b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="21e7b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21e7b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="21e7b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="21e7b-107">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="21e7b-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="21e7b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="21e7b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="21e7b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="21e7b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="21e7b-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="21e7b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="21e7b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="21e7b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="21e7b-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="21e7b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21e7b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="21e7b-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="21e7b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="21e7b-114">Elements and attributes</span></span>

<span data-ttu-id="21e7b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="21e7b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="21e7b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="21e7b-116">Parent elements</span></span>

|<span data-ttu-id="21e7b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="21e7b-117">**Element**</span></span>|<span data-ttu-id="21e7b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="21e7b-118">**Type**</span></span>|<span data-ttu-id="21e7b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21e7b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21e7b-120">Элемент Row (геометрия)</span><span class="sxs-lookup"><span data-stu-id="21e7b-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="21e7b-121">Линето_типе</span><span class="sxs-lookup"><span data-stu-id="21e7b-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21e7b-122">Содержит координаты x или y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="21e7b-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21e7b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="21e7b-123">Child elements</span></span>

|<span data-ttu-id="21e7b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="21e7b-124">**Element**</span></span>|<span data-ttu-id="21e7b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="21e7b-125">**Type**</span></span>|<span data-ttu-id="21e7b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21e7b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21e7b-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="21e7b-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21e7b-128">Рефби_типе</span><span class="sxs-lookup"><span data-stu-id="21e7b-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21e7b-129">Указывает ссылку на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="21e7b-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="21e7b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="21e7b-130">Attributes</span></span>

|<span data-ttu-id="21e7b-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="21e7b-131">**Attribute**</span></span>|<span data-ttu-id="21e7b-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="21e7b-132">**Type**</span></span>|<span data-ttu-id="21e7b-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="21e7b-133">**Required**</span></span>|<span data-ttu-id="21e7b-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21e7b-134">**Description**</span></span>|<span data-ttu-id="21e7b-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="21e7b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="21e7b-136">E</span><span class="sxs-lookup"><span data-stu-id="21e7b-136">E</span></span>  <br/> |<span data-ttu-id="21e7b-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="21e7b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="21e7b-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="21e7b-138">optional</span></span>  <br/> |<span data-ttu-id="21e7b-139">Указывает, что формула возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="21e7b-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="21e7b-140">Значение **E** — это текущее значение (строка сообщения об ошибке); значение атрибута **V** — это Последнее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="21e7b-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="21e7b-141">Строка сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="21e7b-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="21e7b-142">F</span><span class="sxs-lookup"><span data-stu-id="21e7b-142">F</span></span>  <br/> |<span data-ttu-id="21e7b-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="21e7b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="21e7b-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="21e7b-144">optional</span></span>  <br/> | <span data-ttu-id="21e7b-145">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="21e7b-145">Represents the element's formula.</span></span> <span data-ttu-id="21e7b-146">Этот атрибут может содержать одну из следующих строк:</span><span class="sxs-lookup"><span data-stu-id="21e7b-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="21e7b-147">' (формула) ', если формула существует локально</span><span class="sxs-lookup"><span data-stu-id="21e7b-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="21e7b-148">`No Formula`Если формула локально удалена или заблокирована</span><span class="sxs-lookup"><span data-stu-id="21e7b-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="21e7b-149">`Inh`, если формула наследуется.</span><span class="sxs-lookup"><span data-stu-id="21e7b-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="21e7b-150">Формула.</span><span class="sxs-lookup"><span data-stu-id="21e7b-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="21e7b-151">N</span><span class="sxs-lookup"><span data-stu-id="21e7b-151">N</span></span>  <br/> |<span data-ttu-id="21e7b-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="21e7b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="21e7b-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="21e7b-153">required</span></span>  <br/> |<span data-ttu-id="21e7b-154">Представляет имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="21e7b-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="21e7b-155">Имя ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="21e7b-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="21e7b-156">Ознакомьтесь с разделом "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="21e7b-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="21e7b-157">U</span><span class="sxs-lookup"><span data-stu-id="21e7b-157">U</span></span>  <br/> |<span data-ttu-id="21e7b-158">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="21e7b-158">xsd:string</span></span>  <br/> |<span data-ttu-id="21e7b-159">необязательный</span><span class="sxs-lookup"><span data-stu-id="21e7b-159">optional</span></span>  <br/> |<span data-ttu-id="21e7b-160">Представляет единицу измерения. значение по умолчанию — DL.</span><span class="sxs-lookup"><span data-stu-id="21e7b-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="21e7b-161">Единицы ячейки.</span><span class="sxs-lookup"><span data-stu-id="21e7b-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="21e7b-162">V</span><span class="sxs-lookup"><span data-stu-id="21e7b-162">V</span></span>  <br/> |<span data-ttu-id="21e7b-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="21e7b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="21e7b-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="21e7b-164">optional</span></span>  <br/> |<span data-ttu-id="21e7b-165">Представляет значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="21e7b-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="21e7b-166">Значение ячейки таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="21e7b-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21e7b-167">Замечания</span><span class="sxs-lookup"><span data-stu-id="21e7b-167">Remarks</span></span>

<span data-ttu-id="21e7b-168">Атрибут **N** этого элемента **Cell** должен иметь ограниченный набор значений, соответствующих ячейкам таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="21e7b-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="21e7b-169">Чтобы определить значения атрибута **N** , которые разрешено использовать для этого элемента **ячейки** , обратитесь к приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="21e7b-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="21e7b-170">**Value**</span><span class="sxs-lookup"><span data-stu-id="21e7b-170">**Value**</span></span>|<span data-ttu-id="21e7b-171">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21e7b-171">**Description**</span></span>|<span data-ttu-id="21e7b-172">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="21e7b-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21e7b-173">X</span><span class="sxs-lookup"><span data-stu-id="21e7b-173">X</span></span>  <br/> |<span data-ttu-id="21e7b-174">Координата x конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="21e7b-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="21e7b-175">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="21e7b-175">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="21e7b-176">Да</span><span class="sxs-lookup"><span data-stu-id="21e7b-176">Y</span></span>  <br/> |<span data-ttu-id="21e7b-177">Координата y конечной вершины сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="21e7b-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |[<span data-ttu-id="21e7b-178">LineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="21e7b-178">LineTo Row (Geometry Section)</span></span>](lineto-row-geometry-section.md) <br/> |
   

