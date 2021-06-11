---
title: Элемент DocumentSheet (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Указывает структуру Таблицы документов.
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540044"
---
# <a name="documentsheet-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="7e31d-103">Элемент DocumentSheet (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7e31d-103">DocumentSheet element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7e31d-104">Указывает структуру Таблицы документов.</span><span class="sxs-lookup"><span data-stu-id="7e31d-104">Specifies a DocumentSheet structure.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e31d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7e31d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e31d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7e31d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7e31d-107">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="7e31d-107">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7e31d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7e31d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7e31d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7e31d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7e31d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7e31d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7e31d-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="7e31d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7e31d-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="7e31d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e31d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7e31d-113">Definition</span></span>

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e31d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7e31d-114">Elements and attributes</span></span>

<span data-ttu-id="7e31d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7e31d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7e31d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7e31d-116">Parent elements</span></span>

|<span data-ttu-id="7e31d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7e31d-117">**Element**</span></span>|<span data-ttu-id="7e31d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7e31d-118">**Type**</span></span>|<span data-ttu-id="7e31d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7e31d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e31d-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="7e31d-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="7e31d-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="7e31d-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e31d-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7e31d-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e31d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7e31d-123">Child elements</span></span>

|<span data-ttu-id="7e31d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7e31d-124">**Element**</span></span>|<span data-ttu-id="7e31d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7e31d-125">**Type**</span></span>|<span data-ttu-id="7e31d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7e31d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e31d-127">Cell</span><span class="sxs-lookup"><span data-stu-id="7e31d-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="7e31d-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7e31d-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e31d-129">Указывает ячейку в таблице DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7e31d-129">Specifies a cell in a DocumentSheet.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7e31d-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7e31d-130">Attributes</span></span>

|<span data-ttu-id="7e31d-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7e31d-131">**Attribute**</span></span>|<span data-ttu-id="7e31d-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7e31d-132">**Type**</span></span>|<span data-ttu-id="7e31d-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7e31d-133">**Required**</span></span>|<span data-ttu-id="7e31d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7e31d-134">**Description**</span></span>|<span data-ttu-id="7e31d-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7e31d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7e31d-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="7e31d-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="7e31d-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7e31d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7e31d-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="7e31d-138">optional</span></span>  <br/> |<span data-ttu-id="7e31d-139">Описывает, было ли имя настроено пользователем.</span><span class="sxs-lookup"><span data-stu-id="7e31d-139">Describes whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="7e31d-140">Значения типа xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="7e31d-140">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="7e31d-141">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="7e31d-141">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="7e31d-142">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7e31d-142">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7e31d-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="7e31d-143">optional</span></span>  <br/> |<span data-ttu-id="7e31d-144">Описывает, было ли универсальное имя настроено пользователем.</span><span class="sxs-lookup"><span data-stu-id="7e31d-144">Describes whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="7e31d-145">Значения типа xsd:Boolean.</span><span class="sxs-lookup"><span data-stu-id="7e31d-145">Values of the xsd:Boolean type.</span></span>  <br/> |
|<span data-ttu-id="7e31d-146">Имя</span><span class="sxs-lookup"><span data-stu-id="7e31d-146">Name</span></span>  <br/> |<span data-ttu-id="7e31d-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7e31d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="7e31d-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="7e31d-148">optional</span></span>  <br/> |<span data-ttu-id="7e31d-149">Указывает имя таблицы DocumentSheet, зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="7e31d-149">Specifies the language-dependent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="7e31d-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7e31d-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7e31d-151">NameU</span><span class="sxs-lookup"><span data-stu-id="7e31d-151">NameU</span></span>  <br/> |<span data-ttu-id="7e31d-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7e31d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="7e31d-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="7e31d-153">optional</span></span>  <br/> |<span data-ttu-id="7e31d-154">Указывает независимое от языка имя таблицы DocumentSheet.</span><span class="sxs-lookup"><span data-stu-id="7e31d-154">Specifies the language- independent name of the DocumentSheet.</span></span>  <br/> |<span data-ttu-id="7e31d-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7e31d-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7e31d-156">UniqueID</span><span class="sxs-lookup"><span data-stu-id="7e31d-156">UniqueID</span></span>  <br/> |<span data-ttu-id="7e31d-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7e31d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="7e31d-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="7e31d-158">optional</span></span>  <br/> |<span data-ttu-id="7e31d-159">Необязательный атрибут типа string.</span><span class="sxs-lookup"><span data-stu-id="7e31d-159">Optional string.</span></span> <span data-ttu-id="7e31d-160">GuID (глобальный уникальный идентификатор), определяющий фигуру.</span><span class="sxs-lookup"><span data-stu-id="7e31d-160">A GUID (globally unique identifier) identifying the shape.</span></span>  <br/> |<span data-ttu-id="7e31d-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7e31d-161">Values of the xsd:string type.</span></span>  <br/> |
   

