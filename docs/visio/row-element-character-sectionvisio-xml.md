---
title: Элемент Row (Раздел символов) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: Показаны атрибуты форматирования для текстового запуска фигуры, такие как шрифт, цвет, стиль текста, корпус, положение относительно базового и размера точеки.
ms.openlocfilehash: afff4dcb809bf73da6ada25045678711ade75b6b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541787"
---
# <a name="row-element-character-section-visio-xml"></a><span data-ttu-id="f0977-103">Элемент Row (Раздел символов) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f0977-103">Row element (Character Section) (Visio XML)</span></span>

<span data-ttu-id="f0977-104">Показаны атрибуты форматирования для текстового запуска фигуры, такие как шрифт, цвет, стиль текста, корпус, положение относительно базового и размера точеки.</span><span class="sxs-lookup"><span data-stu-id="f0977-104">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0977-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f0977-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0977-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f0977-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f0977-107">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="f0977-107">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f0977-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f0977-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f0977-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f0977-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f0977-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f0977-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f0977-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="f0977-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f0977-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="f0977-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0977-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f0977-113">Definition</span></span>

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f0977-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0977-114">Elements and attributes</span></span>

<span data-ttu-id="f0977-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f0977-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f0977-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f0977-116">Parent elements</span></span>

|<span data-ttu-id="f0977-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f0977-117">**Element**</span></span>|<span data-ttu-id="f0977-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f0977-118">**Type**</span></span>|<span data-ttu-id="f0977-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0977-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0977-120">Section</span><span class="sxs-lookup"><span data-stu-id="f0977-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0977-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="f0977-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0977-122">Показаны атрибуты форматирования для текстового запуска фигуры, такие как шрифт, цвет, стиль текста, корпус, положение относительно базового и размера точеки.</span><span class="sxs-lookup"><span data-stu-id="f0977-122">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f0977-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f0977-123">Child elements</span></span>

|<span data-ttu-id="f0977-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f0977-124">**Element**</span></span>|<span data-ttu-id="f0977-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f0977-125">**Type**</span></span>|<span data-ttu-id="f0977-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0977-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0977-127">Cell</span><span class="sxs-lookup"><span data-stu-id="f0977-127">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f0977-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f0977-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f0977-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="f0977-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f0977-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f0977-130">Attributes</span></span>

|<span data-ttu-id="f0977-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f0977-131">**Attribute**</span></span>|<span data-ttu-id="f0977-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f0977-132">**Type**</span></span>|<span data-ttu-id="f0977-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f0977-133">**Required**</span></span>|<span data-ttu-id="f0977-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f0977-134">**Description**</span></span>|<span data-ttu-id="f0977-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f0977-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0977-136">Del</span><span class="sxs-lookup"><span data-stu-id="f0977-136">Del</span></span>  <br/> |<span data-ttu-id="f0977-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f0977-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f0977-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f0977-138">optional</span></span>  <br/> |<span data-ttu-id="f0977-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="f0977-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="f0977-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f0977-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f0977-141">IX</span><span class="sxs-lookup"><span data-stu-id="f0977-141">IX</span></span>  <br/> |<span data-ttu-id="f0977-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f0977-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f0977-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="f0977-143">optional</span></span>  <br/> |<span data-ttu-id="f0977-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="f0977-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="f0977-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="f0977-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="f0977-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="f0977-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f0977-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f0977-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f0977-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="f0977-148">LocalName</span></span>  <br/> |<span data-ttu-id="f0977-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f0977-149">xsd:string</span></span>  <br/> |<span data-ttu-id="f0977-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="f0977-150">optional</span></span>  <br/> |<span data-ttu-id="f0977-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="f0977-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="f0977-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f0977-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f0977-153">Нет</span><span class="sxs-lookup"><span data-stu-id="f0977-153">N</span></span>  <br/> |<span data-ttu-id="f0977-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f0977-154">xsd:string</span></span>  <br/> |<span data-ttu-id="f0977-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="f0977-155">optional</span></span>  <br/> |<span data-ttu-id="f0977-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="f0977-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="f0977-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="f0977-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f0977-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f0977-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f0977-159">T</span><span class="sxs-lookup"><span data-stu-id="f0977-159">T</span></span>  <br/> |<span data-ttu-id="f0977-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f0977-160">xsd:string</span></span>  <br/> |<span data-ttu-id="f0977-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="f0977-161">optional</span></span>  <br/> |<span data-ttu-id="f0977-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="f0977-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="f0977-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="f0977-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="f0977-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f0977-164">Values of the xsd:string type.</span></span>  <br/> |
   

