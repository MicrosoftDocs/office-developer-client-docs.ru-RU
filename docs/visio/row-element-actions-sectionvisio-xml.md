---
title: Элемент Row (Actions Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Содержит строки с описанием элементов меню в ярлыке или меню тегов действий фигуры или страницы.
ms.openlocfilehash: dfe23aa7d635fc09d625c414e5548a0166384fbb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540415"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="ace5c-103">Элемент Row (Actions Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ace5c-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="ace5c-104">Содержит строки с описанием элементов меню в ярлыке или меню тегов действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="ace5c-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ace5c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ace5c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ace5c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ace5c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ace5c-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="ace5c-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ace5c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ace5c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ace5c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ace5c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ace5c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ace5c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ace5c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ace5c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ace5c-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="ace5c-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ace5c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ace5c-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ace5c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ace5c-114">Elements and attributes</span></span>

<span data-ttu-id="ace5c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ace5c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ace5c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ace5c-116">Parent elements</span></span>

|<span data-ttu-id="ace5c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ace5c-117">**Element**</span></span>|<span data-ttu-id="ace5c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace5c-118">**Type**</span></span>|<span data-ttu-id="ace5c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace5c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ace5c-120">Section</span><span class="sxs-lookup"><span data-stu-id="ace5c-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ace5c-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ace5c-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ace5c-122">Содержит строки с описанием элементов меню в ярлыке или меню тегов действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="ace5c-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ace5c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ace5c-123">Child elements</span></span>

|<span data-ttu-id="ace5c-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ace5c-124">**Element**</span></span>|<span data-ttu-id="ace5c-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace5c-125">**Type**</span></span>|<span data-ttu-id="ace5c-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace5c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ace5c-127">Cell</span><span class="sxs-lookup"><span data-stu-id="ace5c-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="ace5c-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ace5c-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ace5c-129">Указывает одно свойство действия, связанное с настраиваемой командой в меню ярлыка или тега действия.</span><span class="sxs-lookup"><span data-stu-id="ace5c-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ace5c-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ace5c-130">Attributes</span></span>

|<span data-ttu-id="ace5c-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ace5c-131">**Attribute**</span></span>|<span data-ttu-id="ace5c-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ace5c-132">**Type**</span></span>|<span data-ttu-id="ace5c-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ace5c-133">**Required**</span></span>|<span data-ttu-id="ace5c-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ace5c-134">**Description**</span></span>|<span data-ttu-id="ace5c-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ace5c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ace5c-136">Del</span><span class="sxs-lookup"><span data-stu-id="ace5c-136">Del</span></span>  <br/> |<span data-ttu-id="ace5c-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ace5c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ace5c-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace5c-138">optional</span></span>  <br/> |<span data-ttu-id="ace5c-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="ace5c-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="ace5c-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ace5c-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ace5c-141">IX</span><span class="sxs-lookup"><span data-stu-id="ace5c-141">IX</span></span>  <br/> |<span data-ttu-id="ace5c-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ace5c-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ace5c-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace5c-143">optional</span></span>  <br/> |<span data-ttu-id="ace5c-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="ace5c-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="ace5c-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="ace5c-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="ace5c-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ace5c-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ace5c-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ace5c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ace5c-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="ace5c-148">LocalName</span></span>  <br/> |<span data-ttu-id="ace5c-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ace5c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ace5c-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace5c-150">optional</span></span>  <br/> |<span data-ttu-id="ace5c-151">Указывает уникальное имя строки, зависимое от языка.</span><span class="sxs-lookup"><span data-stu-id="ace5c-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="ace5c-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace5c-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ace5c-153">N</span><span class="sxs-lookup"><span data-stu-id="ace5c-153">N</span></span>  <br/> |<span data-ttu-id="ace5c-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ace5c-154">xsd:string</span></span>  <br/> |<span data-ttu-id="ace5c-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace5c-155">optional</span></span>  <br/> |<span data-ttu-id="ace5c-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="ace5c-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="ace5c-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="ace5c-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="ace5c-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace5c-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ace5c-159">T</span><span class="sxs-lookup"><span data-stu-id="ace5c-159">T</span></span>  <br/> |<span data-ttu-id="ace5c-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ace5c-160">xsd:string</span></span>  <br/> |<span data-ttu-id="ace5c-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="ace5c-161">optional</span></span>  <br/> |<span data-ttu-id="ace5c-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="ace5c-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="ace5c-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="ace5c-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="ace5c-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ace5c-164">Values of the xsd:string type.</span></span>  <br/> |
   

