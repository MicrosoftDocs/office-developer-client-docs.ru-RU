---
title: Элемент Row (вкладки раздел) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a30d5701-4b56-c44c-fb62-d9daaee3b86e
description: Содержит ячейки для фигур или стилей, которые управляют позиции табуляции и выравнивание.
ms.openlocfilehash: 7d233e5051e5b7ab9715d2840182b1426f31f5bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814686"
---
# <a name="row-element-tabs-section-visio-xml"></a><span data-ttu-id="bd51d-103">Элемент Row (вкладки раздел) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bd51d-103">Row element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="bd51d-104">Содержит ячейки для фигур или стилей, которые управляют позиции табуляции и выравнивание.</span><span class="sxs-lookup"><span data-stu-id="bd51d-104">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd51d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bd51d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd51d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="bd51d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bd51d-107">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="bd51d-107">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bd51d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bd51d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bd51d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bd51d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bd51d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bd51d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bd51d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="bd51d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bd51d-112">Document.XML, главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="bd51d-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd51d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="bd51d-113">Definition</span></span>

```XML
< xs:element name="Row" type="TabsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bd51d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bd51d-114">Elements and attributes</span></span>

<span data-ttu-id="bd51d-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bd51d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bd51d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bd51d-116">Parent elements</span></span>

|<span data-ttu-id="bd51d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bd51d-117">**Element**</span></span>|<span data-ttu-id="bd51d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bd51d-118">**Type**</span></span>|<span data-ttu-id="bd51d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd51d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd51d-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="bd51d-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bd51d-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="bd51d-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bd51d-122">Содержит ячейки для фигур или стилей, которые управляют позиции табуляции и выравнивание.</span><span class="sxs-lookup"><span data-stu-id="bd51d-122">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd51d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bd51d-123">Child elements</span></span>

|<span data-ttu-id="bd51d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bd51d-124">**Element**</span></span>|<span data-ttu-id="bd51d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bd51d-125">**Type**</span></span>|<span data-ttu-id="bd51d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd51d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd51d-127">Cell</span><span class="sxs-lookup"><span data-stu-id="bd51d-127">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bd51d-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bd51d-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bd51d-129">Задает отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="bd51d-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bd51d-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bd51d-130">Attributes</span></span>

|<span data-ttu-id="bd51d-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bd51d-131">**Attribute**</span></span>|<span data-ttu-id="bd51d-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bd51d-132">**Type**</span></span>|<span data-ttu-id="bd51d-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="bd51d-133">**Required**</span></span>|<span data-ttu-id="bd51d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd51d-134">**Description**</span></span>|<span data-ttu-id="bd51d-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bd51d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd51d-136">DEL</span><span class="sxs-lookup"><span data-stu-id="bd51d-136">Del</span></span>  <br/> |<span data-ttu-id="bd51d-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="bd51d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bd51d-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="bd51d-138">optional</span></span>  <br/> |<span data-ttu-id="bd51d-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="bd51d-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="bd51d-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="bd51d-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bd51d-141">IX</span><span class="sxs-lookup"><span data-stu-id="bd51d-141">IX</span></span>  <br/> |<span data-ttu-id="bd51d-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd51d-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd51d-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="bd51d-143">optional</span></span>  <br/> |<span data-ttu-id="bd51d-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="bd51d-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="bd51d-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="bd51d-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="bd51d-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="bd51d-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bd51d-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd51d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd51d-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="bd51d-148">LocalName</span></span>  <br/> |<span data-ttu-id="bd51d-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bd51d-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bd51d-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="bd51d-150">optional</span></span>  <br/> |<span data-ttu-id="bd51d-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="bd51d-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="bd51d-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bd51d-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd51d-153">N</span><span class="sxs-lookup"><span data-stu-id="bd51d-153">N</span></span>  <br/> |<span data-ttu-id="bd51d-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bd51d-154">xsd:string</span></span>  <br/> |<span data-ttu-id="bd51d-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="bd51d-155">optional</span></span>  <br/> |<span data-ttu-id="bd51d-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="bd51d-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="bd51d-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="bd51d-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bd51d-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bd51d-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd51d-159">T</span><span class="sxs-lookup"><span data-stu-id="bd51d-159">T</span></span>  <br/> |<span data-ttu-id="bd51d-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bd51d-160">xsd:string</span></span>  <br/> |<span data-ttu-id="bd51d-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="bd51d-161">optional</span></span>  <br/> |<span data-ttu-id="bd51d-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="bd51d-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="bd51d-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="bd51d-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="bd51d-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bd51d-164">Values of the xsd:string type.</span></span>  <br/> |
   

