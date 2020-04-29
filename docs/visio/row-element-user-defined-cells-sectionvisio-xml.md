---
title: Элемент Row (раздел "пользовательские ячейки") (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Указанный пользователем набор данных, на который можно ссылаться по другим ячейкам и средствам надстроек.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538174"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="62417-103">Элемент Row (раздел "пользовательские ячейки") (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="62417-103">Row element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="62417-104">Указанный пользователем набор данных, на который можно ссылаться по другим ячейкам и средствам надстроек.</span><span class="sxs-lookup"><span data-stu-id="62417-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62417-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62417-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62417-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="62417-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62417-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="62417-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62417-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="62417-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62417-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="62417-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62417-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="62417-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62417-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="62417-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62417-112">Document. XML, Master. XML, Master #. XML, Pages. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="62417-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62417-113">Определение</span><span class="sxs-lookup"><span data-stu-id="62417-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62417-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="62417-114">Elements and attributes</span></span>

<span data-ttu-id="62417-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="62417-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62417-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="62417-116">Parent elements</span></span>

|<span data-ttu-id="62417-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="62417-117">**Element**</span></span>|<span data-ttu-id="62417-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62417-118">**Type**</span></span>|<span data-ttu-id="62417-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62417-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62417-120">Section</span><span class="sxs-lookup"><span data-stu-id="62417-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62417-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="62417-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62417-122">Указанный пользователем набор данных, на который можно ссылаться по другим ячейкам и средствам надстроек.</span><span class="sxs-lookup"><span data-stu-id="62417-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62417-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62417-123">Child elements</span></span>

|<span data-ttu-id="62417-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="62417-124">**Element**</span></span>|<span data-ttu-id="62417-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62417-125">**Type**</span></span>|<span data-ttu-id="62417-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62417-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62417-127">Cell</span><span class="sxs-lookup"><span data-stu-id="62417-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="62417-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="62417-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62417-129">Одно свойство указанного пользователем набора данных, на которые можно ссылаться по другим ячейкам и средствам надстроек.</span><span class="sxs-lookup"><span data-stu-id="62417-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="62417-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62417-130">Attributes</span></span>

|<span data-ttu-id="62417-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="62417-131">**Attribute**</span></span>|<span data-ttu-id="62417-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62417-132">**Type**</span></span>|<span data-ttu-id="62417-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="62417-133">**Required**</span></span>|<span data-ttu-id="62417-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62417-134">**Description**</span></span>|<span data-ttu-id="62417-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="62417-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62417-136">Del</span><span class="sxs-lookup"><span data-stu-id="62417-136">Del</span></span>  <br/> |<span data-ttu-id="62417-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="62417-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62417-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="62417-138">optional</span></span>  <br/> |<span data-ttu-id="62417-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="62417-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="62417-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="62417-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="62417-141">IX</span><span class="sxs-lookup"><span data-stu-id="62417-141">IX</span></span>  <br/> |<span data-ttu-id="62417-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="62417-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62417-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="62417-143">optional</span></span>  <br/> |<span data-ttu-id="62417-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="62417-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="62417-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="62417-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="62417-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="62417-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="62417-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="62417-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="62417-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="62417-148">LocalName</span></span>  <br/> |<span data-ttu-id="62417-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="62417-149">xsd:string</span></span>  <br/> |<span data-ttu-id="62417-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="62417-150">optional</span></span>  <br/> |<span data-ttu-id="62417-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="62417-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="62417-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="62417-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62417-153">N</span><span class="sxs-lookup"><span data-stu-id="62417-153">N</span></span>  <br/> |<span data-ttu-id="62417-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="62417-154">xsd:string</span></span>  <br/> |<span data-ttu-id="62417-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="62417-155">optional</span></span>  <br/> |<span data-ttu-id="62417-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="62417-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="62417-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="62417-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="62417-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="62417-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62417-159">Д</span><span class="sxs-lookup"><span data-stu-id="62417-159">T</span></span>  <br/> |<span data-ttu-id="62417-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="62417-160">xsd:string</span></span>  <br/> |<span data-ttu-id="62417-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="62417-161">optional</span></span>  <br/> |<span data-ttu-id="62417-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="62417-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="62417-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="62417-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="62417-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="62417-164">Values of the xsd:string type.</span></span>  <br/> |
   

