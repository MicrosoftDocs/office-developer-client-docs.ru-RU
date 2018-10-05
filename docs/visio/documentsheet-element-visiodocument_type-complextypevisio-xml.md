---
title: Элемент DocumentSheet (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Определяет структуру DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383466"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="a7948-103">Элемент DocumentSheet (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="a7948-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a7948-104">Определяет структуру DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a7948-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7948-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a7948-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7948-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a7948-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a7948-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a7948-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a7948-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a7948-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a7948-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a7948-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a7948-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a7948-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a7948-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="a7948-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a7948-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="a7948-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7948-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a7948-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7948-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a7948-114">Elements and attributes</span></span>

<span data-ttu-id="a7948-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a7948-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a7948-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a7948-116">Parent elements</span></span>

|<span data-ttu-id="a7948-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a7948-117">**Element**</span></span>|<span data-ttu-id="a7948-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a7948-118">**Type**</span></span>|<span data-ttu-id="a7948-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7948-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7948-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="a7948-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="a7948-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="a7948-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7948-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a7948-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7948-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a7948-123">Child elements</span></span>

|<span data-ttu-id="a7948-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a7948-124">**Element**</span></span>|<span data-ttu-id="a7948-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a7948-125">**Type**</span></span>|<span data-ttu-id="a7948-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7948-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a7948-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a7948-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a7948-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a7948-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a7948-129">Указывает ячейку в DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a7948-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a7948-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a7948-130">Attributes</span></span>

|<span data-ttu-id="a7948-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a7948-131">**Attribute**</span></span>|<span data-ttu-id="a7948-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a7948-132">**Type**</span></span>|<span data-ttu-id="a7948-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a7948-133">**Required**</span></span>|<span data-ttu-id="a7948-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7948-134">**Description**</span></span>|<span data-ttu-id="a7948-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a7948-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a7948-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a7948-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="a7948-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a7948-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a7948-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="a7948-138">optional</span></span>  <br/> |<span data-ttu-id="a7948-139">Описание, настроен ли имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7948-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a7948-140">Значения типа xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="a7948-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a7948-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a7948-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a7948-142">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a7948-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a7948-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="a7948-143">optional</span></span>  <br/> |<span data-ttu-id="a7948-144">Описание, настроен ли универсального имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7948-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a7948-145">Значения типа xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="a7948-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="a7948-146">Имя</span><span class="sxs-lookup"><span data-stu-id="a7948-146">Name</span></span>  <br/> |<span data-ttu-id="a7948-147">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a7948-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a7948-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="a7948-148">optional</span></span>  <br/> |<span data-ttu-id="a7948-149">Задает имя зависит от языка DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a7948-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a7948-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a7948-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a7948-151">NameU</span><span class="sxs-lookup"><span data-stu-id="a7948-151">NameU</span></span>  <br/> |<span data-ttu-id="a7948-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a7948-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a7948-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="a7948-153">optional</span></span>  <br/> |<span data-ttu-id="a7948-154">Задает имя зависящего от языка DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="a7948-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="a7948-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a7948-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a7948-156">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="a7948-156">UniqueID</span></span>  <br/> |<span data-ttu-id="a7948-157">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a7948-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a7948-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="a7948-158">optional</span></span>  <br/> |<span data-ttu-id="a7948-159">Необязательный атрибут типа string.</span><span class="sxs-lookup"><span data-stu-id="a7948-159">Optional string.</span></span> <span data-ttu-id="a7948-160">GUID (глобальный уникальный идентификатор), идентифицирующий фигуры.</span><span class="sxs-lookup"><span data-stu-id="a7948-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="a7948-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a7948-161">Values of the xsd:string type.</span></span>  <br/> |
   

