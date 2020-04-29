---
title: Элемент Row (раздел "слой") (XML-файл Visio)
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
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="547de-103">Элемент Row (раздел "слой") (XML-файл Visio)</span><span class="sxs-lookup"><span data-stu-id="547de-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="547de-104">Содержит элементы, определяющие один слой и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="547de-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="547de-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="547de-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="547de-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="547de-106">**Element type**</span></span> <br/> |[<span data-ttu-id="547de-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="547de-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="547de-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="547de-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="547de-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="547de-109">**Schema file**</span></span> <br/> |<span data-ttu-id="547de-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="547de-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="547de-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="547de-111">**Document parts**</span></span> <br/> |<span data-ttu-id="547de-112">файлы хозяев. XML, Pages. XML</span><span class="sxs-lookup"><span data-stu-id="547de-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="547de-113">Определение</span><span class="sxs-lookup"><span data-stu-id="547de-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="547de-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="547de-114">Elements and attributes</span></span>

<span data-ttu-id="547de-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="547de-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="547de-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="547de-116">Parent elements</span></span>

|<span data-ttu-id="547de-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="547de-117">**Element**</span></span>|<span data-ttu-id="547de-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="547de-118">**Type**</span></span>|<span data-ttu-id="547de-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="547de-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="547de-120">Section</span><span class="sxs-lookup"><span data-stu-id="547de-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="547de-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="547de-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="547de-122">Содержит элементы, определяющие один слой и его свойства для страницы.</span><span class="sxs-lookup"><span data-stu-id="547de-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="547de-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="547de-123">Child elements</span></span>

|<span data-ttu-id="547de-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="547de-124">**Element**</span></span>|<span data-ttu-id="547de-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="547de-125">**Type**</span></span>|<span data-ttu-id="547de-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="547de-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="547de-127">Cell</span><span class="sxs-lookup"><span data-stu-id="547de-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="547de-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="547de-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="547de-129">Задает одно свойство для слоя или его свойств для страницы.</span><span class="sxs-lookup"><span data-stu-id="547de-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="547de-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="547de-130">Attributes</span></span>

|<span data-ttu-id="547de-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="547de-131">**Attribute**</span></span>|<span data-ttu-id="547de-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="547de-132">**Type**</span></span>|<span data-ttu-id="547de-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="547de-133">**Required**</span></span>|<span data-ttu-id="547de-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="547de-134">**Description**</span></span>|<span data-ttu-id="547de-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="547de-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="547de-136">Del</span><span class="sxs-lookup"><span data-stu-id="547de-136">Del</span></span>  <br/> |<span data-ttu-id="547de-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="547de-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="547de-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="547de-138">optional</span></span>  <br/> |<span data-ttu-id="547de-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="547de-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="547de-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="547de-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="547de-141">IX</span><span class="sxs-lookup"><span data-stu-id="547de-141">IX</span></span>  <br/> |<span data-ttu-id="547de-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="547de-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="547de-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="547de-143">optional</span></span>  <br/> |<span data-ttu-id="547de-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="547de-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="547de-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="547de-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="547de-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="547de-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="547de-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="547de-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="547de-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="547de-148">LocalName</span></span>  <br/> |<span data-ttu-id="547de-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="547de-149">xsd:string</span></span>  <br/> |<span data-ttu-id="547de-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="547de-150">optional</span></span>  <br/> |<span data-ttu-id="547de-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="547de-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="547de-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="547de-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="547de-153">N</span><span class="sxs-lookup"><span data-stu-id="547de-153">N</span></span>  <br/> |<span data-ttu-id="547de-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="547de-154">xsd:string</span></span>  <br/> |<span data-ttu-id="547de-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="547de-155">optional</span></span>  <br/> |<span data-ttu-id="547de-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="547de-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="547de-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="547de-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="547de-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="547de-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="547de-159">Д</span><span class="sxs-lookup"><span data-stu-id="547de-159">T</span></span>  <br/> |<span data-ttu-id="547de-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="547de-160">xsd:string</span></span>  <br/> |<span data-ttu-id="547de-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="547de-161">optional</span></span>  <br/> |<span data-ttu-id="547de-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="547de-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="547de-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="547de-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="547de-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="547de-164">Values of the xsd:string type.</span></span>  <br/> |
   

