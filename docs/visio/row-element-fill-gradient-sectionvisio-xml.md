---
title: Элемент Row (раздел "Градиентная заливка") (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538622"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="81f59-103">Элемент Row (раздел "Градиентная заливка") (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="81f59-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="81f59-104">Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.</span><span class="sxs-lookup"><span data-stu-id="81f59-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81f59-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="81f59-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81f59-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="81f59-106">**Element type**</span></span> <br/> |[<span data-ttu-id="81f59-107">Филлградиентров_типе</span><span class="sxs-lookup"><span data-stu-id="81f59-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="81f59-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="81f59-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="81f59-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="81f59-109">**Schema file**</span></span> <br/> |<span data-ttu-id="81f59-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="81f59-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="81f59-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="81f59-111">**Document parts**</span></span> <br/> |<span data-ttu-id="81f59-112">Document. XML, Master #. XML, Page #. XML</span><span class="sxs-lookup"><span data-stu-id="81f59-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81f59-113">Определение</span><span class="sxs-lookup"><span data-stu-id="81f59-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="81f59-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="81f59-114">Elements and attributes</span></span>

<span data-ttu-id="81f59-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="81f59-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="81f59-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="81f59-116">Parent elements</span></span>

|<span data-ttu-id="81f59-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="81f59-117">**Element**</span></span>|<span data-ttu-id="81f59-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="81f59-118">**Type**</span></span>|<span data-ttu-id="81f59-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81f59-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81f59-120">Section</span><span class="sxs-lookup"><span data-stu-id="81f59-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81f59-121">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="81f59-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="81f59-122">Содержит цвет, прозрачность и положение остановки градиента для градиента заливки.</span><span class="sxs-lookup"><span data-stu-id="81f59-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81f59-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81f59-123">Child elements</span></span>

|<span data-ttu-id="81f59-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="81f59-124">**Element**</span></span>|<span data-ttu-id="81f59-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="81f59-125">**Type**</span></span>|<span data-ttu-id="81f59-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81f59-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81f59-127">Cell</span><span class="sxs-lookup"><span data-stu-id="81f59-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="81f59-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="81f59-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="81f59-129">Задает одно свойство.</span><span class="sxs-lookup"><span data-stu-id="81f59-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="81f59-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="81f59-130">Attributes</span></span>

|<span data-ttu-id="81f59-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="81f59-131">**Attribute**</span></span>|<span data-ttu-id="81f59-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="81f59-132">**Type**</span></span>|<span data-ttu-id="81f59-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="81f59-133">**Required**</span></span>|<span data-ttu-id="81f59-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81f59-134">**Description**</span></span>|<span data-ttu-id="81f59-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="81f59-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="81f59-136">Del</span><span class="sxs-lookup"><span data-stu-id="81f59-136">Del</span></span>  <br/> |<span data-ttu-id="81f59-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="81f59-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="81f59-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="81f59-138">optional</span></span>  <br/> |<span data-ttu-id="81f59-139">Указывает, удалена ли строка, которая в противном случае была бы унаследована от основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="81f59-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="81f59-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="81f59-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="81f59-141">IX</span><span class="sxs-lookup"><span data-stu-id="81f59-141">IX</span></span>  <br/> |<span data-ttu-id="81f59-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="81f59-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81f59-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="81f59-143">optional</span></span>  <br/> |<span data-ttu-id="81f59-144">Задает отсчитываемый от единицы идентификатор строки.</span><span class="sxs-lookup"><span data-stu-id="81f59-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="81f59-145">Он должен быть уникальное и превышать другие идентификаторы в одном разделе. Атрибут IX используется только для разделов "символ", "подключение", "Филлградиент", "геометрия", "область", "Линеградиент", "Абзац", "фрагмент" и "вкладки".</span><span class="sxs-lookup"><span data-stu-id="81f59-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="81f59-146">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="81f59-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="81f59-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="81f59-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="81f59-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="81f59-148">LocalName</span></span>  <br/> |<span data-ttu-id="81f59-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="81f59-149">xsd:string</span></span>  <br/> |<span data-ttu-id="81f59-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="81f59-150">optional</span></span>  <br/> |<span data-ttu-id="81f59-151">Задает уникальное зависящее от языка имя строки.</span><span class="sxs-lookup"><span data-stu-id="81f59-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="81f59-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="81f59-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="81f59-153">N</span><span class="sxs-lookup"><span data-stu-id="81f59-153">N</span></span>  <br/> |<span data-ttu-id="81f59-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="81f59-154">xsd:string</span></span>  <br/> |<span data-ttu-id="81f59-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="81f59-155">optional</span></span>  <br/> |<span data-ttu-id="81f59-156">Задает уникальное имя строки, не зависящее от языка. Атрибут N используется только для разделов "пользователь", "свойство", "действия", "элементы управления", "гиперссылка" и "Актионтаг".</span><span class="sxs-lookup"><span data-stu-id="81f59-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="81f59-157">Строка может иметь только один из атрибутов IX или N.</span><span class="sxs-lookup"><span data-stu-id="81f59-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="81f59-158">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="81f59-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="81f59-159">Д</span><span class="sxs-lookup"><span data-stu-id="81f59-159">T</span></span>  <br/> |<span data-ttu-id="81f59-160">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="81f59-160">xsd:string</span></span>  <br/> |<span data-ttu-id="81f59-161">необязательный</span><span class="sxs-lookup"><span data-stu-id="81f59-161">optional</span></span>  <br/> |<span data-ttu-id="81f59-162">Указывает тип геометрического пути, представленного строкой и используемый в визуализации геометрии.</span><span class="sxs-lookup"><span data-stu-id="81f59-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="81f59-163">Атрибут T используется только для раздела Geometry.</span><span class="sxs-lookup"><span data-stu-id="81f59-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="81f59-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="81f59-164">Values of the xsd:string type.</span></span>  <br/> |
   

