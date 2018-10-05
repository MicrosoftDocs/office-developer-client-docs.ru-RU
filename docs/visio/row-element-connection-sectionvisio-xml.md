---
title: Элемент Row (раздел подключения) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.
ms.openlocfilehash: 9f8f5f0735f7eeff2f1b2ec4562b79e6550d1716
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389920"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="98c51-103">Элемент Row (раздел подключения) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="98c51-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="98c51-104">Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.</span><span class="sxs-lookup"><span data-stu-id="98c51-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98c51-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98c51-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98c51-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="98c51-106">**Element type**</span></span> <br/> |[<span data-ttu-id="98c51-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="98c51-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="98c51-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="98c51-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="98c51-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="98c51-109">**Schema file**</span></span> <br/> |<span data-ttu-id="98c51-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="98c51-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="98c51-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="98c51-111">**Document parts**</span></span> <br/> |<span data-ttu-id="98c51-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="98c51-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98c51-113">Определение</span><span class="sxs-lookup"><span data-stu-id="98c51-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="98c51-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="98c51-114">Elements and attributes</span></span>

<span data-ttu-id="98c51-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="98c51-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="98c51-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="98c51-116">Parent elements</span></span>

|<span data-ttu-id="98c51-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="98c51-117">**Element**</span></span>|<span data-ttu-id="98c51-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="98c51-118">**Type**</span></span>|<span data-ttu-id="98c51-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98c51-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98c51-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="98c51-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="98c51-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="98c51-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="98c51-122">Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.</span><span class="sxs-lookup"><span data-stu-id="98c51-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98c51-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="98c51-123">Child elements</span></span>

|<span data-ttu-id="98c51-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="98c51-124">**Element**</span></span>|<span data-ttu-id="98c51-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="98c51-125">**Type**</span></span>|<span data-ttu-id="98c51-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98c51-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98c51-127">Cell</span><span class="sxs-lookup"><span data-stu-id="98c51-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="98c51-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="98c51-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="98c51-129">Задает отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="98c51-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="98c51-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="98c51-130">Attributes</span></span>

|<span data-ttu-id="98c51-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="98c51-131">**Attribute**</span></span>|<span data-ttu-id="98c51-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="98c51-132">**Type**</span></span>|<span data-ttu-id="98c51-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="98c51-133">**Required**</span></span>|<span data-ttu-id="98c51-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98c51-134">**Description**</span></span>|<span data-ttu-id="98c51-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="98c51-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98c51-136">DEL</span><span class="sxs-lookup"><span data-stu-id="98c51-136">Del</span></span>  <br/> |<span data-ttu-id="98c51-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="98c51-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="98c51-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="98c51-138">optional</span></span>  <br/> |<span data-ttu-id="98c51-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="98c51-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="98c51-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="98c51-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="98c51-141">IX</span><span class="sxs-lookup"><span data-stu-id="98c51-141">IX</span></span>  <br/> |<span data-ttu-id="98c51-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="98c51-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="98c51-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="98c51-143">optional</span></span>  <br/> |<span data-ttu-id="98c51-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="98c51-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="98c51-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="98c51-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="98c51-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="98c51-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="98c51-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="98c51-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="98c51-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="98c51-148">LocalName</span></span>  <br/> |<span data-ttu-id="98c51-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="98c51-149">xsd:string</span></span>  <br/> |<span data-ttu-id="98c51-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="98c51-150">optional</span></span>  <br/> |<span data-ttu-id="98c51-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="98c51-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="98c51-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98c51-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="98c51-153">N</span><span class="sxs-lookup"><span data-stu-id="98c51-153">N</span></span>  <br/> |<span data-ttu-id="98c51-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="98c51-154">xsd:string</span></span>  <br/> |<span data-ttu-id="98c51-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="98c51-155">optional</span></span>  <br/> |<span data-ttu-id="98c51-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="98c51-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="98c51-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="98c51-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="98c51-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98c51-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="98c51-159">T</span><span class="sxs-lookup"><span data-stu-id="98c51-159">T</span></span>  <br/> |<span data-ttu-id="98c51-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="98c51-160">xsd:string</span></span>  <br/> |<span data-ttu-id="98c51-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="98c51-161">optional</span></span>  <br/> |<span data-ttu-id="98c51-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="98c51-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="98c51-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="98c51-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="98c51-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="98c51-164">Values of the xsd:string type.</span></span>  <br/> |
   

