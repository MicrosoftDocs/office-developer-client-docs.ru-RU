---
title: Элемент Row (Раздел подключения) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: Содержит x- или y-координаты, горизонтальное и вертикальное направление и введите для одной точки подключения на фигуре.
ms.openlocfilehash: eb32030e89d3ac77adfdc64e2d20a5fb954dbb53
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541766"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="78556-103">Элемент Row (Раздел подключения) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="78556-103">Row element (Connection Section) (Visio XML)</span></span>

<span data-ttu-id="78556-104">Содержит x- или y-координаты, горизонтальное и вертикальное направление и введите для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="78556-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78556-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="78556-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78556-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="78556-106">**Element type**</span></span> <br/> |[<span data-ttu-id="78556-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="78556-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="78556-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="78556-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="78556-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="78556-109">**Schema file**</span></span> <br/> |<span data-ttu-id="78556-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="78556-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="78556-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="78556-111">**Document parts**</span></span> <br/> |<span data-ttu-id="78556-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="78556-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78556-113">Определение</span><span class="sxs-lookup"><span data-stu-id="78556-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78556-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="78556-114">Elements and attributes</span></span>

<span data-ttu-id="78556-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="78556-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="78556-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="78556-116">Parent elements</span></span>

|<span data-ttu-id="78556-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="78556-117">**Element**</span></span>|<span data-ttu-id="78556-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="78556-118">**Type**</span></span>|<span data-ttu-id="78556-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78556-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78556-120">Section</span><span class="sxs-lookup"><span data-stu-id="78556-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78556-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="78556-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78556-122">Содержит x- или y-координаты, горизонтальное и вертикальное направление и введите для одной точки подключения на фигуре.</span><span class="sxs-lookup"><span data-stu-id="78556-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="78556-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="78556-123">Child elements</span></span>

|<span data-ttu-id="78556-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="78556-124">**Element**</span></span>|<span data-ttu-id="78556-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="78556-125">**Type**</span></span>|<span data-ttu-id="78556-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78556-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78556-127">Cell</span><span class="sxs-lookup"><span data-stu-id="78556-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="78556-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="78556-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78556-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="78556-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="78556-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="78556-130">Attributes</span></span>

|<span data-ttu-id="78556-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="78556-131">**Attribute**</span></span>|<span data-ttu-id="78556-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="78556-132">**Type**</span></span>|<span data-ttu-id="78556-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="78556-133">**Required**</span></span>|<span data-ttu-id="78556-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78556-134">**Description**</span></span>|<span data-ttu-id="78556-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="78556-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="78556-136">Del</span><span class="sxs-lookup"><span data-stu-id="78556-136">Del</span></span>  <br/> |<span data-ttu-id="78556-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="78556-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="78556-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="78556-138">optional</span></span>  <br/> |<span data-ttu-id="78556-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="78556-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="78556-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="78556-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="78556-141">IX</span><span class="sxs-lookup"><span data-stu-id="78556-141">IX</span></span>  <br/> |<span data-ttu-id="78556-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="78556-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="78556-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="78556-143">optional</span></span>  <br/> |<span data-ttu-id="78556-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="78556-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="78556-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="78556-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="78556-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="78556-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="78556-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="78556-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="78556-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="78556-148">LocalName</span></span>  <br/> |<span data-ttu-id="78556-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="78556-149">xsd:string</span></span>  <br/> |<span data-ttu-id="78556-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="78556-150">optional</span></span>  <br/> |<span data-ttu-id="78556-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="78556-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="78556-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="78556-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="78556-153">Нет</span><span class="sxs-lookup"><span data-stu-id="78556-153">N</span></span>  <br/> |<span data-ttu-id="78556-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="78556-154">xsd:string</span></span>  <br/> |<span data-ttu-id="78556-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="78556-155">optional</span></span>  <br/> |<span data-ttu-id="78556-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="78556-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="78556-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="78556-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="78556-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="78556-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="78556-159">T</span><span class="sxs-lookup"><span data-stu-id="78556-159">T</span></span>  <br/> |<span data-ttu-id="78556-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="78556-160">xsd:string</span></span>  <br/> |<span data-ttu-id="78556-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="78556-161">optional</span></span>  <br/> |<span data-ttu-id="78556-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="78556-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="78556-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="78556-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="78556-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="78556-164">Values of the xsd:string type.</span></span>  <br/> |
   

