---
title: Элемент Row (раздел Layer) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие одного уровня и его свойства для страницы.
ms.openlocfilehash: ed8368c0c7215068cbbfcdd89c1f5b56969b5a06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814685"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="ace19-103">Элемент Row (раздел Layer) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ace19-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="ace19-104">Содержит элементы, определяющие одного уровня и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="ace19-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ace19-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ace19-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ace19-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ace19-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ace19-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="ace19-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ace19-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ace19-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ace19-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ace19-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ace19-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ace19-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ace19-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ace19-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ace19-112">Masters.XML, pages.xml</span><span class="sxs-lookup"><span data-stu-id="ace19-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ace19-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ace19-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ace19-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ace19-114">Elements and attributes</span></span>

<span data-ttu-id="ace19-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ace19-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ace19-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ace19-116">Parent elements</span></span>

|<span data-ttu-id="ace19-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ace19-117">**Element**</span></span>|<span data-ttu-id="ace19-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace19-118">**Type**</span></span>|<span data-ttu-id="ace19-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace19-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ace19-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="ace19-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ace19-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ace19-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ace19-122">Содержит элементы, определяющие одного уровня и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="ace19-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ace19-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ace19-123">Child elements</span></span>

|<span data-ttu-id="ace19-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ace19-124">**Element**</span></span>|<span data-ttu-id="ace19-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace19-125">**Type**</span></span>|<span data-ttu-id="ace19-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace19-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ace19-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ace19-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ace19-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ace19-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ace19-129">Указывает одно свойство для слоя или его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="ace19-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ace19-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ace19-130">Attributes</span></span>

|<span data-ttu-id="ace19-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ace19-131">**Attribute**</span></span>|<span data-ttu-id="ace19-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace19-132">**Type**</span></span>|<span data-ttu-id="ace19-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ace19-133">**Required**</span></span>|<span data-ttu-id="ace19-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace19-134">**Description**</span></span>|<span data-ttu-id="ace19-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ace19-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ace19-136">DEL</span><span class="sxs-lookup"><span data-stu-id="ace19-136">Del</span></span>  <br/> |<span data-ttu-id="ace19-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ace19-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ace19-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace19-138">optional</span></span>  <br/> |<span data-ttu-id="ace19-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="ace19-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ace19-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ace19-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ace19-141">IX</span><span class="sxs-lookup"><span data-stu-id="ace19-141">IX</span></span>  <br/> |<span data-ttu-id="ace19-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ace19-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ace19-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace19-143">optional</span></span>  <br/> |<span data-ttu-id="ace19-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="ace19-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ace19-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="ace19-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ace19-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ace19-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ace19-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ace19-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ace19-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ace19-148">LocalName</span></span>  <br/> |<span data-ttu-id="ace19-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ace19-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ace19-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace19-150">optional</span></span>  <br/> |<span data-ttu-id="ace19-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="ace19-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ace19-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace19-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ace19-153">N</span><span class="sxs-lookup"><span data-stu-id="ace19-153">N</span></span>  <br/> |<span data-ttu-id="ace19-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ace19-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ace19-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace19-155">optional</span></span>  <br/> |<span data-ttu-id="ace19-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="ace19-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ace19-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ace19-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ace19-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace19-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ace19-159">T</span><span class="sxs-lookup"><span data-stu-id="ace19-159">T</span></span>  <br/> |<span data-ttu-id="ace19-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ace19-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ace19-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace19-161">optional</span></span>  <br/> |<span data-ttu-id="ace19-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="ace19-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ace19-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="ace19-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ace19-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace19-164">Values of the xsd:string type.</span></span>  <br/> |
   

