---
title: Элемент Row (раздел в тег действие) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Определяет тег действие на фигуры или страницы.
ms.openlocfilehash: 1ecdb256fbde4a667ade747c2c7216cd0d248fc2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387323"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="a315c-103">Элемент Row (раздел в тег действие) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="a315c-103">Row element (Action Tag Section) ('Visio XML')</span></span>

<span data-ttu-id="a315c-104">Определяет тег действие на фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="a315c-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a315c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a315c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a315c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a315c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a315c-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="a315c-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a315c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a315c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a315c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a315c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a315c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a315c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a315c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="a315c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a315c-112">Masters.XML, главные # .xml, pages.xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="a315c-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a315c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a315c-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a315c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a315c-114">Elements and attributes</span></span>

<span data-ttu-id="a315c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a315c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a315c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a315c-116">Parent elements</span></span>

|<span data-ttu-id="a315c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a315c-117">**Element**</span></span>|<span data-ttu-id="a315c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a315c-118">**Type**</span></span>|<span data-ttu-id="a315c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a315c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a315c-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="a315c-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a315c-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a315c-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a315c-122">Определяет тег действие на фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="a315c-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a315c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a315c-123">Child elements</span></span>

|<span data-ttu-id="a315c-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a315c-124">**Element**</span></span>|<span data-ttu-id="a315c-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a315c-125">**Type**</span></span>|<span data-ttu-id="a315c-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a315c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a315c-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a315c-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a315c-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a315c-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a315c-129">Определяет одно свойство для тега действие на фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="a315c-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a315c-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a315c-130">Attributes</span></span>

|<span data-ttu-id="a315c-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a315c-131">**Attribute**</span></span>|<span data-ttu-id="a315c-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a315c-132">**Type**</span></span>|<span data-ttu-id="a315c-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a315c-133">**Required**</span></span>|<span data-ttu-id="a315c-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a315c-134">**Description**</span></span>|<span data-ttu-id="a315c-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a315c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a315c-136">DEL</span><span class="sxs-lookup"><span data-stu-id="a315c-136">Del</span></span>  <br/> |<span data-ttu-id="a315c-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a315c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a315c-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="a315c-138">optional</span></span>  <br/> |<span data-ttu-id="a315c-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="a315c-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="a315c-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a315c-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a315c-141">IX</span><span class="sxs-lookup"><span data-stu-id="a315c-141">IX</span></span>  <br/> |<span data-ttu-id="a315c-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a315c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a315c-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="a315c-143">optional</span></span>  <br/> |<span data-ttu-id="a315c-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="a315c-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="a315c-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="a315c-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="a315c-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="a315c-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="a315c-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a315c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a315c-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="a315c-148">LocalName</span></span>  <br/> |<span data-ttu-id="a315c-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a315c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="a315c-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="a315c-150">optional</span></span>  <br/> |<span data-ttu-id="a315c-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="a315c-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="a315c-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a315c-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a315c-153">N</span><span class="sxs-lookup"><span data-stu-id="a315c-153">N</span></span>  <br/> |<span data-ttu-id="a315c-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a315c-154">xsd:string</span></span>  <br/> |<span data-ttu-id="a315c-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="a315c-155">optional</span></span>  <br/> |<span data-ttu-id="a315c-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="a315c-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="a315c-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="a315c-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="a315c-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a315c-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a315c-159">T</span><span class="sxs-lookup"><span data-stu-id="a315c-159">T</span></span>  <br/> |<span data-ttu-id="a315c-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a315c-160">xsd:string</span></span>  <br/> |<span data-ttu-id="a315c-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="a315c-161">optional</span></span>  <br/> |<span data-ttu-id="a315c-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="a315c-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="a315c-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="a315c-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="a315c-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a315c-164">Values of the xsd:string type.</span></span>  <br/> |
   

