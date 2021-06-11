---
title: Элемент Row (Раздел элементов управления) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Содержит ячейки для определенной ручки управления, определенной для фигуры.
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541745"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="01af4-103">Элемент Row (Раздел элементов управления) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="01af4-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="01af4-104">Содержит ячейки для определенной ручки управления, определенной для фигуры.</span><span class="sxs-lookup"><span data-stu-id="01af4-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01af4-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="01af4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01af4-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="01af4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="01af4-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="01af4-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="01af4-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="01af4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="01af4-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="01af4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="01af4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="01af4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="01af4-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="01af4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="01af4-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="01af4-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01af4-113">Определение</span><span class="sxs-lookup"><span data-stu-id="01af4-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="01af4-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="01af4-114">Elements and attributes</span></span>

<span data-ttu-id="01af4-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="01af4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="01af4-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="01af4-116">Parent elements</span></span>

|<span data-ttu-id="01af4-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="01af4-117">**Element**</span></span>|<span data-ttu-id="01af4-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01af4-118">**Type**</span></span>|<span data-ttu-id="01af4-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01af4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01af4-120">Section</span><span class="sxs-lookup"><span data-stu-id="01af4-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01af4-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="01af4-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01af4-122">Содержит ячейки для определенной ручки управления, определенной для фигуры.</span><span class="sxs-lookup"><span data-stu-id="01af4-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01af4-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="01af4-123">Child elements</span></span>

|<span data-ttu-id="01af4-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="01af4-124">**Element**</span></span>|<span data-ttu-id="01af4-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01af4-125">**Type**</span></span>|<span data-ttu-id="01af4-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01af4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01af4-127">Cell</span><span class="sxs-lookup"><span data-stu-id="01af4-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="01af4-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="01af4-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01af4-129">Содержит свойство для определенной ручки управления, определенной для фигуры.</span><span class="sxs-lookup"><span data-stu-id="01af4-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="01af4-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="01af4-130">Attributes</span></span>

|<span data-ttu-id="01af4-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="01af4-131">**Attribute**</span></span>|<span data-ttu-id="01af4-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01af4-132">**Type**</span></span>|<span data-ttu-id="01af4-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="01af4-133">**Required**</span></span>|<span data-ttu-id="01af4-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01af4-134">**Description**</span></span>|<span data-ttu-id="01af4-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="01af4-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01af4-136">Del</span><span class="sxs-lookup"><span data-stu-id="01af4-136">Del</span></span>  <br/> |<span data-ttu-id="01af4-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="01af4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="01af4-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="01af4-138">optional</span></span>  <br/> |<span data-ttu-id="01af4-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="01af4-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="01af4-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="01af4-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="01af4-141">IX</span><span class="sxs-lookup"><span data-stu-id="01af4-141">IX</span></span>  <br/> |<span data-ttu-id="01af4-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="01af4-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01af4-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="01af4-143">optional</span></span>  <br/> |<span data-ttu-id="01af4-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="01af4-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="01af4-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="01af4-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="01af4-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="01af4-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="01af4-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="01af4-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01af4-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="01af4-148">LocalName</span></span>  <br/> |<span data-ttu-id="01af4-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="01af4-149">xsd:string</span></span>  <br/> |<span data-ttu-id="01af4-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="01af4-150">optional</span></span>  <br/> |<span data-ttu-id="01af4-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="01af4-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="01af4-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="01af4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="01af4-153">Нет</span><span class="sxs-lookup"><span data-stu-id="01af4-153">N</span></span>  <br/> |<span data-ttu-id="01af4-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="01af4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="01af4-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="01af4-155">optional</span></span>  <br/> |<span data-ttu-id="01af4-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="01af4-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="01af4-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="01af4-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="01af4-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="01af4-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="01af4-159">T</span><span class="sxs-lookup"><span data-stu-id="01af4-159">T</span></span>  <br/> |<span data-ttu-id="01af4-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="01af4-160">xsd:string</span></span>  <br/> |<span data-ttu-id="01af4-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="01af4-161">optional</span></span>  <br/> |<span data-ttu-id="01af4-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="01af4-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="01af4-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="01af4-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="01af4-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="01af4-164">Values of the xsd:string type.</span></span>  <br/> |
   

