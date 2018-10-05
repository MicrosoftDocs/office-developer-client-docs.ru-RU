---
title: Элемент Row (вспомогательный раздел) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.
ms.openlocfilehash: eac975fa1233e74b7bb5f2efc90b6b6edad8215c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388009"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="d6e3b-103">Элемент Row (вспомогательный раздел) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d6e3b-103">Row element (Scratch Section) ('Visio XML')</span></span>

<span data-ttu-id="d6e3b-104">Рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6e3b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d6e3b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6e3b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d6e3b-107">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="d6e3b-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d6e3b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d6e3b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d6e3b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d6e3b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d6e3b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d6e3b-112">Document.XML, masters.xml, главные # .xml, pages.xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="d6e3b-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6e3b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d6e3b-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6e3b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-114">Elements and attributes</span></span>

<span data-ttu-id="d6e3b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d6e3b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d6e3b-116">Parent elements</span></span>

|<span data-ttu-id="d6e3b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-117">**Element**</span></span>|<span data-ttu-id="d6e3b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-118">**Type**</span></span>|<span data-ttu-id="d6e3b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6e3b-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="d6e3b-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6e3b-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d6e3b-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6e3b-122">Рабочая область для ввода и проверки формул, которые могут использоваться в других ячеек.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6e3b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d6e3b-123">Child elements</span></span>

|<span data-ttu-id="d6e3b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-124">**Element**</span></span>|<span data-ttu-id="d6e3b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-125">**Type**</span></span>|<span data-ttu-id="d6e3b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6e3b-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d6e3b-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d6e3b-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d6e3b-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6e3b-129">Задает отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d6e3b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d6e3b-130">Attributes</span></span>

|<span data-ttu-id="d6e3b-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-131">**Attribute**</span></span>|<span data-ttu-id="d6e3b-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-132">**Type**</span></span>|<span data-ttu-id="d6e3b-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-133">**Required**</span></span>|<span data-ttu-id="d6e3b-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-134">**Description**</span></span>|<span data-ttu-id="d6e3b-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d6e3b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6e3b-136">DEL</span><span class="sxs-lookup"><span data-stu-id="d6e3b-136">Del</span></span>  <br/> |<span data-ttu-id="d6e3b-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d6e3b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d6e3b-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-138">optional</span></span>  <br/> |<span data-ttu-id="d6e3b-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="d6e3b-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d6e3b-141">IX</span><span class="sxs-lookup"><span data-stu-id="d6e3b-141">IX</span></span>  <br/> |<span data-ttu-id="d6e3b-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d6e3b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d6e3b-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-143">optional</span></span>  <br/> |<span data-ttu-id="d6e3b-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="d6e3b-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="d6e3b-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d6e3b-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d6e3b-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="d6e3b-148">LocalName</span></span>  <br/> |<span data-ttu-id="d6e3b-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d6e3b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d6e3b-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-150">optional</span></span>  <br/> |<span data-ttu-id="d6e3b-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="d6e3b-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d6e3b-153">N</span><span class="sxs-lookup"><span data-stu-id="d6e3b-153">N</span></span>  <br/> |<span data-ttu-id="d6e3b-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d6e3b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="d6e3b-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-155">optional</span></span>  <br/> |<span data-ttu-id="d6e3b-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="d6e3b-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d6e3b-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d6e3b-159">T</span><span class="sxs-lookup"><span data-stu-id="d6e3b-159">T</span></span>  <br/> |<span data-ttu-id="d6e3b-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d6e3b-160">xsd:string</span></span>  <br/> |<span data-ttu-id="d6e3b-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="d6e3b-161">optional</span></span>  <br/> |<span data-ttu-id="d6e3b-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="d6e3b-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="d6e3b-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-164">Values of the xsd:string type.</span></span>  <br/> |
   

