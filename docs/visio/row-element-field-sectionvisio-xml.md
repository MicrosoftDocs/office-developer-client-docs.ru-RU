---
title: Элемент Row (Field Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7883cb55-a7db-10c0-be20-5d3c561e490f
description: Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "Поле".
ms.openlocfilehash: c05f704610d7061b9e2c8b742adc39f2b72ba4ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541759"
---
# <a name="row-element-field-section-visio-xml"></a><span data-ttu-id="892ef-103">Элемент Row (Field Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="892ef-103">Row element (Field Section) (Visio XML)</span></span>

<span data-ttu-id="892ef-104">Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "Поле".</span><span class="sxs-lookup"><span data-stu-id="892ef-104">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="892ef-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="892ef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="892ef-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="892ef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="892ef-107">FieldRow_Type</span><span class="sxs-lookup"><span data-stu-id="892ef-107">FieldRow_Type</span></span>](fieldrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="892ef-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="892ef-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="892ef-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="892ef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="892ef-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="892ef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="892ef-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="892ef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="892ef-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="892ef-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="892ef-113">Определение</span><span class="sxs-lookup"><span data-stu-id="892ef-113">Definition</span></span>

```XML
< xs:element name="Row" type="FieldRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="892ef-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="892ef-114">Elements and attributes</span></span>

<span data-ttu-id="892ef-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="892ef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="892ef-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="892ef-116">Parent elements</span></span>

|<span data-ttu-id="892ef-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="892ef-117">**Element**</span></span>|<span data-ttu-id="892ef-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="892ef-118">**Type**</span></span>|<span data-ttu-id="892ef-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="892ef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="892ef-120">Section</span><span class="sxs-lookup"><span data-stu-id="892ef-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="892ef-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="892ef-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="892ef-122">Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "Поле".</span><span class="sxs-lookup"><span data-stu-id="892ef-122">Displays functions and formulas inserted in the shape's text by using the Field dialog box.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="892ef-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="892ef-123">Child elements</span></span>

|<span data-ttu-id="892ef-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="892ef-124">**Element**</span></span>|<span data-ttu-id="892ef-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="892ef-125">**Type**</span></span>|<span data-ttu-id="892ef-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="892ef-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="892ef-127">Cell</span><span class="sxs-lookup"><span data-stu-id="892ef-127">Cell</span></span>](cell-element-field-sectionvisio-xml.md) <br/> |[<span data-ttu-id="892ef-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="892ef-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="892ef-129">Отображает функции и формулы, вставленные в текст фигуры, с помощью диалогового окна "Поле"</span><span class="sxs-lookup"><span data-stu-id="892ef-129">Displays functions and formulas inserted in the shape's text by using the Field dialog box</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="892ef-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="892ef-130">Attributes</span></span>

|<span data-ttu-id="892ef-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="892ef-131">**Attribute**</span></span>|<span data-ttu-id="892ef-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="892ef-132">**Type**</span></span>|<span data-ttu-id="892ef-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="892ef-133">**Required**</span></span>|<span data-ttu-id="892ef-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="892ef-134">**Description**</span></span>|<span data-ttu-id="892ef-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="892ef-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="892ef-136">Del</span><span class="sxs-lookup"><span data-stu-id="892ef-136">Del</span></span>  <br/> |<span data-ttu-id="892ef-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="892ef-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="892ef-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="892ef-138">optional</span></span>  <br/> |<span data-ttu-id="892ef-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="892ef-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="892ef-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="892ef-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="892ef-141">IX</span><span class="sxs-lookup"><span data-stu-id="892ef-141">IX</span></span>  <br/> |<span data-ttu-id="892ef-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="892ef-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="892ef-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="892ef-143">optional</span></span>  <br/> |<span data-ttu-id="892ef-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="892ef-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="892ef-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="892ef-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="892ef-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="892ef-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="892ef-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="892ef-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="892ef-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="892ef-148">LocalName</span></span>  <br/> |<span data-ttu-id="892ef-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="892ef-149">xsd:string</span></span>  <br/> |<span data-ttu-id="892ef-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="892ef-150">optional</span></span>  <br/> |<span data-ttu-id="892ef-151">Указывает уникальное имя строки, зависимое от языка.</span><span class="sxs-lookup"><span data-stu-id="892ef-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="892ef-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="892ef-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="892ef-153">N</span><span class="sxs-lookup"><span data-stu-id="892ef-153">N</span></span>  <br/> |<span data-ttu-id="892ef-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="892ef-154">xsd:string</span></span>  <br/> |<span data-ttu-id="892ef-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="892ef-155">optional</span></span>  <br/> |<span data-ttu-id="892ef-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="892ef-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="892ef-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="892ef-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="892ef-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="892ef-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="892ef-159">T</span><span class="sxs-lookup"><span data-stu-id="892ef-159">T</span></span>  <br/> |<span data-ttu-id="892ef-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="892ef-160">xsd:string</span></span>  <br/> |<span data-ttu-id="892ef-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="892ef-161">optional</span></span>  <br/> |<span data-ttu-id="892ef-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="892ef-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="892ef-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="892ef-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="892ef-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="892ef-164">Values of the xsd:string type.</span></span>  <br/> |
   

