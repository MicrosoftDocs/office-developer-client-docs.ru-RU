---
title: Элемент Row (раздел элементы управления) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Содержит ячейки для определенного элемента управления дескриптор, определенных для фигуры.
ms.openlocfilehash: cf8015b82f759ba2c166ff5179b2c4324c168e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814648"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="04677-103">Элемент Row (раздел элементы управления) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="04677-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="04677-104">Содержит ячейки для определенного элемента управления дескриптор, определенных для фигуры.</span><span class="sxs-lookup"><span data-stu-id="04677-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04677-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="04677-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04677-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="04677-106">**Element type**</span></span> <br/> |[<span data-ttu-id="04677-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="04677-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="04677-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="04677-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="04677-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="04677-109">**Schema file**</span></span> <br/> |<span data-ttu-id="04677-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="04677-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="04677-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="04677-111">**Document parts**</span></span> <br/> |<span data-ttu-id="04677-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="04677-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04677-113">Определение</span><span class="sxs-lookup"><span data-stu-id="04677-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04677-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="04677-114">Elements and attributes</span></span>

<span data-ttu-id="04677-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="04677-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="04677-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="04677-116">Parent elements</span></span>

|<span data-ttu-id="04677-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="04677-117">**Element**</span></span>|<span data-ttu-id="04677-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="04677-118">**Type**</span></span>|<span data-ttu-id="04677-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04677-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="04677-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="04677-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="04677-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="04677-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="04677-122">Содержит ячейки для определенного элемента управления дескриптор, определенных для фигуры.</span><span class="sxs-lookup"><span data-stu-id="04677-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="04677-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="04677-123">Child elements</span></span>

|<span data-ttu-id="04677-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="04677-124">**Element**</span></span>|<span data-ttu-id="04677-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="04677-125">**Type**</span></span>|<span data-ttu-id="04677-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04677-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="04677-127">Cell</span><span class="sxs-lookup"><span data-stu-id="04677-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="04677-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="04677-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="04677-129">Содержит свойство для определенного элемента управления дескриптор, определенных для фигуры.</span><span class="sxs-lookup"><span data-stu-id="04677-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="04677-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="04677-130">Attributes</span></span>

|<span data-ttu-id="04677-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="04677-131">**Attribute**</span></span>|<span data-ttu-id="04677-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="04677-132">**Type**</span></span>|<span data-ttu-id="04677-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="04677-133">**Required**</span></span>|<span data-ttu-id="04677-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="04677-134">**Description**</span></span>|<span data-ttu-id="04677-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="04677-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04677-136">DEL</span><span class="sxs-lookup"><span data-stu-id="04677-136">Del</span></span>  <br/> |<span data-ttu-id="04677-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="04677-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="04677-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="04677-138">optional</span></span>  <br/> |<span data-ttu-id="04677-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="04677-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="04677-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="04677-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="04677-141">IX</span><span class="sxs-lookup"><span data-stu-id="04677-141">IX</span></span>  <br/> |<span data-ttu-id="04677-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04677-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04677-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="04677-143">optional</span></span>  <br/> |<span data-ttu-id="04677-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="04677-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="04677-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="04677-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="04677-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="04677-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="04677-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04677-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04677-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="04677-148">LocalName</span></span>  <br/> |<span data-ttu-id="04677-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="04677-149">xsd:string</span></span>  <br/> |<span data-ttu-id="04677-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="04677-150">optional</span></span>  <br/> |<span data-ttu-id="04677-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="04677-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="04677-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04677-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04677-153">N</span><span class="sxs-lookup"><span data-stu-id="04677-153">N</span></span>  <br/> |<span data-ttu-id="04677-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="04677-154">xsd:string</span></span>  <br/> |<span data-ttu-id="04677-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="04677-155">optional</span></span>  <br/> |<span data-ttu-id="04677-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="04677-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="04677-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="04677-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="04677-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04677-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04677-159">T</span><span class="sxs-lookup"><span data-stu-id="04677-159">T</span></span>  <br/> |<span data-ttu-id="04677-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="04677-160">xsd:string</span></span>  <br/> |<span data-ttu-id="04677-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="04677-161">optional</span></span>  <br/> |<span data-ttu-id="04677-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="04677-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="04677-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="04677-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="04677-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="04677-164">Values of the xsd:string type.</span></span>  <br/> |
   

