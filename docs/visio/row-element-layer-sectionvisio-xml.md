---
title: Элемент Row (Раздел layer) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: Содержит элементы, определяющие один слой и его свойства для страницы.
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540865"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="c00b8-103">Элемент Row (Раздел layer) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c00b8-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="c00b8-104">Содержит элементы, определяющие один слой и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="c00b8-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c00b8-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c00b8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c00b8-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c00b8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c00b8-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="c00b8-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c00b8-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c00b8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c00b8-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c00b8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c00b8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c00b8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c00b8-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c00b8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c00b8-112">masters.xml, pages.xml</span><span class="sxs-lookup"><span data-stu-id="c00b8-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c00b8-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c00b8-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c00b8-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c00b8-114">Elements and attributes</span></span>

<span data-ttu-id="c00b8-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c00b8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c00b8-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c00b8-116">Parent elements</span></span>

|<span data-ttu-id="c00b8-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c00b8-117">**Element**</span></span>|<span data-ttu-id="c00b8-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c00b8-118">**Type**</span></span>|<span data-ttu-id="c00b8-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c00b8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c00b8-120">Section</span><span class="sxs-lookup"><span data-stu-id="c00b8-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c00b8-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c00b8-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c00b8-122">Содержит элементы, определяющие один слой и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="c00b8-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c00b8-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c00b8-123">Child elements</span></span>

|<span data-ttu-id="c00b8-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c00b8-124">**Element**</span></span>|<span data-ttu-id="c00b8-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c00b8-125">**Type**</span></span>|<span data-ttu-id="c00b8-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c00b8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c00b8-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c00b8-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c00b8-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c00b8-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c00b8-129">Указывает одно свойство для слоя или его свойств для страницы.</span><span class="sxs-lookup"><span data-stu-id="c00b8-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c00b8-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c00b8-130">Attributes</span></span>

|<span data-ttu-id="c00b8-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c00b8-131">**Attribute**</span></span>|<span data-ttu-id="c00b8-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c00b8-132">**Type**</span></span>|<span data-ttu-id="c00b8-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c00b8-133">**Required**</span></span>|<span data-ttu-id="c00b8-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c00b8-134">**Description**</span></span>|<span data-ttu-id="c00b8-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c00b8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c00b8-136">Del</span><span class="sxs-lookup"><span data-stu-id="c00b8-136">Del</span></span>  <br/> |<span data-ttu-id="c00b8-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c00b8-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c00b8-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c00b8-138">optional</span></span>  <br/> |<span data-ttu-id="c00b8-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="c00b8-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c00b8-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c00b8-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c00b8-141">IX</span><span class="sxs-lookup"><span data-stu-id="c00b8-141">IX</span></span>  <br/> |<span data-ttu-id="c00b8-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c00b8-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c00b8-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="c00b8-143">optional</span></span>  <br/> |<span data-ttu-id="c00b8-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="c00b8-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c00b8-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="c00b8-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c00b8-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c00b8-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c00b8-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c00b8-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c00b8-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c00b8-148">LocalName</span></span>  <br/> |<span data-ttu-id="c00b8-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c00b8-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c00b8-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="c00b8-150">optional</span></span>  <br/> |<span data-ttu-id="c00b8-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="c00b8-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c00b8-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c00b8-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c00b8-153">Нет</span><span class="sxs-lookup"><span data-stu-id="c00b8-153">N</span></span>  <br/> |<span data-ttu-id="c00b8-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c00b8-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c00b8-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="c00b8-155">optional</span></span>  <br/> |<span data-ttu-id="c00b8-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c00b8-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c00b8-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c00b8-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c00b8-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c00b8-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c00b8-159">T</span><span class="sxs-lookup"><span data-stu-id="c00b8-159">T</span></span>  <br/> |<span data-ttu-id="c00b8-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c00b8-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c00b8-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="c00b8-161">optional</span></span>  <br/> |<span data-ttu-id="c00b8-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="c00b8-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c00b8-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="c00b8-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c00b8-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c00b8-164">Values of the xsd:string type.</span></span>  <br/> |
   

