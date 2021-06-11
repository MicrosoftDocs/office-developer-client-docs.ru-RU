---
title: Элемент Row (Раздел Действия) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Содержит строки, описывая элементы меню в меню ярлыка или тега действий фигуры или страницы.
ms.openlocfilehash: dfe23aa7d635fc09d625c414e5548a0166384fbb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540415"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="5daa0-103">Элемент Row (Раздел Действия) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5daa0-103">Row element (Actions Section) (Visio XML)</span></span>

<span data-ttu-id="5daa0-104">Содержит строки, описывая элементы меню в меню ярлыка или тега действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="5daa0-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5daa0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5daa0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5daa0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5daa0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5daa0-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="5daa0-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5daa0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5daa0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5daa0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5daa0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5daa0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5daa0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5daa0-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="5daa0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5daa0-112">masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="5daa0-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5daa0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5daa0-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5daa0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5daa0-114">Elements and attributes</span></span>

<span data-ttu-id="5daa0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5daa0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5daa0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5daa0-116">Parent elements</span></span>

|<span data-ttu-id="5daa0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5daa0-117">**Element**</span></span>|<span data-ttu-id="5daa0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5daa0-118">**Type**</span></span>|<span data-ttu-id="5daa0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5daa0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5daa0-120">Section</span><span class="sxs-lookup"><span data-stu-id="5daa0-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5daa0-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5daa0-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5daa0-122">Содержит строки, описывая элементы меню в меню ярлыка или тега действий фигуры или страницы.</span><span class="sxs-lookup"><span data-stu-id="5daa0-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5daa0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5daa0-123">Child elements</span></span>

|<span data-ttu-id="5daa0-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5daa0-124">**Element**</span></span>|<span data-ttu-id="5daa0-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5daa0-125">**Type**</span></span>|<span data-ttu-id="5daa0-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5daa0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5daa0-127">Cell</span><span class="sxs-lookup"><span data-stu-id="5daa0-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="5daa0-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5daa0-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5daa0-129">Указывает одно свойство действия, связанного с настраиваемой командой в меню ярлыка или тега действий.</span><span class="sxs-lookup"><span data-stu-id="5daa0-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5daa0-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5daa0-130">Attributes</span></span>

|<span data-ttu-id="5daa0-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5daa0-131">**Attribute**</span></span>|<span data-ttu-id="5daa0-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5daa0-132">**Type**</span></span>|<span data-ttu-id="5daa0-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5daa0-133">**Required**</span></span>|<span data-ttu-id="5daa0-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5daa0-134">**Description**</span></span>|<span data-ttu-id="5daa0-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5daa0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5daa0-136">Del</span><span class="sxs-lookup"><span data-stu-id="5daa0-136">Del</span></span>  <br/> |<span data-ttu-id="5daa0-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5daa0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5daa0-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="5daa0-138">optional</span></span>  <br/> |<span data-ttu-id="5daa0-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="5daa0-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="5daa0-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5daa0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5daa0-141">IX</span><span class="sxs-lookup"><span data-stu-id="5daa0-141">IX</span></span>  <br/> |<span data-ttu-id="5daa0-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5daa0-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5daa0-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="5daa0-143">optional</span></span>  <br/> |<span data-ttu-id="5daa0-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="5daa0-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="5daa0-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="5daa0-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="5daa0-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="5daa0-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5daa0-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5daa0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5daa0-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="5daa0-148">LocalName</span></span>  <br/> |<span data-ttu-id="5daa0-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5daa0-149">xsd:string</span></span>  <br/> |<span data-ttu-id="5daa0-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="5daa0-150">optional</span></span>  <br/> |<span data-ttu-id="5daa0-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="5daa0-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="5daa0-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5daa0-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5daa0-153">Нет</span><span class="sxs-lookup"><span data-stu-id="5daa0-153">N</span></span>  <br/> |<span data-ttu-id="5daa0-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5daa0-154">xsd:string</span></span>  <br/> |<span data-ttu-id="5daa0-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="5daa0-155">optional</span></span>  <br/> |<span data-ttu-id="5daa0-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="5daa0-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="5daa0-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="5daa0-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="5daa0-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5daa0-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5daa0-159">T</span><span class="sxs-lookup"><span data-stu-id="5daa0-159">T</span></span>  <br/> |<span data-ttu-id="5daa0-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5daa0-160">xsd:string</span></span>  <br/> |<span data-ttu-id="5daa0-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="5daa0-161">optional</span></span>  <br/> |<span data-ttu-id="5daa0-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="5daa0-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="5daa0-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="5daa0-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="5daa0-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5daa0-164">Values of the xsd:string type.</span></span>  <br/> |
   

