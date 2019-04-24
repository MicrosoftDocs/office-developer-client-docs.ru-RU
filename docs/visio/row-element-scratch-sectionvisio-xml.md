---
title: Элемент Row (раздел "вспомогательный") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bdbaf263-ae57-2807-f100-8d590ab92927
description: Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.
ms.openlocfilehash: eac975fa1233e74b7bb5f2efc90b6b6edad8215c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342737"
---
# <a name="row-element-scratch-section-visio-xml"></a><span data-ttu-id="29944-103">Элемент Row (раздел "вспомогательный") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="29944-103">Row element (Scratch Section) ('Visio XML')</span></span>

<span data-ttu-id="29944-104">Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.</span><span class="sxs-lookup"><span data-stu-id="29944-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29944-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="29944-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29944-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="29944-106">**Element type**</span></span> <br/> |[<span data-ttu-id="29944-107">Скратчров_типе</span><span class="sxs-lookup"><span data-stu-id="29944-107">ScratchRow_Type</span></span>](scratchrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="29944-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="29944-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="29944-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="29944-109">**Schema file**</span></span> <br/> |<span data-ttu-id="29944-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="29944-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="29944-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="29944-111">**Document parts**</span></span> <br/> |<span data-ttu-id="29944-112">Document. XML, Master. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="29944-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29944-113">Определение</span><span class="sxs-lookup"><span data-stu-id="29944-113">Definition</span></span>

```XML
< xs:element name="Row" type="ScratchRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="29944-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="29944-114">Elements and attributes</span></span>

<span data-ttu-id="29944-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="29944-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="29944-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="29944-116">Parent elements</span></span>

|<span data-ttu-id="29944-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="29944-117">**Element**</span></span>|<span data-ttu-id="29944-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29944-118">**Type**</span></span>|<span data-ttu-id="29944-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29944-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29944-120">Section</span><span class="sxs-lookup"><span data-stu-id="29944-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29944-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="29944-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29944-122">Рабочая область для ввода и тестирования формул, на которые можно ссылаться по другим ячейкам.</span><span class="sxs-lookup"><span data-stu-id="29944-122">A work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29944-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="29944-123">Child elements</span></span>

|<span data-ttu-id="29944-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="29944-124">**Element**</span></span>|<span data-ttu-id="29944-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29944-125">**Type**</span></span>|<span data-ttu-id="29944-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29944-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29944-127">Cell</span><span class="sxs-lookup"><span data-stu-id="29944-127">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="29944-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="29944-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29944-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="29944-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="29944-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="29944-130">Attributes</span></span>

|<span data-ttu-id="29944-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="29944-131">**Attribute**</span></span>|<span data-ttu-id="29944-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29944-132">**Type**</span></span>|<span data-ttu-id="29944-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="29944-133">**Required**</span></span>|<span data-ttu-id="29944-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29944-134">**Description**</span></span>|<span data-ttu-id="29944-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="29944-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29944-136">Del</span><span class="sxs-lookup"><span data-stu-id="29944-136">Del</span></span>  <br/> |<span data-ttu-id="29944-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="29944-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29944-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="29944-138">optional</span></span>  <br/> |<span data-ttu-id="29944-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="29944-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="29944-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="29944-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29944-141">IX</span><span class="sxs-lookup"><span data-stu-id="29944-141">IX</span></span>  <br/> |<span data-ttu-id="29944-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="29944-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29944-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="29944-143">optional</span></span>  <br/> |<span data-ttu-id="29944-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="29944-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="29944-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="29944-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="29944-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="29944-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="29944-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="29944-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29944-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="29944-148">LocalName</span></span>  <br/> |<span data-ttu-id="29944-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="29944-149">xsd:string</span></span>  <br/> |<span data-ttu-id="29944-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="29944-150">optional</span></span>  <br/> |<span data-ttu-id="29944-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="29944-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="29944-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="29944-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29944-153">N</span><span class="sxs-lookup"><span data-stu-id="29944-153">N</span></span>  <br/> |<span data-ttu-id="29944-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="29944-154">xsd:string</span></span>  <br/> |<span data-ttu-id="29944-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="29944-155">optional</span></span>  <br/> |<span data-ttu-id="29944-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="29944-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="29944-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="29944-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="29944-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="29944-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29944-159">Д</span><span class="sxs-lookup"><span data-stu-id="29944-159">T</span></span>  <br/> |<span data-ttu-id="29944-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="29944-160">xsd:string</span></span>  <br/> |<span data-ttu-id="29944-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="29944-161">optional</span></span>  <br/> |<span data-ttu-id="29944-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="29944-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="29944-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="29944-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="29944-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="29944-164">Values of the xsd:string type.</span></span>  <br/> |
   

