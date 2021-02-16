---
title: Элемент Row (Scratch Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Область работы для ввода и тестирования формул, на которые могут ссылиться другие ячейки.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541003"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="e43d3-103">Элемент Row (Scratch Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e43d3-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="e43d3-104">Область работы для ввода и тестирования формул, на которые могут ссылиться другие ячейки.</span><span class="sxs-lookup"><span data-stu-id="e43d3-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e43d3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e43d3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e43d3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e43d3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e43d3-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="e43d3-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e43d3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e43d3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e43d3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e43d3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e43d3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e43d3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e43d3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e43d3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e43d3-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="e43d3-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e43d3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e43d3-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e43d3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e43d3-114">Elements and attributes</span></span>

<span data-ttu-id="e43d3-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e43d3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e43d3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e43d3-116">Parent elements</span></span>

|<span data-ttu-id="e43d3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e43d3-117">**Element**</span></span>|<span data-ttu-id="e43d3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e43d3-118">**Type**</span></span>|<span data-ttu-id="e43d3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e43d3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e43d3-120">Section</span><span class="sxs-lookup"><span data-stu-id="e43d3-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e43d3-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e43d3-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e43d3-122">Область работы для ввода и тестирования формул, на которые могут ссылиться другие ячейки.</span><span class="sxs-lookup"><span data-stu-id="e43d3-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e43d3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e43d3-123">Child elements</span></span>

|<span data-ttu-id="e43d3-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e43d3-124">**Element**</span></span>|<span data-ttu-id="e43d3-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e43d3-125">**Type**</span></span>|<span data-ttu-id="e43d3-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e43d3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e43d3-127">Cell</span><span class="sxs-lookup"><span data-stu-id="e43d3-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e43d3-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e43d3-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e43d3-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="e43d3-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e43d3-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e43d3-130">Attributes</span></span>

|<span data-ttu-id="e43d3-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e43d3-131">**Attribute**</span></span>|<span data-ttu-id="e43d3-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e43d3-132">**Type**</span></span>|<span data-ttu-id="e43d3-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e43d3-133">**Required**</span></span>|<span data-ttu-id="e43d3-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e43d3-134">**Description**</span></span>|<span data-ttu-id="e43d3-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e43d3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e43d3-136">Del</span><span class="sxs-lookup"><span data-stu-id="e43d3-136">Del</span></span>  <br/> |<span data-ttu-id="e43d3-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e43d3-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e43d3-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e43d3-138">optional</span></span>  <br/> |<span data-ttu-id="e43d3-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="e43d3-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="e43d3-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e43d3-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e43d3-141">IX</span><span class="sxs-lookup"><span data-stu-id="e43d3-141">IX</span></span>  <br/> |<span data-ttu-id="e43d3-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e43d3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e43d3-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="e43d3-143">optional</span></span>  <br/> |<span data-ttu-id="e43d3-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="e43d3-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="e43d3-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="e43d3-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="e43d3-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="e43d3-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e43d3-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e43d3-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e43d3-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="e43d3-148">LocalName</span></span>  <br/> |<span data-ttu-id="e43d3-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e43d3-149">xsd:string</span></span>  <br/> |<span data-ttu-id="e43d3-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="e43d3-150">optional</span></span>  <br/> |<span data-ttu-id="e43d3-151">Указывает уникальное имя строки, зависимое от языка.</span><span class="sxs-lookup"><span data-stu-id="e43d3-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="e43d3-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e43d3-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e43d3-153">N</span><span class="sxs-lookup"><span data-stu-id="e43d3-153">N</span></span>  <br/> |<span data-ttu-id="e43d3-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e43d3-154">xsd:string</span></span>  <br/> |<span data-ttu-id="e43d3-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="e43d3-155">optional</span></span>  <br/> |<span data-ttu-id="e43d3-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="e43d3-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="e43d3-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="e43d3-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e43d3-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e43d3-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e43d3-159">T</span><span class="sxs-lookup"><span data-stu-id="e43d3-159">T</span></span>  <br/> |<span data-ttu-id="e43d3-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e43d3-160">xsd:string</span></span>  <br/> |<span data-ttu-id="e43d3-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="e43d3-161">optional</span></span>  <br/> |<span data-ttu-id="e43d3-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="e43d3-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="e43d3-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="e43d3-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="e43d3-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e43d3-164">Values of the xsd:string type.</span></span>  <br/> |
   

