---
title: Элемент Row (раздел определенных пользователем ячеек) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Определенные пользователем блок данных, можно ссылаться другие ячейки и надстройки.
ms.openlocfilehash: 10a0e0e5f7255274de528a34d5faa2de6137446e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814676"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="7ad67-103">Элемент Row (раздел определенных пользователем ячеек) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7ad67-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="7ad67-104">Определенные пользователем блок данных, можно ссылаться другие ячейки и надстройки.</span><span class="sxs-lookup"><span data-stu-id="7ad67-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ad67-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7ad67-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ad67-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7ad67-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7ad67-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="7ad67-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7ad67-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7ad67-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7ad67-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7ad67-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7ad67-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7ad67-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7ad67-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7ad67-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7ad67-112">Document.XML, masters.xml, главные # .xml, pages.xml, страницы # .xml</span><span class="sxs-lookup"><span data-stu-id="7ad67-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ad67-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7ad67-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7ad67-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ad67-114">Elements and attributes</span></span>

<span data-ttu-id="7ad67-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="7ad67-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7ad67-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7ad67-116">Parent elements</span></span>

|<span data-ttu-id="7ad67-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7ad67-117">**Element**</span></span>|<span data-ttu-id="7ad67-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ad67-118">**Type**</span></span>|<span data-ttu-id="7ad67-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ad67-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ad67-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ad67-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7ad67-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7ad67-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7ad67-122">Определенные пользователем блок данных, можно ссылаться другие ячейки и надстройки.</span><span class="sxs-lookup"><span data-stu-id="7ad67-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7ad67-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7ad67-123">Child elements</span></span>

|<span data-ttu-id="7ad67-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7ad67-124">**Element**</span></span>|<span data-ttu-id="7ad67-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ad67-125">**Type**</span></span>|<span data-ttu-id="7ad67-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ad67-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ad67-127">Cell</span><span class="sxs-lookup"><span data-stu-id="7ad67-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7ad67-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7ad67-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7ad67-129">Одно свойство фрагмента определенные пользователем сведения, которые могут быть ссылается другие ячейки и надстройки.</span><span class="sxs-lookup"><span data-stu-id="7ad67-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7ad67-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ad67-130">Attributes</span></span>

|<span data-ttu-id="7ad67-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7ad67-131">**Attribute**</span></span>|<span data-ttu-id="7ad67-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ad67-132">**Type**</span></span>|<span data-ttu-id="7ad67-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="7ad67-133">**Required**</span></span>|<span data-ttu-id="7ad67-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ad67-134">**Description**</span></span>|<span data-ttu-id="7ad67-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7ad67-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7ad67-136">DEL</span><span class="sxs-lookup"><span data-stu-id="7ad67-136">Del</span></span>  <br/> |<span data-ttu-id="7ad67-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="7ad67-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7ad67-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ad67-138">optional</span></span>  <br/> |<span data-ttu-id="7ad67-139">Указывает, был ли удален строку, в противном случае будут унаследованы от образца фигуры.</span><span class="sxs-lookup"><span data-stu-id="7ad67-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="7ad67-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7ad67-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7ad67-141">IX</span><span class="sxs-lookup"><span data-stu-id="7ad67-141">IX</span></span>  <br/> |<span data-ttu-id="7ad67-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7ad67-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7ad67-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ad67-143">optional</span></span>  <br/> |<span data-ttu-id="7ad67-144">Указывает идентификатор на основе одной строки.</span><span class="sxs-lookup"><span data-stu-id="7ad67-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="7ad67-145">Оно должно быть unqiue и больше, чем другие идентификаторы в одном разделе. Атрибут IX используется только для разделов символ, подключения, поле, FillGradient, геометрии, уровень, LineGradient, абзаца, редактор, нуля и вкладок.</span><span class="sxs-lookup"><span data-stu-id="7ad67-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="7ad67-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="7ad67-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7ad67-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7ad67-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7ad67-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="7ad67-148">LocalName</span></span>  <br/> |<span data-ttu-id="7ad67-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7ad67-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7ad67-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ad67-150">optional</span></span>  <br/> |<span data-ttu-id="7ad67-151">Указывает уникальное имя зависит от языка строки.</span><span class="sxs-lookup"><span data-stu-id="7ad67-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="7ad67-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7ad67-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ad67-153">N</span><span class="sxs-lookup"><span data-stu-id="7ad67-153">N</span></span>  <br/> |<span data-ttu-id="7ad67-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7ad67-154">xsd:string</span></span>  <br/> |<span data-ttu-id="7ad67-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ad67-155">optional</span></span>  <br/> |<span data-ttu-id="7ad67-156">Указывает уникальное имя зависящего от языка строки. Атрибут N используется только для пользователя, свойство, действия, элемент управления, подключения, гиперссылки и ActionTag разделы.</span><span class="sxs-lookup"><span data-stu-id="7ad67-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="7ad67-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="7ad67-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7ad67-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7ad67-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ad67-159">T</span><span class="sxs-lookup"><span data-stu-id="7ad67-159">T</span></span>  <br/> |<span data-ttu-id="7ad67-160">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7ad67-160">xsd:string</span></span>  <br/> |<span data-ttu-id="7ad67-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ad67-161">optional</span></span>  <br/> |<span data-ttu-id="7ad67-162">Указывает тип геометрического пути представленного строкой и используется в геометрии визуализации.</span><span class="sxs-lookup"><span data-stu-id="7ad67-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="7ad67-163">Атрибут T используется только для раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="7ad67-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="7ad67-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7ad67-164">Values of the xsd:string type.</span></span>  <br/> |
   

