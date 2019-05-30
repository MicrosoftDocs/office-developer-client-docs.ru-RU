---
title: Элемент DocumentSheet (Висиодокумент_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Указывает структуру DocumentSheet.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540044"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="f70b9-103">Элемент DocumentSheet (Висиодокумент_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="f70b9-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f70b9-104">Указывает структуру DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="f70b9-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f70b9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f70b9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f70b9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f70b9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f70b9-107">Документшит_типе</span><span class="sxs-lookup"><span data-stu-id="f70b9-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f70b9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f70b9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f70b9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f70b9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f70b9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f70b9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f70b9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f70b9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f70b9-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="f70b9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f70b9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f70b9-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f70b9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f70b9-114">Elements and attributes</span></span>

<span data-ttu-id="f70b9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f70b9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f70b9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f70b9-116">Parent elements</span></span>

|<span data-ttu-id="f70b9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f70b9-117">**Element**</span></span>|<span data-ttu-id="f70b9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f70b9-118">**Type**</span></span>|<span data-ttu-id="f70b9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f70b9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f70b9-120">Висиодокумент</span><span class="sxs-lookup"><span data-stu-id="f70b9-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="f70b9-121">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="f70b9-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f70b9-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="f70b9-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f70b9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f70b9-123">Child elements</span></span>

|<span data-ttu-id="f70b9-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f70b9-124">**Element**</span></span>|<span data-ttu-id="f70b9-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f70b9-125">**Type**</span></span>|<span data-ttu-id="f70b9-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f70b9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f70b9-127">Cell</span><span class="sxs-lookup"><span data-stu-id="f70b9-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="f70b9-128">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="f70b9-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f70b9-129">Указывает ячейку в элементе DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="f70b9-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f70b9-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f70b9-130">Attributes</span></span>

|<span data-ttu-id="f70b9-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f70b9-131">**Attribute**</span></span>|<span data-ttu-id="f70b9-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f70b9-132">**Type**</span></span>|<span data-ttu-id="f70b9-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f70b9-133">**Required**</span></span>|<span data-ttu-id="f70b9-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f70b9-134">**Description**</span></span>|<span data-ttu-id="f70b9-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f70b9-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f70b9-136">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="f70b9-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="f70b9-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f70b9-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f70b9-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f70b9-138">optional</span></span>  <br/> |<span data-ttu-id="f70b9-139">Указывает, было ли имя настроено пользователем.</span><span class="sxs-lookup"><span data-stu-id="f70b9-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="f70b9-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f70b9-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="f70b9-141">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="f70b9-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f70b9-142">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f70b9-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f70b9-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="f70b9-143">optional</span></span>  <br/> |<span data-ttu-id="f70b9-144">Указывает, настроено ли универсальное имя пользователем.</span><span class="sxs-lookup"><span data-stu-id="f70b9-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="f70b9-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f70b9-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="f70b9-146">Имя</span><span class="sxs-lookup"><span data-stu-id="f70b9-146">Name</span></span>  <br/> |<span data-ttu-id="f70b9-147">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f70b9-147">xsd:string</span></span>  <br/> |<span data-ttu-id="f70b9-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="f70b9-148">optional</span></span>  <br/> |<span data-ttu-id="f70b9-149">Задает зависящее от языка имя DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="f70b9-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="f70b9-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f70b9-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f70b9-151">NameU</span><span class="sxs-lookup"><span data-stu-id="f70b9-151">NameU</span></span>  <br/> |<span data-ttu-id="f70b9-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f70b9-152">xsd:string</span></span>  <br/> |<span data-ttu-id="f70b9-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="f70b9-153">optional</span></span>  <br/> |<span data-ttu-id="f70b9-154">Указывает имя DocumentSheet, не зависящее от языка.</span><span class="sxs-lookup"><span data-stu-id="f70b9-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="f70b9-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f70b9-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f70b9-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f70b9-156">UniqueID</span></span>  <br/> |<span data-ttu-id="f70b9-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f70b9-157">xsd:string</span></span>  <br/> |<span data-ttu-id="f70b9-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="f70b9-158">optional</span></span>  <br/> |<span data-ttu-id="f70b9-159">Необязательный атрибут типа string.</span><span class="sxs-lookup"><span data-stu-id="f70b9-159">Optional string.</span></span> <span data-ttu-id="f70b9-160">GUID (глобальный уникальный идентификатор), определяющий фигуру.</span><span class="sxs-lookup"><span data-stu-id="f70b9-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="f70b9-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f70b9-161">Values of the xsd:string type.</span></span>  <br/> |
   

