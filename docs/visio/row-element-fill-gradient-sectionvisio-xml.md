---
title: Элемент Row (Раздел Заполнения Градиента) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Содержит цвет, прозрачность и расположение остановки градиента для градиента заполнения.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538622"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="4be22-103">Элемент Row (Раздел Заполнения Градиента) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4be22-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="4be22-104">Содержит цвет, прозрачность и расположение остановки градиента для градиента заполнения.</span><span class="sxs-lookup"><span data-stu-id="4be22-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4be22-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4be22-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4be22-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4be22-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4be22-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="4be22-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4be22-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4be22-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4be22-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4be22-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4be22-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4be22-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4be22-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="4be22-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4be22-112">document.xml, master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="4be22-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4be22-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4be22-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4be22-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4be22-114">Elements and attributes</span></span>

<span data-ttu-id="4be22-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4be22-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4be22-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4be22-116">Parent elements</span></span>

|<span data-ttu-id="4be22-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4be22-117">**Element**</span></span>|<span data-ttu-id="4be22-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4be22-118">**Type**</span></span>|<span data-ttu-id="4be22-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4be22-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4be22-120">Section</span><span class="sxs-lookup"><span data-stu-id="4be22-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4be22-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="4be22-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4be22-122">Содержит цвет, прозрачность и расположение остановки градиента для градиента заполнения.</span><span class="sxs-lookup"><span data-stu-id="4be22-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4be22-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4be22-123">Child elements</span></span>

|<span data-ttu-id="4be22-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4be22-124">**Element**</span></span>|<span data-ttu-id="4be22-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4be22-125">**Type**</span></span>|<span data-ttu-id="4be22-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4be22-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4be22-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4be22-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4be22-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4be22-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4be22-129">Указывает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="4be22-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4be22-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4be22-130">Attributes</span></span>

|<span data-ttu-id="4be22-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4be22-131">**Attribute**</span></span>|<span data-ttu-id="4be22-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4be22-132">**Type**</span></span>|<span data-ttu-id="4be22-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4be22-133">**Required**</span></span>|<span data-ttu-id="4be22-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4be22-134">**Description**</span></span>|<span data-ttu-id="4be22-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4be22-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4be22-136">Del</span><span class="sxs-lookup"><span data-stu-id="4be22-136">Del</span></span>  <br/> |<span data-ttu-id="4be22-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4be22-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4be22-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4be22-138">optional</span></span>  <br/> |<span data-ttu-id="4be22-139">Указывает, была ли удалена строка, которая в противном случае была бы унаследована от мастер-фигуры.</span><span class="sxs-lookup"><span data-stu-id="4be22-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="4be22-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4be22-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4be22-141">IX</span><span class="sxs-lookup"><span data-stu-id="4be22-141">IX</span></span>  <br/> |<span data-ttu-id="4be22-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4be22-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4be22-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="4be22-143">optional</span></span>  <br/> |<span data-ttu-id="4be22-144">Указывает идентификатор для строки на основе одного.</span><span class="sxs-lookup"><span data-stu-id="4be22-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="4be22-145">Он должен быть unqiue и больше, чем другие идентификаторы в том же разделе. Атрибут IX используется только для разделов Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch и Tabs.</span><span class="sxs-lookup"><span data-stu-id="4be22-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="4be22-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="4be22-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4be22-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4be22-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4be22-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="4be22-148">LocalName</span></span>  <br/> |<span data-ttu-id="4be22-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4be22-149">xsd:string</span></span>  <br/> |<span data-ttu-id="4be22-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="4be22-150">optional</span></span>  <br/> |<span data-ttu-id="4be22-151">Указывает уникальное имя строки, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="4be22-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="4be22-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4be22-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4be22-153">Нет</span><span class="sxs-lookup"><span data-stu-id="4be22-153">N</span></span>  <br/> |<span data-ttu-id="4be22-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4be22-154">xsd:string</span></span>  <br/> |<span data-ttu-id="4be22-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="4be22-155">optional</span></span>  <br/> |<span data-ttu-id="4be22-156">Указывает уникальное имя строки, независимое от языка. Атрибут N используется только для разделов User, Property, Actions, Control, Connection, Hyperlink и ActionTag.</span><span class="sxs-lookup"><span data-stu-id="4be22-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="4be22-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="4be22-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4be22-158">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4be22-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4be22-159">T</span><span class="sxs-lookup"><span data-stu-id="4be22-159">T</span></span>  <br/> |<span data-ttu-id="4be22-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4be22-160">xsd:string</span></span>  <br/> |<span data-ttu-id="4be22-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="4be22-161">optional</span></span>  <br/> |<span data-ttu-id="4be22-162">Указывает тип геометрического пути, представленного строкой и используемого в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="4be22-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="4be22-163">Атрибут T используется только для раздела Геометрия.</span><span class="sxs-lookup"><span data-stu-id="4be22-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="4be22-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4be22-164">Values of the xsd:string type.</span></span>  <br/> |
   

