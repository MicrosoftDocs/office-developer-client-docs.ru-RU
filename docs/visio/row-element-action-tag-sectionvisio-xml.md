---
title: Элемент Row (раздел "теги действий") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Определяет тег действия на фигуре или странице.
ms.openlocfilehash: 1ecdb256fbde4a667ade747c2c7216cd0d248fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358438"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="95590-103">Элемент Row (раздел "теги действий") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="95590-103">Row element (Action Tag Section) ('Visio XML')</span></span>

<span data-ttu-id="95590-104">Определяет тег действия на фигуре или странице.</span><span class="sxs-lookup"><span data-stu-id="95590-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95590-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="95590-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95590-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="95590-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95590-107">Актионтагров_типе</span><span class="sxs-lookup"><span data-stu-id="95590-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95590-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="95590-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95590-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="95590-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95590-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="95590-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95590-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="95590-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95590-112">Master. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="95590-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95590-113">Определение</span><span class="sxs-lookup"><span data-stu-id="95590-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95590-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="95590-114">Elements and attributes</span></span>

<span data-ttu-id="95590-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="95590-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95590-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95590-116">Parent elements</span></span>

|<span data-ttu-id="95590-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="95590-117">**Element**</span></span>|<span data-ttu-id="95590-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95590-118">**Type**</span></span>|<span data-ttu-id="95590-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95590-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95590-120">Section</span><span class="sxs-lookup"><span data-stu-id="95590-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95590-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="95590-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95590-122">Определяет тег действия на фигуре или странице.</span><span class="sxs-lookup"><span data-stu-id="95590-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95590-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95590-123">Child elements</span></span>

|<span data-ttu-id="95590-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="95590-124">**Element**</span></span>|<span data-ttu-id="95590-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95590-125">**Type**</span></span>|<span data-ttu-id="95590-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95590-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95590-127">Cell</span><span class="sxs-lookup"><span data-stu-id="95590-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="95590-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="95590-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95590-129">Определяет одно свойство для тега действия на фигуре или странице.</span><span class="sxs-lookup"><span data-stu-id="95590-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95590-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95590-130">Attributes</span></span>

|<span data-ttu-id="95590-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="95590-131">**Attribute**</span></span>|<span data-ttu-id="95590-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95590-132">**Type**</span></span>|<span data-ttu-id="95590-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="95590-133">**Required**</span></span>|<span data-ttu-id="95590-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95590-134">**Description**</span></span>|<span data-ttu-id="95590-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="95590-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95590-136">Del</span><span class="sxs-lookup"><span data-stu-id="95590-136">Del</span></span>  <br/> |<span data-ttu-id="95590-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="95590-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="95590-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="95590-138">optional</span></span>  <br/> |<span data-ttu-id="95590-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="95590-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="95590-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="95590-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="95590-141">IX</span><span class="sxs-lookup"><span data-stu-id="95590-141">IX</span></span>  <br/> |<span data-ttu-id="95590-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="95590-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95590-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="95590-143">optional</span></span>  <br/> |<span data-ttu-id="95590-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="95590-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="95590-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="95590-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="95590-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="95590-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="95590-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="95590-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="95590-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="95590-148">LocalName</span></span>  <br/> |<span data-ttu-id="95590-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="95590-149">xsd:string</span></span>  <br/> |<span data-ttu-id="95590-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="95590-150">optional</span></span>  <br/> |<span data-ttu-id="95590-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="95590-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="95590-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="95590-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95590-153">N</span><span class="sxs-lookup"><span data-stu-id="95590-153">N</span></span>  <br/> |<span data-ttu-id="95590-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="95590-154">xsd:string</span></span>  <br/> |<span data-ttu-id="95590-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="95590-155">optional</span></span>  <br/> |<span data-ttu-id="95590-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="95590-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="95590-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="95590-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="95590-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="95590-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95590-159">Д</span><span class="sxs-lookup"><span data-stu-id="95590-159">T</span></span>  <br/> |<span data-ttu-id="95590-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="95590-160">xsd:string</span></span>  <br/> |<span data-ttu-id="95590-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="95590-161">optional</span></span>  <br/> |<span data-ttu-id="95590-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="95590-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="95590-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="95590-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="95590-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="95590-164">Values of the xsd:string type.</span></span>  <br/> |
   

