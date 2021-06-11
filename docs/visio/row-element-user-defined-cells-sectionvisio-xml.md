---
title: Элемент Row (Раздел ячеек, определенный пользователем) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Указанная пользователем часть информации, на которую можно ссылаться другими ячейками и средствами надстройки.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538174"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="c5c18-103">Элемент Row (Раздел ячеек, определенный пользователем) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5c18-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="c5c18-104">Указанная пользователем часть информации, на которую можно ссылаться другими ячейками и средствами надстройки.</span><span class="sxs-lookup"><span data-stu-id="c5c18-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5c18-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c5c18-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5c18-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c5c18-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5c18-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="c5c18-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5c18-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c5c18-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5c18-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c5c18-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5c18-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5c18-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5c18-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c5c18-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c5c18-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="c5c18-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5c18-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c5c18-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5c18-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5c18-114">Elements and attributes</span></span>

<span data-ttu-id="c5c18-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c5c18-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5c18-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c5c18-116">Parent elements</span></span>

|<span data-ttu-id="c5c18-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5c18-117">**Element**</span></span>|<span data-ttu-id="c5c18-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5c18-118">**Type**</span></span>|<span data-ttu-id="c5c18-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5c18-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5c18-120">Section</span><span class="sxs-lookup"><span data-stu-id="c5c18-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c5c18-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="c5c18-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5c18-122">Указанная пользователем часть информации, на которую можно ссылаться другими ячейками и средствами надстройки.</span><span class="sxs-lookup"><span data-stu-id="c5c18-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5c18-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c5c18-123">Child elements</span></span>

|<span data-ttu-id="c5c18-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5c18-124">**Element**</span></span>|<span data-ttu-id="c5c18-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5c18-125">**Type**</span></span>|<span data-ttu-id="c5c18-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5c18-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5c18-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c5c18-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c5c18-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c5c18-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5c18-129">Одно свойство указанного пользователем фрагмента информации, на которое можно ссылаться другими ячейками и средствами надстройки.</span><span class="sxs-lookup"><span data-stu-id="c5c18-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c5c18-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5c18-130">Attributes</span></span>

|<span data-ttu-id="c5c18-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c5c18-131">**Attribute**</span></span>|<span data-ttu-id="c5c18-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5c18-132">**Type**</span></span>|<span data-ttu-id="c5c18-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c5c18-133">**Required**</span></span>|<span data-ttu-id="c5c18-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5c18-134">**Description**</span></span>|<span data-ttu-id="c5c18-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c5c18-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5c18-136">Del</span><span class="sxs-lookup"><span data-stu-id="c5c18-136">Del</span></span>  <br/> |<span data-ttu-id="c5c18-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c5c18-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c5c18-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5c18-138">optional</span></span>  <br/> |<span data-ttu-id="c5c18-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="c5c18-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="c5c18-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c5c18-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c5c18-141">IX</span><span class="sxs-lookup"><span data-stu-id="c5c18-141">IX</span></span>  <br/> |<span data-ttu-id="c5c18-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5c18-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5c18-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5c18-143">optional</span></span>  <br/> |<span data-ttu-id="c5c18-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="c5c18-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="c5c18-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="c5c18-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="c5c18-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c5c18-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c5c18-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5c18-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5c18-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="c5c18-148">LocalName</span></span>  <br/> |<span data-ttu-id="c5c18-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5c18-149">xsd:string</span></span>  <br/> |<span data-ttu-id="c5c18-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5c18-150">optional</span></span>  <br/> |<span data-ttu-id="c5c18-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="c5c18-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="c5c18-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5c18-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c5c18-153">Нет</span><span class="sxs-lookup"><span data-stu-id="c5c18-153">N</span></span>  <br/> |<span data-ttu-id="c5c18-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5c18-154">xsd:string</span></span>  <br/> |<span data-ttu-id="c5c18-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5c18-155">optional</span></span>  <br/> |<span data-ttu-id="c5c18-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="c5c18-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="c5c18-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="c5c18-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="c5c18-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5c18-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c5c18-159">T</span><span class="sxs-lookup"><span data-stu-id="c5c18-159">T</span></span>  <br/> |<span data-ttu-id="c5c18-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5c18-160">xsd:string</span></span>  <br/> |<span data-ttu-id="c5c18-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="c5c18-161">optional</span></span>  <br/> |<span data-ttu-id="c5c18-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="c5c18-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="c5c18-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="c5c18-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="c5c18-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5c18-164">Values of the xsd:string type.</span></span>  <br/> |
   

