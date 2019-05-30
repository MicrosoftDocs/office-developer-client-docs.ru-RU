---
title: Элемент Row (раздел "подключение") (XML-файл Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541766"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="2134f-103">Элемент Row (раздел "подключение") (XML-файл Visio)</span><span class="sxs-lookup"><span data-stu-id="2134f-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="2134f-104">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="2134f-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2134f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2134f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2134f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="2134f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2134f-107">Коннектионров_типе</span><span class="sxs-lookup"><span data-stu-id="2134f-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2134f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2134f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2134f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2134f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2134f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2134f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2134f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="2134f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2134f-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="2134f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2134f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="2134f-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2134f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2134f-114">Elements and attributes</span></span>

<span data-ttu-id="2134f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2134f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2134f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2134f-116">Parent elements</span></span>

|<span data-ttu-id="2134f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2134f-117">**Element**</span></span>|<span data-ttu-id="2134f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2134f-118">**Type**</span></span>|<span data-ttu-id="2134f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2134f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2134f-120">Section</span><span class="sxs-lookup"><span data-stu-id="2134f-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2134f-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="2134f-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2134f-122">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="2134f-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2134f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2134f-123">Child elements</span></span>

|<span data-ttu-id="2134f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2134f-124">**Element**</span></span>|<span data-ttu-id="2134f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2134f-125">**Type**</span></span>|<span data-ttu-id="2134f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2134f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2134f-127">Cell</span><span class="sxs-lookup"><span data-stu-id="2134f-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="2134f-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="2134f-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2134f-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="2134f-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2134f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2134f-130">Attributes</span></span>

|<span data-ttu-id="2134f-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="2134f-131">**Attribute**</span></span>|<span data-ttu-id="2134f-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2134f-132">**Type**</span></span>|<span data-ttu-id="2134f-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="2134f-133">**Required**</span></span>|<span data-ttu-id="2134f-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2134f-134">**Description**</span></span>|<span data-ttu-id="2134f-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="2134f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2134f-136">Del</span><span class="sxs-lookup"><span data-stu-id="2134f-136">Del</span></span>  <br/> |<span data-ttu-id="2134f-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2134f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2134f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="2134f-138">optional</span></span>  <br/> |<span data-ttu-id="2134f-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="2134f-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="2134f-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="2134f-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2134f-141">IX</span><span class="sxs-lookup"><span data-stu-id="2134f-141">IX</span></span>  <br/> |<span data-ttu-id="2134f-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="2134f-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2134f-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="2134f-143">optional</span></span>  <br/> |<span data-ttu-id="2134f-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="2134f-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="2134f-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="2134f-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="2134f-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="2134f-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2134f-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="2134f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2134f-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="2134f-148">LocalName</span></span>  <br/> |<span data-ttu-id="2134f-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2134f-149">xsd:string</span></span>  <br/> |<span data-ttu-id="2134f-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="2134f-150">optional</span></span>  <br/> |<span data-ttu-id="2134f-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="2134f-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="2134f-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2134f-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2134f-153">N</span><span class="sxs-lookup"><span data-stu-id="2134f-153">N</span></span>  <br/> |<span data-ttu-id="2134f-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2134f-154">xsd:string</span></span>  <br/> |<span data-ttu-id="2134f-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="2134f-155">optional</span></span>  <br/> |<span data-ttu-id="2134f-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="2134f-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="2134f-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="2134f-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="2134f-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2134f-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2134f-159">Д</span><span class="sxs-lookup"><span data-stu-id="2134f-159">T</span></span>  <br/> |<span data-ttu-id="2134f-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2134f-160">xsd:string</span></span>  <br/> |<span data-ttu-id="2134f-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="2134f-161">optional</span></span>  <br/> |<span data-ttu-id="2134f-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="2134f-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="2134f-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="2134f-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="2134f-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2134f-164">Values of the xsd:string type.</span></span>  <br/> |
   

