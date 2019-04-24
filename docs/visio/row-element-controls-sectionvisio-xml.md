---
title: Элемент Row (раздел "элементы управления") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: Содержит ячейки для определенного управляющего маркера, определенного для фигуры.
ms.openlocfilehash: aa690bf70078a711dffca3f01b6e7acc05507bdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358424"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="68156-103">Элемент Row (раздел "элементы управления") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="68156-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="68156-104">Содержит ячейки для определенного управляющего маркера, определенного для фигуры.</span><span class="sxs-lookup"><span data-stu-id="68156-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68156-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="68156-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68156-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="68156-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68156-107">Контролров_типе</span><span class="sxs-lookup"><span data-stu-id="68156-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68156-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="68156-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68156-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="68156-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68156-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="68156-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68156-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="68156-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68156-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="68156-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68156-113">Определение</span><span class="sxs-lookup"><span data-stu-id="68156-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68156-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="68156-114">Elements and attributes</span></span>

<span data-ttu-id="68156-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="68156-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68156-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="68156-116">Parent elements</span></span>

|<span data-ttu-id="68156-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="68156-117">**Element**</span></span>|<span data-ttu-id="68156-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="68156-118">**Type**</span></span>|<span data-ttu-id="68156-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68156-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68156-120">Section</span><span class="sxs-lookup"><span data-stu-id="68156-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68156-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="68156-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68156-122">Содержит ячейки для определенного управляющего маркера, определенного для фигуры.</span><span class="sxs-lookup"><span data-stu-id="68156-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68156-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="68156-123">Child elements</span></span>

|<span data-ttu-id="68156-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="68156-124">**Element**</span></span>|<span data-ttu-id="68156-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="68156-125">**Type**</span></span>|<span data-ttu-id="68156-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68156-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68156-127">Cell</span><span class="sxs-lookup"><span data-stu-id="68156-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="68156-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="68156-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68156-129">Содержит свойство для определенного управляющего маркера, определенного для фигуры.</span><span class="sxs-lookup"><span data-stu-id="68156-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68156-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="68156-130">Attributes</span></span>

|<span data-ttu-id="68156-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="68156-131">**Attribute**</span></span>|<span data-ttu-id="68156-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="68156-132">**Type**</span></span>|<span data-ttu-id="68156-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="68156-133">**Required**</span></span>|<span data-ttu-id="68156-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68156-134">**Description**</span></span>|<span data-ttu-id="68156-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="68156-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68156-136">Del</span><span class="sxs-lookup"><span data-stu-id="68156-136">Del</span></span>  <br/> |<span data-ttu-id="68156-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="68156-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="68156-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="68156-138">optional</span></span>  <br/> |<span data-ttu-id="68156-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="68156-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="68156-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="68156-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="68156-141">IX</span><span class="sxs-lookup"><span data-stu-id="68156-141">IX</span></span>  <br/> |<span data-ttu-id="68156-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="68156-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68156-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="68156-143">optional</span></span>  <br/> |<span data-ttu-id="68156-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="68156-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="68156-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="68156-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="68156-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="68156-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68156-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="68156-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68156-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="68156-148">LocalName</span></span>  <br/> |<span data-ttu-id="68156-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="68156-149">xsd:string</span></span>  <br/> |<span data-ttu-id="68156-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="68156-150">optional</span></span>  <br/> |<span data-ttu-id="68156-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="68156-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="68156-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="68156-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68156-153">N</span><span class="sxs-lookup"><span data-stu-id="68156-153">N</span></span>  <br/> |<span data-ttu-id="68156-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="68156-154">xsd:string</span></span>  <br/> |<span data-ttu-id="68156-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="68156-155">optional</span></span>  <br/> |<span data-ttu-id="68156-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="68156-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="68156-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="68156-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="68156-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="68156-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="68156-159">Д</span><span class="sxs-lookup"><span data-stu-id="68156-159">T</span></span>  <br/> |<span data-ttu-id="68156-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="68156-160">xsd:string</span></span>  <br/> |<span data-ttu-id="68156-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="68156-161">optional</span></span>  <br/> |<span data-ttu-id="68156-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="68156-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="68156-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="68156-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="68156-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="68156-164">Values of the xsd:string type.</span></span>  <br/> |
   

