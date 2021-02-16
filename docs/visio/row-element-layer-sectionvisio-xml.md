---
title: Элемент Row (Layer Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие один уровень и его свойства для страницы.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540865"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="85e22-103">Элемент Row (Layer Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="85e22-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="85e22-104">Содержит элементы, определяющие один уровень и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="85e22-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85e22-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="85e22-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85e22-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="85e22-106">**Element type**</span></span> <br/> |[<span data-ttu-id="85e22-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="85e22-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="85e22-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="85e22-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="85e22-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="85e22-109">**Schema file**</span></span> <br/> |<span data-ttu-id="85e22-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="85e22-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="85e22-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="85e22-111">**Document parts**</span></span> <br/> |<span data-ttu-id="85e22-112">masters.xml, pages.xml</span><span class="sxs-lookup"><span data-stu-id="85e22-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85e22-113">Определение</span><span class="sxs-lookup"><span data-stu-id="85e22-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85e22-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="85e22-114">Elements and attributes</span></span>

<span data-ttu-id="85e22-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="85e22-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="85e22-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="85e22-116">Parent elements</span></span>

|<span data-ttu-id="85e22-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="85e22-117">**Element**</span></span>|<span data-ttu-id="85e22-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="85e22-118">**Type**</span></span>|<span data-ttu-id="85e22-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85e22-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85e22-120">Section</span><span class="sxs-lookup"><span data-stu-id="85e22-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85e22-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="85e22-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85e22-122">Содержит элементы, определяющие один уровень и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="85e22-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85e22-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="85e22-123">Child elements</span></span>

|<span data-ttu-id="85e22-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="85e22-124">**Element**</span></span>|<span data-ttu-id="85e22-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="85e22-125">**Type**</span></span>|<span data-ttu-id="85e22-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85e22-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85e22-127">Cell</span><span class="sxs-lookup"><span data-stu-id="85e22-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="85e22-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="85e22-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="85e22-129">Указывает одно свойство для уровня или его свойств для страницы.</span><span class="sxs-lookup"><span data-stu-id="85e22-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="85e22-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="85e22-130">Attributes</span></span>

|<span data-ttu-id="85e22-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="85e22-131">**Attribute**</span></span>|<span data-ttu-id="85e22-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="85e22-132">**Type**</span></span>|<span data-ttu-id="85e22-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="85e22-133">**Required**</span></span>|<span data-ttu-id="85e22-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85e22-134">**Description**</span></span>|<span data-ttu-id="85e22-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="85e22-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85e22-136">Del</span><span class="sxs-lookup"><span data-stu-id="85e22-136">Del</span></span>  <br/> |<span data-ttu-id="85e22-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="85e22-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85e22-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="85e22-138">optional</span></span>  <br/> |<span data-ttu-id="85e22-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="85e22-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="85e22-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="85e22-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="85e22-141">IX</span><span class="sxs-lookup"><span data-stu-id="85e22-141">IX</span></span>  <br/> |<span data-ttu-id="85e22-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85e22-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85e22-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="85e22-143">optional</span></span>  <br/> |<span data-ttu-id="85e22-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="85e22-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="85e22-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="85e22-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="85e22-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="85e22-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="85e22-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85e22-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85e22-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="85e22-148">LocalName</span></span>  <br/> |<span data-ttu-id="85e22-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85e22-149">xsd:string</span></span>  <br/> |<span data-ttu-id="85e22-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="85e22-150">optional</span></span>  <br/> |<span data-ttu-id="85e22-151">Указывает уникальное зависимое от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="85e22-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="85e22-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85e22-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85e22-153">N</span><span class="sxs-lookup"><span data-stu-id="85e22-153">N</span></span>  <br/> |<span data-ttu-id="85e22-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85e22-154">xsd:string</span></span>  <br/> |<span data-ttu-id="85e22-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="85e22-155">optional</span></span>  <br/> |<span data-ttu-id="85e22-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="85e22-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="85e22-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="85e22-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="85e22-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85e22-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85e22-159">T</span><span class="sxs-lookup"><span data-stu-id="85e22-159">T</span></span>  <br/> |<span data-ttu-id="85e22-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="85e22-160">xsd:string</span></span>  <br/> |<span data-ttu-id="85e22-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="85e22-161">optional</span></span>  <br/> |<span data-ttu-id="85e22-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="85e22-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="85e22-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="85e22-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="85e22-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="85e22-164">Values of the xsd:string type.</span></span>  <br/> |
   

