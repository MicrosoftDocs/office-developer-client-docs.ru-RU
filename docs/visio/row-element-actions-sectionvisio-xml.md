---
title: Элемент Row (раздел "действия") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Содержит строки, описывающие пункты меню в контекстном меню или меню тегов действий фигуры или страницы.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2019
ms.locfileid: "32356422"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="df821-103">Элемент Row (раздел "действия") ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="df821-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="df821-104">Содержит строки, описывающие пункты меню в контекстном меню или меню тегов действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="df821-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df821-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="df821-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df821-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="df821-106">**Element type**</span></span> <br/> |[<span data-ttu-id="df821-107">Актионсров_типе</span><span class="sxs-lookup"><span data-stu-id="df821-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df821-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="df821-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df821-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="df821-109">**Schema file**</span></span> <br/> |<span data-ttu-id="df821-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="df821-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df821-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="df821-111">**Document parts**</span></span> <br/> |<span data-ttu-id="df821-112">Master. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="df821-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df821-113">Определение</span><span class="sxs-lookup"><span data-stu-id="df821-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df821-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="df821-114">Elements and attributes</span></span>

<span data-ttu-id="df821-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="df821-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df821-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="df821-116">Parent elements</span></span>

|<span data-ttu-id="df821-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="df821-117">**Element**</span></span>|<span data-ttu-id="df821-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df821-118">**Type**</span></span>|<span data-ttu-id="df821-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df821-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df821-120">Section</span><span class="sxs-lookup"><span data-stu-id="df821-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df821-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="df821-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df821-122">Содержит строки, описывающие пункты меню в контекстном меню или меню тегов действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="df821-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df821-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="df821-123">Child elements</span></span>

|<span data-ttu-id="df821-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="df821-124">**Element**</span></span>|<span data-ttu-id="df821-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df821-125">**Type**</span></span>|<span data-ttu-id="df821-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df821-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df821-127">Cell</span><span class="sxs-lookup"><span data-stu-id="df821-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="df821-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="df821-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df821-129">Задает одно свойство действия, связанного с настраиваемой командой, в контекстном меню или меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="df821-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="df821-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="df821-130">Attributes</span></span>

|<span data-ttu-id="df821-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="df821-131">**Attribute**</span></span>|<span data-ttu-id="df821-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df821-132">**Type**</span></span>|<span data-ttu-id="df821-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="df821-133">**Required**</span></span>|<span data-ttu-id="df821-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df821-134">**Description**</span></span>|<span data-ttu-id="df821-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="df821-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df821-136">Del</span><span class="sxs-lookup"><span data-stu-id="df821-136">Del</span></span>  <br/> |<span data-ttu-id="df821-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="df821-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="df821-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="df821-138">optional</span></span>  <br/> |<span data-ttu-id="df821-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="df821-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="df821-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="df821-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="df821-141">IX</span><span class="sxs-lookup"><span data-stu-id="df821-141">IX</span></span>  <br/> |<span data-ttu-id="df821-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="df821-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="df821-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="df821-143">optional</span></span>  <br/> |<span data-ttu-id="df821-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="df821-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="df821-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="df821-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="df821-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="df821-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="df821-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="df821-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="df821-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="df821-148">LocalName</span></span>  <br/> |<span data-ttu-id="df821-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="df821-149">xsd:string</span></span>  <br/> |<span data-ttu-id="df821-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="df821-150">optional</span></span>  <br/> |<span data-ttu-id="df821-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="df821-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="df821-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="df821-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="df821-153">N</span><span class="sxs-lookup"><span data-stu-id="df821-153">N</span></span>  <br/> |<span data-ttu-id="df821-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="df821-154">xsd:string</span></span>  <br/> |<span data-ttu-id="df821-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="df821-155">optional</span></span>  <br/> |<span data-ttu-id="df821-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="df821-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="df821-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="df821-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="df821-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="df821-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="df821-159">Д</span><span class="sxs-lookup"><span data-stu-id="df821-159">T</span></span>  <br/> |<span data-ttu-id="df821-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="df821-160">xsd:string</span></span>  <br/> |<span data-ttu-id="df821-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="df821-161">optional</span></span>  <br/> |<span data-ttu-id="df821-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="df821-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="df821-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="df821-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="df821-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="df821-164">Values of the xsd:string type.</span></span>  <br/> |
   

