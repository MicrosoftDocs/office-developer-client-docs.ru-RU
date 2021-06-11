---
title: Элемент Row (Раздел Градиента строки) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.
ms.openlocfilehash: bfaf3ab8cc16e11051310d7e838b9dddbf7e108d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540828"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="77dcb-103">Элемент Row (Раздел Градиента строки) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="77dcb-103">Row element (Line Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="77dcb-104">Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.</span><span class="sxs-lookup"><span data-stu-id="77dcb-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77dcb-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="77dcb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77dcb-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="77dcb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="77dcb-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="77dcb-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="77dcb-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="77dcb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="77dcb-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="77dcb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="77dcb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="77dcb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="77dcb-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="77dcb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="77dcb-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="77dcb-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77dcb-113">Определение</span><span class="sxs-lookup"><span data-stu-id="77dcb-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="77dcb-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="77dcb-114">Elements and attributes</span></span>

<span data-ttu-id="77dcb-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="77dcb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="77dcb-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="77dcb-116">Parent elements</span></span>

|<span data-ttu-id="77dcb-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="77dcb-117">**Element**</span></span>|<span data-ttu-id="77dcb-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="77dcb-118">**Type**</span></span>|<span data-ttu-id="77dcb-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77dcb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77dcb-120">Section</span><span class="sxs-lookup"><span data-stu-id="77dcb-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="77dcb-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="77dcb-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="77dcb-122">Содержит цвет, прозрачность и расположение остановки градиента для градиента строки.</span><span class="sxs-lookup"><span data-stu-id="77dcb-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="77dcb-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="77dcb-123">Child elements</span></span>

|<span data-ttu-id="77dcb-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="77dcb-124">**Element**</span></span>|<span data-ttu-id="77dcb-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="77dcb-125">**Type**</span></span>|<span data-ttu-id="77dcb-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77dcb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77dcb-127">Cell</span><span class="sxs-lookup"><span data-stu-id="77dcb-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="77dcb-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="77dcb-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="77dcb-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="77dcb-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="77dcb-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="77dcb-130">Attributes</span></span>

|<span data-ttu-id="77dcb-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="77dcb-131">**Attribute**</span></span>|<span data-ttu-id="77dcb-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="77dcb-132">**Type**</span></span>|<span data-ttu-id="77dcb-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="77dcb-133">**Required**</span></span>|<span data-ttu-id="77dcb-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77dcb-134">**Description**</span></span>|<span data-ttu-id="77dcb-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="77dcb-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="77dcb-136">Del</span><span class="sxs-lookup"><span data-stu-id="77dcb-136">Del</span></span>  <br/> |<span data-ttu-id="77dcb-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="77dcb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="77dcb-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="77dcb-138">optional</span></span>  <br/> |<span data-ttu-id="77dcb-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="77dcb-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="77dcb-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="77dcb-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="77dcb-141">IX</span><span class="sxs-lookup"><span data-stu-id="77dcb-141">IX</span></span>  <br/> |<span data-ttu-id="77dcb-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="77dcb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77dcb-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="77dcb-143">optional</span></span>  <br/> |<span data-ttu-id="77dcb-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="77dcb-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="77dcb-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="77dcb-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="77dcb-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="77dcb-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="77dcb-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="77dcb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="77dcb-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="77dcb-148">LocalName</span></span>  <br/> |<span data-ttu-id="77dcb-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="77dcb-149">xsd:string</span></span>  <br/> |<span data-ttu-id="77dcb-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="77dcb-150">optional</span></span>  <br/> |<span data-ttu-id="77dcb-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="77dcb-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="77dcb-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="77dcb-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="77dcb-153">Нет</span><span class="sxs-lookup"><span data-stu-id="77dcb-153">N</span></span>  <br/> |<span data-ttu-id="77dcb-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="77dcb-154">xsd:string</span></span>  <br/> |<span data-ttu-id="77dcb-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="77dcb-155">optional</span></span>  <br/> |<span data-ttu-id="77dcb-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="77dcb-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="77dcb-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="77dcb-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="77dcb-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="77dcb-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="77dcb-159">T</span><span class="sxs-lookup"><span data-stu-id="77dcb-159">T</span></span>  <br/> |<span data-ttu-id="77dcb-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="77dcb-160">xsd:string</span></span>  <br/> |<span data-ttu-id="77dcb-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="77dcb-161">optional</span></span>  <br/> |<span data-ttu-id="77dcb-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="77dcb-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="77dcb-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="77dcb-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="77dcb-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="77dcb-164">Values of the xsd:string type.</span></span>  <br/> |
   

