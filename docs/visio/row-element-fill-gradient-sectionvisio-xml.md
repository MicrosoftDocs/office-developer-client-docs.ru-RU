---
title: Элемент Row (Fill Gradient Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538622"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="c65ed-103">Элемент Row (Fill Gradient Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c65ed-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="c65ed-104">Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.</span><span class="sxs-lookup"><span data-stu-id="c65ed-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c65ed-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c65ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c65ed-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c65ed-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c65ed-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="c65ed-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c65ed-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c65ed-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c65ed-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c65ed-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c65ed-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c65ed-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c65ed-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c65ed-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c65ed-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c65ed-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c65ed-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c65ed-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c65ed-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c65ed-114">Elements and attributes</span></span>

<span data-ttu-id="c65ed-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c65ed-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c65ed-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c65ed-116">Parent elements</span></span>

|<span data-ttu-id="c65ed-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c65ed-117">**Element**</span></span>|<span data-ttu-id="c65ed-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c65ed-118">**Type**</span></span>|<span data-ttu-id="c65ed-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c65ed-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c65ed-120">Section</span><span class="sxs-lookup"><span data-stu-id="c65ed-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c65ed-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c65ed-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c65ed-122">Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.</span><span class="sxs-lookup"><span data-stu-id="c65ed-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c65ed-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c65ed-123">Child elements</span></span>

|<span data-ttu-id="c65ed-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c65ed-124">**Element**</span></span>|<span data-ttu-id="c65ed-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c65ed-125">**Type**</span></span>|<span data-ttu-id="c65ed-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c65ed-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c65ed-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c65ed-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c65ed-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c65ed-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c65ed-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="c65ed-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c65ed-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c65ed-130">Attributes</span></span>

|<span data-ttu-id="c65ed-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c65ed-131">**Attribute**</span></span>|<span data-ttu-id="c65ed-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c65ed-132">**Type**</span></span>|<span data-ttu-id="c65ed-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c65ed-133">**Required**</span></span>|<span data-ttu-id="c65ed-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c65ed-134">**Description**</span></span>|<span data-ttu-id="c65ed-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c65ed-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c65ed-136">Del</span><span class="sxs-lookup"><span data-stu-id="c65ed-136">Del</span></span>  <br/> |<span data-ttu-id="c65ed-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c65ed-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c65ed-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c65ed-138">optional</span></span>  <br/> |<span data-ttu-id="c65ed-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="c65ed-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c65ed-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c65ed-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c65ed-141">IX</span><span class="sxs-lookup"><span data-stu-id="c65ed-141">IX</span></span>  <br/> |<span data-ttu-id="c65ed-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c65ed-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c65ed-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="c65ed-143">optional</span></span>  <br/> |<span data-ttu-id="c65ed-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="c65ed-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c65ed-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="c65ed-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c65ed-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c65ed-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c65ed-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c65ed-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c65ed-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c65ed-148">LocalName</span></span>  <br/> |<span data-ttu-id="c65ed-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c65ed-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c65ed-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="c65ed-150">optional</span></span>  <br/> |<span data-ttu-id="c65ed-151">Указывает уникальное зависимое от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="c65ed-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c65ed-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c65ed-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c65ed-153">N</span><span class="sxs-lookup"><span data-stu-id="c65ed-153">N</span></span>  <br/> |<span data-ttu-id="c65ed-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c65ed-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c65ed-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="c65ed-155">optional</span></span>  <br/> |<span data-ttu-id="c65ed-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="c65ed-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c65ed-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c65ed-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c65ed-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c65ed-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c65ed-159">T</span><span class="sxs-lookup"><span data-stu-id="c65ed-159">T</span></span>  <br/> |<span data-ttu-id="c65ed-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c65ed-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c65ed-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="c65ed-161">optional</span></span>  <br/> |<span data-ttu-id="c65ed-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="c65ed-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c65ed-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="c65ed-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c65ed-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c65ed-164">Values of the xsd:string type.</span></span>  <br/> |
   

