---
title: Элемент Row (Controls Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Содержит ячейки для определенного работки элементов управления, определенных для фигуры.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541745"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="ca3db-103">Элемент Row (Controls Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ca3db-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="ca3db-104">Содержит ячейки для определенного работки элементов управления, определенных для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca3db-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca3db-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ca3db-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca3db-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ca3db-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ca3db-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="ca3db-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ca3db-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ca3db-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ca3db-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ca3db-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ca3db-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ca3db-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ca3db-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ca3db-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ca3db-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="ca3db-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca3db-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ca3db-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca3db-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca3db-114">Elements and attributes</span></span>

<span data-ttu-id="ca3db-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ca3db-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ca3db-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ca3db-116">Parent elements</span></span>

|<span data-ttu-id="ca3db-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca3db-117">**Element**</span></span>|<span data-ttu-id="ca3db-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca3db-118">**Type**</span></span>|<span data-ttu-id="ca3db-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca3db-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca3db-120">Section</span><span class="sxs-lookup"><span data-stu-id="ca3db-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ca3db-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ca3db-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ca3db-122">Содержит ячейки для определенного работки элементов управления, определенных для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca3db-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca3db-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ca3db-123">Child elements</span></span>

|<span data-ttu-id="ca3db-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca3db-124">**Element**</span></span>|<span data-ttu-id="ca3db-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca3db-125">**Type**</span></span>|<span data-ttu-id="ca3db-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca3db-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca3db-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ca3db-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="ca3db-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ca3db-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ca3db-129">Содержит свойство для определенного работки управления, определенной для фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca3db-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ca3db-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca3db-130">Attributes</span></span>

|<span data-ttu-id="ca3db-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ca3db-131">**Attribute**</span></span>|<span data-ttu-id="ca3db-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca3db-132">**Type**</span></span>|<span data-ttu-id="ca3db-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ca3db-133">**Required**</span></span>|<span data-ttu-id="ca3db-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca3db-134">**Description**</span></span>|<span data-ttu-id="ca3db-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ca3db-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca3db-136">Del</span><span class="sxs-lookup"><span data-stu-id="ca3db-136">Del</span></span>  <br/> |<span data-ttu-id="ca3db-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ca3db-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ca3db-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca3db-138">optional</span></span>  <br/> |<span data-ttu-id="ca3db-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="ca3db-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ca3db-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ca3db-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ca3db-141">IX</span><span class="sxs-lookup"><span data-stu-id="ca3db-141">IX</span></span>  <br/> |<span data-ttu-id="ca3db-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca3db-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca3db-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca3db-143">optional</span></span>  <br/> |<span data-ttu-id="ca3db-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="ca3db-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ca3db-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="ca3db-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ca3db-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ca3db-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ca3db-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca3db-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca3db-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ca3db-148">LocalName</span></span>  <br/> |<span data-ttu-id="ca3db-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca3db-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ca3db-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca3db-150">optional</span></span>  <br/> |<span data-ttu-id="ca3db-151">Указывает уникальное имя строки, зависимое от языка.</span><span class="sxs-lookup"><span data-stu-id="ca3db-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ca3db-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ca3db-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca3db-153">N</span><span class="sxs-lookup"><span data-stu-id="ca3db-153">N</span></span>  <br/> |<span data-ttu-id="ca3db-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca3db-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ca3db-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca3db-155">optional</span></span>  <br/> |<span data-ttu-id="ca3db-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="ca3db-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ca3db-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ca3db-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ca3db-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ca3db-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca3db-159">T</span><span class="sxs-lookup"><span data-stu-id="ca3db-159">T</span></span>  <br/> |<span data-ttu-id="ca3db-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca3db-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ca3db-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca3db-161">optional</span></span>  <br/> |<span data-ttu-id="ca3db-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="ca3db-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ca3db-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="ca3db-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ca3db-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ca3db-164">Values of the xsd:string type.</span></span>  <br/> |
   

