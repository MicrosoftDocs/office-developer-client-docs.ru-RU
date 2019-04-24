---
title: Элемент DocumentSheet (Висиодокумент_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Указывает структуру DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356366"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="c6558-103">Элемент DocumentSheet (Висиодокумент_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c6558-103">DocumentSheet element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c6558-104">Указывает структуру DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="c6558-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6558-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c6558-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6558-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c6558-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c6558-107">Документшит_типе</span><span class="sxs-lookup"><span data-stu-id="c6558-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c6558-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c6558-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c6558-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c6558-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c6558-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c6558-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c6558-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c6558-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c6558-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="c6558-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c6558-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c6558-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c6558-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6558-114">Elements and attributes</span></span>

<span data-ttu-id="c6558-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c6558-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c6558-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c6558-116">Parent elements</span></span>

|<span data-ttu-id="c6558-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c6558-117">**Element**</span></span>|<span data-ttu-id="c6558-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c6558-118">**Type**</span></span>|<span data-ttu-id="c6558-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6558-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6558-120">Висиодокумент</span><span class="sxs-lookup"><span data-stu-id="c6558-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="c6558-121">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="c6558-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6558-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c6558-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c6558-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c6558-123">Child elements</span></span>

|<span data-ttu-id="c6558-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c6558-124">**Element**</span></span>|<span data-ttu-id="c6558-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c6558-125">**Type**</span></span>|<span data-ttu-id="c6558-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6558-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6558-127">Cell</span><span class="sxs-lookup"><span data-stu-id="c6558-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="c6558-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="c6558-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c6558-129">Указывает ячейку в элементе DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="c6558-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c6558-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6558-130">Attributes</span></span>

|<span data-ttu-id="c6558-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c6558-131">**Attribute**</span></span>|<span data-ttu-id="c6558-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c6558-132">**Type**</span></span>|<span data-ttu-id="c6558-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c6558-133">**Required**</span></span>|<span data-ttu-id="c6558-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6558-134">**Description**</span></span>|<span data-ttu-id="c6558-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c6558-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c6558-136">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="c6558-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="c6558-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c6558-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c6558-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c6558-138">optional</span></span>  <br/> |<span data-ttu-id="c6558-139">Указывает, было ли имя настроено пользователем.</span><span class="sxs-lookup"><span data-stu-id="c6558-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="c6558-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c6558-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="c6558-141">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="c6558-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c6558-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c6558-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c6558-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="c6558-143">optional</span></span>  <br/> |<span data-ttu-id="c6558-144">Указывает, настроено ли универсальное имя пользователем.</span><span class="sxs-lookup"><span data-stu-id="c6558-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="c6558-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c6558-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="c6558-146">Имя</span><span class="sxs-lookup"><span data-stu-id="c6558-146">Name</span></span>  <br/> |<span data-ttu-id="c6558-147">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c6558-147">xsd:string</span></span>  <br/> |<span data-ttu-id="c6558-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="c6558-148">optional</span></span>  <br/> |<span data-ttu-id="c6558-149">Задает зависящее от языка имя DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="c6558-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="c6558-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="c6558-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6558-151">NameU</span><span class="sxs-lookup"><span data-stu-id="c6558-151">NameU</span></span>  <br/> |<span data-ttu-id="c6558-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c6558-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c6558-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="c6558-153">optional</span></span>  <br/> |<span data-ttu-id="c6558-154">Указывает имя DocumentSheet, не зависящее от языка.</span><span class="sxs-lookup"><span data-stu-id="c6558-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="c6558-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="c6558-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c6558-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c6558-156">UniqueID</span></span>  <br/> |<span data-ttu-id="c6558-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c6558-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c6558-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="c6558-158">optional</span></span>  <br/> |<span data-ttu-id="c6558-159">Необязательный атрибут типа string.</span><span class="sxs-lookup"><span data-stu-id="c6558-159">Optional string.</span></span> <span data-ttu-id="c6558-160">GUID (глобальный уникальный идентификатор), определяющий фигуру.</span><span class="sxs-lookup"><span data-stu-id="c6558-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="c6558-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="c6558-161">Values of the xsd:string type.</span></span>  <br/> |
   

