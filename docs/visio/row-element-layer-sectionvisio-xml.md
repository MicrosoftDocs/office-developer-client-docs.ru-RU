---
title: Элемент Row (раздел Layer) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие одного уровня и его свойства для страницы.
ms.openlocfilehash: 2aff1666f5a2cb87ed10b76e0facdb19a4278c89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396843"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="5c503-103">Элемент Row (раздел Layer) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5c503-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="5c503-104">Содержит элементы, определяющие одного уровня и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="5c503-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c503-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5c503-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c503-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5c503-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5c503-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="5c503-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5c503-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5c503-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5c503-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5c503-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5c503-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5c503-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5c503-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5c503-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5c503-112">Masters.XML, pages.xml</span><span class="sxs-lookup"><span data-stu-id="5c503-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c503-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5c503-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c503-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5c503-114">Elements and attributes</span></span>

<span data-ttu-id="5c503-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5c503-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5c503-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5c503-116">Parent elements</span></span>

|<span data-ttu-id="5c503-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5c503-117">**Element**</span></span>|<span data-ttu-id="5c503-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5c503-118">**Type**</span></span>|<span data-ttu-id="5c503-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c503-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c503-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="5c503-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5c503-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5c503-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c503-122">Содержит элементы, определяющие одного уровня и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="5c503-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c503-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5c503-123">Child elements</span></span>

|<span data-ttu-id="5c503-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5c503-124">**Element**</span></span>|<span data-ttu-id="5c503-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5c503-125">**Type**</span></span>|<span data-ttu-id="5c503-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c503-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c503-127">Cell</span><span class="sxs-lookup"><span data-stu-id="5c503-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5c503-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5c503-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5c503-129">Указывает одно свойство для слоя или его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="5c503-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5c503-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5c503-130">Attributes</span></span>

|<span data-ttu-id="5c503-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5c503-131">**Attribute**</span></span>|<span data-ttu-id="5c503-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5c503-132">**Type**</span></span>|<span data-ttu-id="5c503-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5c503-133">**Required**</span></span>|<span data-ttu-id="5c503-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5c503-134">**Description**</span></span>|<span data-ttu-id="5c503-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5c503-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c503-136">DEL</span><span class="sxs-lookup"><span data-stu-id="5c503-136">Del</span></span>  <br/> |<span data-ttu-id="5c503-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5c503-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5c503-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="5c503-138">optional</span></span>  <br/> |<span data-ttu-id="5c503-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="5c503-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="5c503-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5c503-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5c503-141">IX</span><span class="sxs-lookup"><span data-stu-id="5c503-141">IX</span></span>  <br/> |<span data-ttu-id="5c503-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5c503-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5c503-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="5c503-143">optional</span></span>  <br/> |<span data-ttu-id="5c503-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="5c503-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="5c503-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="5c503-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="5c503-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="5c503-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5c503-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5c503-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5c503-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="5c503-148">LocalName</span></span>  <br/> |<span data-ttu-id="5c503-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5c503-149">xsd:string</span></span>  <br/> |<span data-ttu-id="5c503-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="5c503-150">optional</span></span>  <br/> |<span data-ttu-id="5c503-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="5c503-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="5c503-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5c503-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c503-153">N</span><span class="sxs-lookup"><span data-stu-id="5c503-153">N</span></span>  <br/> |<span data-ttu-id="5c503-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5c503-154">xsd:string</span></span>  <br/> |<span data-ttu-id="5c503-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="5c503-155">optional</span></span>  <br/> |<span data-ttu-id="5c503-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="5c503-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="5c503-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="5c503-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5c503-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5c503-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5c503-159">T</span><span class="sxs-lookup"><span data-stu-id="5c503-159">T</span></span>  <br/> |<span data-ttu-id="5c503-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5c503-160">xsd:string</span></span>  <br/> |<span data-ttu-id="5c503-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="5c503-161">optional</span></span>  <br/> |<span data-ttu-id="5c503-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="5c503-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="5c503-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="5c503-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="5c503-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5c503-164">Values of the xsd:string type.</span></span>  <br/> |
   

