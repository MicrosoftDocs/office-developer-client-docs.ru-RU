---
title: Элемент Row (раздел "соединение") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.
ms.openlocfilehash: 9f8f5f0735f7eeff2f1b2ec4562b79e6550d1716
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358577"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="bee52-103">Элемент Row (раздел "соединение") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="bee52-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="bee52-104">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="bee52-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bee52-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bee52-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bee52-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="bee52-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bee52-107">Коннектионров_типе</span><span class="sxs-lookup"><span data-stu-id="bee52-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bee52-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bee52-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bee52-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bee52-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bee52-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="bee52-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bee52-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="bee52-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bee52-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="bee52-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bee52-113">Определение</span><span class="sxs-lookup"><span data-stu-id="bee52-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bee52-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bee52-114">Elements and attributes</span></span>

<span data-ttu-id="bee52-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="bee52-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bee52-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bee52-116">Parent elements</span></span>

|<span data-ttu-id="bee52-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bee52-117">**Element**</span></span>|<span data-ttu-id="bee52-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bee52-118">**Type**</span></span>|<span data-ttu-id="bee52-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bee52-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bee52-120">Section</span><span class="sxs-lookup"><span data-stu-id="bee52-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bee52-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="bee52-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bee52-122">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="bee52-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bee52-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bee52-123">Child elements</span></span>

|<span data-ttu-id="bee52-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bee52-124">**Element**</span></span>|<span data-ttu-id="bee52-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bee52-125">**Type**</span></span>|<span data-ttu-id="bee52-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bee52-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bee52-127">Cell</span><span class="sxs-lookup"><span data-stu-id="bee52-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="bee52-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="bee52-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bee52-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="bee52-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bee52-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bee52-130">Attributes</span></span>

|<span data-ttu-id="bee52-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bee52-131">**Attribute**</span></span>|<span data-ttu-id="bee52-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bee52-132">**Type**</span></span>|<span data-ttu-id="bee52-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="bee52-133">**Required**</span></span>|<span data-ttu-id="bee52-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bee52-134">**Description**</span></span>|<span data-ttu-id="bee52-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bee52-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bee52-136">Del</span><span class="sxs-lookup"><span data-stu-id="bee52-136">Del</span></span>  <br/> |<span data-ttu-id="bee52-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bee52-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bee52-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="bee52-138">optional</span></span>  <br/> |<span data-ttu-id="bee52-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="bee52-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="bee52-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bee52-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bee52-141">IX</span><span class="sxs-lookup"><span data-stu-id="bee52-141">IX</span></span>  <br/> |<span data-ttu-id="bee52-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="bee52-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bee52-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="bee52-143">optional</span></span>  <br/> |<span data-ttu-id="bee52-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="bee52-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="bee52-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="bee52-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="bee52-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="bee52-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bee52-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="bee52-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bee52-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="bee52-148">LocalName</span></span>  <br/> |<span data-ttu-id="bee52-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="bee52-149">xsd:string</span></span>  <br/> |<span data-ttu-id="bee52-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="bee52-150">optional</span></span>  <br/> |<span data-ttu-id="bee52-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="bee52-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="bee52-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="bee52-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bee52-153">N</span><span class="sxs-lookup"><span data-stu-id="bee52-153">N</span></span>  <br/> |<span data-ttu-id="bee52-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="bee52-154">xsd:string</span></span>  <br/> |<span data-ttu-id="bee52-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="bee52-155">optional</span></span>  <br/> |<span data-ttu-id="bee52-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="bee52-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="bee52-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="bee52-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="bee52-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="bee52-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bee52-159">Д</span><span class="sxs-lookup"><span data-stu-id="bee52-159">T</span></span>  <br/> |<span data-ttu-id="bee52-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="bee52-160">xsd:string</span></span>  <br/> |<span data-ttu-id="bee52-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="bee52-161">optional</span></span>  <br/> |<span data-ttu-id="bee52-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="bee52-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="bee52-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="bee52-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="bee52-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="bee52-164">Values of the xsd:string type.</span></span>  <br/> |
   

