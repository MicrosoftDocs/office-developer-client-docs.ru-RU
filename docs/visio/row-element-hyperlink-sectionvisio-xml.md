---
title: Элемент Row (раздел "гиперссылка") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.
ms.openlocfilehash: 16935e463e76e0f0ee72b3fa40964551cf125cdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358574"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="563c2-103">Элемент Row (раздел "гиперссылка") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="563c2-103">Row element (Hyperlink Section) ('Visio XML')</span></span>

<span data-ttu-id="563c2-104">Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="563c2-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="563c2-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="563c2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="563c2-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="563c2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="563c2-107">Хиперлинкров_типе</span><span class="sxs-lookup"><span data-stu-id="563c2-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="563c2-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="563c2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="563c2-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="563c2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="563c2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="563c2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="563c2-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="563c2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="563c2-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="563c2-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="563c2-113">Определение</span><span class="sxs-lookup"><span data-stu-id="563c2-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="563c2-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="563c2-114">Elements and attributes</span></span>

<span data-ttu-id="563c2-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="563c2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="563c2-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="563c2-116">Parent elements</span></span>

|<span data-ttu-id="563c2-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="563c2-117">**Element**</span></span>|<span data-ttu-id="563c2-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="563c2-118">**Type**</span></span>|<span data-ttu-id="563c2-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="563c2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="563c2-120">Section</span><span class="sxs-lookup"><span data-stu-id="563c2-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="563c2-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="563c2-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="563c2-122">Содержит элементы для создания нескольких переходов между фигурой или страницей документа и другой странице документа, файлом или веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="563c2-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="563c2-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="563c2-123">Child elements</span></span>

|<span data-ttu-id="563c2-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="563c2-124">**Element**</span></span>|<span data-ttu-id="563c2-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="563c2-125">**Type**</span></span>|<span data-ttu-id="563c2-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="563c2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="563c2-127">Cell</span><span class="sxs-lookup"><span data-stu-id="563c2-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="563c2-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="563c2-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="563c2-129">Содержит сведения о одной гиперссылке, связанной с фигурой</span><span class="sxs-lookup"><span data-stu-id="563c2-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="563c2-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="563c2-130">Attributes</span></span>

|<span data-ttu-id="563c2-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="563c2-131">**Attribute**</span></span>|<span data-ttu-id="563c2-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="563c2-132">**Type**</span></span>|<span data-ttu-id="563c2-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="563c2-133">**Required**</span></span>|<span data-ttu-id="563c2-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="563c2-134">**Description**</span></span>|<span data-ttu-id="563c2-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="563c2-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="563c2-136">Del</span><span class="sxs-lookup"><span data-stu-id="563c2-136">Del</span></span>  <br/> |<span data-ttu-id="563c2-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="563c2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="563c2-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="563c2-138">optional</span></span>  <br/> |<span data-ttu-id="563c2-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="563c2-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="563c2-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="563c2-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="563c2-141">IX</span><span class="sxs-lookup"><span data-stu-id="563c2-141">IX</span></span>  <br/> |<span data-ttu-id="563c2-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="563c2-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="563c2-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="563c2-143">optional</span></span>  <br/> |<span data-ttu-id="563c2-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="563c2-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="563c2-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="563c2-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="563c2-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="563c2-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="563c2-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="563c2-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="563c2-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="563c2-148">LocalName</span></span>  <br/> |<span data-ttu-id="563c2-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="563c2-149">xsd:string</span></span>  <br/> |<span data-ttu-id="563c2-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="563c2-150">optional</span></span>  <br/> |<span data-ttu-id="563c2-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="563c2-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="563c2-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="563c2-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="563c2-153">N</span><span class="sxs-lookup"><span data-stu-id="563c2-153">N</span></span>  <br/> |<span data-ttu-id="563c2-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="563c2-154">xsd:string</span></span>  <br/> |<span data-ttu-id="563c2-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="563c2-155">optional</span></span>  <br/> |<span data-ttu-id="563c2-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="563c2-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="563c2-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="563c2-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="563c2-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="563c2-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="563c2-159">Д</span><span class="sxs-lookup"><span data-stu-id="563c2-159">T</span></span>  <br/> |<span data-ttu-id="563c2-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="563c2-160">xsd:string</span></span>  <br/> |<span data-ttu-id="563c2-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="563c2-161">optional</span></span>  <br/> |<span data-ttu-id="563c2-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="563c2-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="563c2-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="563c2-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="563c2-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="563c2-164">Values of the xsd:string type.</span></span>  <br/> |
   

