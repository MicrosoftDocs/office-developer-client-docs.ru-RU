---
title: Элемент Row (User-defined Cells Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Указанный пользователем фрагмент информации, на который могут ссылаться другие ячейки и средства надстройки.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538174"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="37ad4-103">Элемент Row (User-defined Cells Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="37ad4-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="37ad4-104">Указанный пользователем фрагмент информации, на который могут ссылаться другие ячейки и средства надстройки.</span><span class="sxs-lookup"><span data-stu-id="37ad4-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37ad4-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="37ad4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37ad4-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="37ad4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="37ad4-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="37ad4-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="37ad4-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="37ad4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="37ad4-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="37ad4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="37ad4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="37ad4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="37ad4-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="37ad4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="37ad4-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="37ad4-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37ad4-113">Определение</span><span class="sxs-lookup"><span data-stu-id="37ad4-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37ad4-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="37ad4-114">Elements and attributes</span></span>

<span data-ttu-id="37ad4-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="37ad4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="37ad4-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="37ad4-116">Parent elements</span></span>

|<span data-ttu-id="37ad4-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="37ad4-117">**Element**</span></span>|<span data-ttu-id="37ad4-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="37ad4-118">**Type**</span></span>|<span data-ttu-id="37ad4-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37ad4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37ad4-120">Section</span><span class="sxs-lookup"><span data-stu-id="37ad4-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37ad4-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="37ad4-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37ad4-122">Указанный пользователем фрагмент информации, на который могут ссылаться другие ячейки и средства надстройки.</span><span class="sxs-lookup"><span data-stu-id="37ad4-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37ad4-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="37ad4-123">Child elements</span></span>

|<span data-ttu-id="37ad4-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="37ad4-124">**Element**</span></span>|<span data-ttu-id="37ad4-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="37ad4-125">**Type**</span></span>|<span data-ttu-id="37ad4-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37ad4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37ad4-127">Cell</span><span class="sxs-lookup"><span data-stu-id="37ad4-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="37ad4-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="37ad4-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37ad4-129">Одно свойство определенного пользователем фрагмента информации, на которое могут ссылаться другие ячейки и средства надстройки.</span><span class="sxs-lookup"><span data-stu-id="37ad4-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="37ad4-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="37ad4-130">Attributes</span></span>

|<span data-ttu-id="37ad4-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="37ad4-131">**Attribute**</span></span>|<span data-ttu-id="37ad4-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="37ad4-132">**Type**</span></span>|<span data-ttu-id="37ad4-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="37ad4-133">**Required**</span></span>|<span data-ttu-id="37ad4-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37ad4-134">**Description**</span></span>|<span data-ttu-id="37ad4-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="37ad4-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37ad4-136">Del</span><span class="sxs-lookup"><span data-stu-id="37ad4-136">Del</span></span>  <br/> |<span data-ttu-id="37ad4-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="37ad4-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="37ad4-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="37ad4-138">optional</span></span>  <br/> |<span data-ttu-id="37ad4-139">Указывает, была ли удалена строка, которая в противном случае наследуется от этаго фигуры.</span><span class="sxs-lookup"><span data-stu-id="37ad4-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="37ad4-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="37ad4-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="37ad4-141">IX</span><span class="sxs-lookup"><span data-stu-id="37ad4-141">IX</span></span>  <br/> |<span data-ttu-id="37ad4-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37ad4-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37ad4-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="37ad4-143">optional</span></span>  <br/> |<span data-ttu-id="37ad4-144">Указывает идентификатор строки, основанный на одном.</span><span class="sxs-lookup"><span data-stu-id="37ad4-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="37ad4-145">Оно должно быть неподдерживаемо и больше других идентификаторов в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="37ad4-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="37ad4-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="37ad4-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="37ad4-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="37ad4-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="37ad4-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="37ad4-148">LocalName</span></span>  <br/> |<span data-ttu-id="37ad4-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37ad4-149">xsd:string</span></span>  <br/> |<span data-ttu-id="37ad4-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="37ad4-150">optional</span></span>  <br/> |<span data-ttu-id="37ad4-151">Указывает уникальное имя строки, зависимое от языка.</span><span class="sxs-lookup"><span data-stu-id="37ad4-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="37ad4-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="37ad4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37ad4-153">N</span><span class="sxs-lookup"><span data-stu-id="37ad4-153">N</span></span>  <br/> |<span data-ttu-id="37ad4-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37ad4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="37ad4-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="37ad4-155">optional</span></span>  <br/> |<span data-ttu-id="37ad4-156">Указывает уникальное независимое от языка имя строки. Атрибут N используется только для разделов "Пользователь", "Свойство", "Действия", "Управление", "Подключение", "Гиперссылка" и "ActionTag".</span><span class="sxs-lookup"><span data-stu-id="37ad4-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="37ad4-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="37ad4-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="37ad4-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="37ad4-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37ad4-159">T</span><span class="sxs-lookup"><span data-stu-id="37ad4-159">T</span></span>  <br/> |<span data-ttu-id="37ad4-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37ad4-160">xsd:string</span></span>  <br/> |<span data-ttu-id="37ad4-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="37ad4-161">optional</span></span>  <br/> |<span data-ttu-id="37ad4-162">Указывает тип геометрического пути, представленного строкой и используемого при визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="37ad4-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="37ad4-163">Атрибут T используется только для раздела "Геометрия".</span><span class="sxs-lookup"><span data-stu-id="37ad4-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="37ad4-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="37ad4-164">Values of the xsd:string type.</span></span>  <br/> |
   

