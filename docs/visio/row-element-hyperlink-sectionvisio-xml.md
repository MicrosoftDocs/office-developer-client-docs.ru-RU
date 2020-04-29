---
title: Элемент Row (раздел "гиперссылка") (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.
ms.openlocfilehash: d2147504455c4edb13681a20aab0ade6a100a532
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540884"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="55d35-103">Элемент Row (раздел "гиперссылка") (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="55d35-103">Row element (Hyperlink Section) (Visio XML)</span></span>

<span data-ttu-id="55d35-104">Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="55d35-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55d35-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="55d35-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55d35-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="55d35-106">**Element type**</span></span> <br/> |[<span data-ttu-id="55d35-107">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="55d35-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="55d35-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="55d35-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="55d35-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="55d35-109">**Schema file**</span></span> <br/> |<span data-ttu-id="55d35-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="55d35-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="55d35-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="55d35-111">**Document parts**</span></span> <br/> |<span data-ttu-id="55d35-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="55d35-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55d35-113">Определение</span><span class="sxs-lookup"><span data-stu-id="55d35-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="55d35-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="55d35-114">Elements and attributes</span></span>

<span data-ttu-id="55d35-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="55d35-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="55d35-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="55d35-116">Parent elements</span></span>

|<span data-ttu-id="55d35-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="55d35-117">**Element**</span></span>|<span data-ttu-id="55d35-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="55d35-118">**Type**</span></span>|<span data-ttu-id="55d35-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55d35-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55d35-120">Section</span><span class="sxs-lookup"><span data-stu-id="55d35-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55d35-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="55d35-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55d35-122">Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="55d35-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55d35-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="55d35-123">Child elements</span></span>

|<span data-ttu-id="55d35-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="55d35-124">**Element**</span></span>|<span data-ttu-id="55d35-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="55d35-125">**Type**</span></span>|<span data-ttu-id="55d35-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55d35-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55d35-127">Cell</span><span class="sxs-lookup"><span data-stu-id="55d35-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="55d35-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="55d35-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55d35-129">Содержит сведения о одной гиперссылке, связанной с фигурой</span><span class="sxs-lookup"><span data-stu-id="55d35-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="55d35-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="55d35-130">Attributes</span></span>

|<span data-ttu-id="55d35-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="55d35-131">**Attribute**</span></span>|<span data-ttu-id="55d35-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="55d35-132">**Type**</span></span>|<span data-ttu-id="55d35-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="55d35-133">**Required**</span></span>|<span data-ttu-id="55d35-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55d35-134">**Description**</span></span>|<span data-ttu-id="55d35-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="55d35-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="55d35-136">Del</span><span class="sxs-lookup"><span data-stu-id="55d35-136">Del</span></span>  <br/> |<span data-ttu-id="55d35-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="55d35-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55d35-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="55d35-138">optional</span></span>  <br/> |<span data-ttu-id="55d35-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="55d35-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="55d35-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="55d35-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="55d35-141">IX</span><span class="sxs-lookup"><span data-stu-id="55d35-141">IX</span></span>  <br/> |<span data-ttu-id="55d35-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="55d35-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="55d35-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="55d35-143">optional</span></span>  <br/> |<span data-ttu-id="55d35-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="55d35-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="55d35-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="55d35-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="55d35-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="55d35-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="55d35-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="55d35-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="55d35-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="55d35-148">LocalName</span></span>  <br/> |<span data-ttu-id="55d35-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="55d35-149">xsd:string</span></span>  <br/> |<span data-ttu-id="55d35-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="55d35-150">optional</span></span>  <br/> |<span data-ttu-id="55d35-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="55d35-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="55d35-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="55d35-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55d35-153">N</span><span class="sxs-lookup"><span data-stu-id="55d35-153">N</span></span>  <br/> |<span data-ttu-id="55d35-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="55d35-154">xsd:string</span></span>  <br/> |<span data-ttu-id="55d35-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="55d35-155">optional</span></span>  <br/> |<span data-ttu-id="55d35-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="55d35-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="55d35-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="55d35-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="55d35-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="55d35-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="55d35-159">Д</span><span class="sxs-lookup"><span data-stu-id="55d35-159">T</span></span>  <br/> |<span data-ttu-id="55d35-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="55d35-160">xsd:string</span></span>  <br/> |<span data-ttu-id="55d35-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="55d35-161">optional</span></span>  <br/> |<span data-ttu-id="55d35-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="55d35-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="55d35-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="55d35-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="55d35-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="55d35-164">Values of the xsd:string type.</span></span>  <br/> |
   

