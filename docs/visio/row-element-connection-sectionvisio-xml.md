---
title: Элемент Row (раздел подключения) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.
ms.openlocfilehash: d06a51e52f2b5273171d068f6fc2a6bf5227eed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814651"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="0f93a-103">Элемент Row (раздел подключения) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0f93a-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="0f93a-104">Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.</span><span class="sxs-lookup"><span data-stu-id="0f93a-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f93a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0f93a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f93a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0f93a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0f93a-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="0f93a-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0f93a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0f93a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0f93a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0f93a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0f93a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0f93a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0f93a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0f93a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0f93a-112">главные # .xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="0f93a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f93a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0f93a-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0f93a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f93a-114">Elements and attributes</span></span>

<span data-ttu-id="0f93a-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="0f93a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0f93a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0f93a-116">Parent elements</span></span>

|<span data-ttu-id="0f93a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0f93a-117">**Element**</span></span>|<span data-ttu-id="0f93a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0f93a-118">**Type**</span></span>|<span data-ttu-id="0f93a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f93a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f93a-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="0f93a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0f93a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0f93a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f93a-122">Содержит координаты x и y, направление горизонтальных и вертикальных и тип одна точка подключения на фигуры.</span><span class="sxs-lookup"><span data-stu-id="0f93a-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f93a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0f93a-123">Child elements</span></span>

|<span data-ttu-id="0f93a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0f93a-124">**Element**</span></span>|<span data-ttu-id="0f93a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0f93a-125">**Type**</span></span>|<span data-ttu-id="0f93a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f93a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f93a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="0f93a-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="0f93a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0f93a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0f93a-129">Задает отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="0f93a-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0f93a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f93a-130">Attributes</span></span>

|<span data-ttu-id="0f93a-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0f93a-131">**Attribute**</span></span>|<span data-ttu-id="0f93a-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0f93a-132">**Type**</span></span>|<span data-ttu-id="0f93a-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="0f93a-133">**Required**</span></span>|<span data-ttu-id="0f93a-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f93a-134">**Description**</span></span>|<span data-ttu-id="0f93a-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0f93a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0f93a-136">DEL</span><span class="sxs-lookup"><span data-stu-id="0f93a-136">Del</span></span>  <br/> |<span data-ttu-id="0f93a-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0f93a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0f93a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0f93a-138">optional</span></span>  <br/> |<span data-ttu-id="0f93a-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="0f93a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="0f93a-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0f93a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0f93a-141">IX</span><span class="sxs-lookup"><span data-stu-id="0f93a-141">IX</span></span>  <br/> |<span data-ttu-id="0f93a-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0f93a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0f93a-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="0f93a-143">optional</span></span>  <br/> |<span data-ttu-id="0f93a-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="0f93a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="0f93a-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="0f93a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="0f93a-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="0f93a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0f93a-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0f93a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0f93a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="0f93a-148">LocalName</span></span>  <br/> |<span data-ttu-id="0f93a-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0f93a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="0f93a-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="0f93a-150">optional</span></span>  <br/> |<span data-ttu-id="0f93a-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="0f93a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="0f93a-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0f93a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0f93a-153">N</span><span class="sxs-lookup"><span data-stu-id="0f93a-153">N</span></span>  <br/> |<span data-ttu-id="0f93a-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0f93a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="0f93a-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="0f93a-155">optional</span></span>  <br/> |<span data-ttu-id="0f93a-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="0f93a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="0f93a-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="0f93a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="0f93a-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0f93a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0f93a-159">T</span><span class="sxs-lookup"><span data-stu-id="0f93a-159">T</span></span>  <br/> |<span data-ttu-id="0f93a-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0f93a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="0f93a-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="0f93a-161">optional</span></span>  <br/> |<span data-ttu-id="0f93a-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="0f93a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="0f93a-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="0f93a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="0f93a-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0f93a-164">Values of the xsd:string type.</span></span>  <br/> |
   

