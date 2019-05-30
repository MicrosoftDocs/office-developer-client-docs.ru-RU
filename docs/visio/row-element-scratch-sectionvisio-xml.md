---
title: Элемент Row (раздел "вспомогательный") (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.
ms.openlocfilehash: fb346785b9cb6539d970ae1bd1c44fc706bd657d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541003"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="4f311-103">Элемент Row (раздел "вспомогательный") (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4f311-103">Row element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="4f311-104">Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.</span><span class="sxs-lookup"><span data-stu-id="4f311-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f311-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4f311-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f311-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4f311-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f311-107">Скратчров_типе</span><span class="sxs-lookup"><span data-stu-id="4f311-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f311-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4f311-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f311-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4f311-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f311-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4f311-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f311-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4f311-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4f311-112">Document. XML, Master. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="4f311-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f311-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4f311-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f311-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f311-114">Elements and attributes</span></span>

<span data-ttu-id="4f311-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4f311-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f311-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4f311-116">Parent elements</span></span>

|<span data-ttu-id="4f311-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4f311-117">**Element**</span></span>|<span data-ttu-id="4f311-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f311-118">**Type**</span></span>|<span data-ttu-id="4f311-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f311-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f311-120">Section</span><span class="sxs-lookup"><span data-stu-id="4f311-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f311-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="4f311-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f311-122">Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.</span><span class="sxs-lookup"><span data-stu-id="4f311-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f311-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4f311-123">Child elements</span></span>

|<span data-ttu-id="4f311-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4f311-124">**Element**</span></span>|<span data-ttu-id="4f311-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f311-125">**Type**</span></span>|<span data-ttu-id="4f311-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f311-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f311-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4f311-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4f311-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="4f311-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f311-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="4f311-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f311-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f311-130">Attributes</span></span>

|<span data-ttu-id="4f311-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4f311-131">**Attribute**</span></span>|<span data-ttu-id="4f311-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f311-132">**Type**</span></span>|<span data-ttu-id="4f311-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4f311-133">**Required**</span></span>|<span data-ttu-id="4f311-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f311-134">**Description**</span></span>|<span data-ttu-id="4f311-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4f311-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f311-136">Del</span><span class="sxs-lookup"><span data-stu-id="4f311-136">Del</span></span>  <br/> |<span data-ttu-id="4f311-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4f311-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f311-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f311-138">optional</span></span>  <br/> |<span data-ttu-id="4f311-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="4f311-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="4f311-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4f311-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4f311-141">IX</span><span class="sxs-lookup"><span data-stu-id="4f311-141">IX</span></span>  <br/> |<span data-ttu-id="4f311-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4f311-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f311-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f311-143">optional</span></span>  <br/> |<span data-ttu-id="4f311-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="4f311-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="4f311-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="4f311-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="4f311-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="4f311-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4f311-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4f311-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f311-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="4f311-148">LocalName</span></span>  <br/> |<span data-ttu-id="4f311-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4f311-149">xsd:string</span></span>  <br/> |<span data-ttu-id="4f311-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f311-150">optional</span></span>  <br/> |<span data-ttu-id="4f311-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="4f311-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="4f311-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4f311-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f311-153">N</span><span class="sxs-lookup"><span data-stu-id="4f311-153">N</span></span>  <br/> |<span data-ttu-id="4f311-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4f311-154">xsd:string</span></span>  <br/> |<span data-ttu-id="4f311-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f311-155">optional</span></span>  <br/> |<span data-ttu-id="4f311-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="4f311-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="4f311-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="4f311-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4f311-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4f311-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f311-159">Д</span><span class="sxs-lookup"><span data-stu-id="4f311-159">T</span></span>  <br/> |<span data-ttu-id="4f311-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4f311-160">xsd:string</span></span>  <br/> |<span data-ttu-id="4f311-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f311-161">optional</span></span>  <br/> |<span data-ttu-id="4f311-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="4f311-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="4f311-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="4f311-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="4f311-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4f311-164">Values of the xsd:string type.</span></span>  <br/> |
   

