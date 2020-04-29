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
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="58f5a-103">Элемент Row (раздел "подключение") (XML-файл Visio)</span><span class="sxs-lookup"><span data-stu-id="58f5a-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="58f5a-104">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="58f5a-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58f5a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="58f5a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58f5a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="58f5a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="58f5a-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="58f5a-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="58f5a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="58f5a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="58f5a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="58f5a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="58f5a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="58f5a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="58f5a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="58f5a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="58f5a-112">Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="58f5a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58f5a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="58f5a-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="58f5a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="58f5a-114">Elements and attributes</span></span>

<span data-ttu-id="58f5a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="58f5a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="58f5a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="58f5a-116">Parent elements</span></span>

|<span data-ttu-id="58f5a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="58f5a-117">**Element**</span></span>|<span data-ttu-id="58f5a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58f5a-118">**Type**</span></span>|<span data-ttu-id="58f5a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58f5a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58f5a-120">Section</span><span class="sxs-lookup"><span data-stu-id="58f5a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58f5a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="58f5a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58f5a-122">Содержит координаты x или y, горизонтальное и вертикальное направление и тип для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="58f5a-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58f5a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="58f5a-123">Child elements</span></span>

|<span data-ttu-id="58f5a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="58f5a-124">**Element**</span></span>|<span data-ttu-id="58f5a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58f5a-125">**Type**</span></span>|<span data-ttu-id="58f5a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58f5a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58f5a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="58f5a-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="58f5a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="58f5a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="58f5a-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="58f5a-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="58f5a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="58f5a-130">Attributes</span></span>

|<span data-ttu-id="58f5a-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="58f5a-131">**Attribute**</span></span>|<span data-ttu-id="58f5a-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58f5a-132">**Type**</span></span>|<span data-ttu-id="58f5a-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="58f5a-133">**Required**</span></span>|<span data-ttu-id="58f5a-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58f5a-134">**Description**</span></span>|<span data-ttu-id="58f5a-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="58f5a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58f5a-136">Del</span><span class="sxs-lookup"><span data-stu-id="58f5a-136">Del</span></span>  <br/> |<span data-ttu-id="58f5a-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="58f5a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58f5a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="58f5a-138">optional</span></span>  <br/> |<span data-ttu-id="58f5a-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="58f5a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="58f5a-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="58f5a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58f5a-141">IX</span><span class="sxs-lookup"><span data-stu-id="58f5a-141">IX</span></span>  <br/> |<span data-ttu-id="58f5a-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="58f5a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58f5a-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="58f5a-143">optional</span></span>  <br/> |<span data-ttu-id="58f5a-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="58f5a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="58f5a-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="58f5a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="58f5a-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="58f5a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="58f5a-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="58f5a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58f5a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="58f5a-148">LocalName</span></span>  <br/> |<span data-ttu-id="58f5a-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="58f5a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="58f5a-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="58f5a-150">optional</span></span>  <br/> |<span data-ttu-id="58f5a-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="58f5a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="58f5a-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="58f5a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58f5a-153">N</span><span class="sxs-lookup"><span data-stu-id="58f5a-153">N</span></span>  <br/> |<span data-ttu-id="58f5a-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="58f5a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="58f5a-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="58f5a-155">optional</span></span>  <br/> |<span data-ttu-id="58f5a-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="58f5a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="58f5a-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="58f5a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="58f5a-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="58f5a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58f5a-159">Д</span><span class="sxs-lookup"><span data-stu-id="58f5a-159">T</span></span>  <br/> |<span data-ttu-id="58f5a-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="58f5a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="58f5a-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="58f5a-161">optional</span></span>  <br/> |<span data-ttu-id="58f5a-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="58f5a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="58f5a-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="58f5a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="58f5a-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="58f5a-164">Values of the xsd:string type.</span></span>  <br/> |
   

