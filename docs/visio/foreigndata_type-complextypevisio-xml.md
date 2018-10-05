---
title: ForeignData_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384159"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="73157-102">ForeignData_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="73157-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="73157-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="73157-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73157-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="73157-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="73157-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="73157-105">**Schema file**</span></span> <br/> |<span data-ttu-id="73157-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="73157-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="73157-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="73157-107">**Extension base**</span></span> <br/> |<span data-ttu-id="73157-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="73157-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73157-109">Определение</span><span class="sxs-lookup"><span data-stu-id="73157-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="73157-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="73157-110">Elements and attributes</span></span>

<span data-ttu-id="73157-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="73157-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="73157-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="73157-112">Child elements</span></span>

|<span data-ttu-id="73157-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="73157-113">**Element**</span></span>|<span data-ttu-id="73157-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="73157-114">**Type**</span></span>|<span data-ttu-id="73157-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73157-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73157-116">Rel</span><span class="sxs-lookup"><span data-stu-id="73157-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="73157-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="73157-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="73157-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="73157-118">Attributes</span></span>

|<span data-ttu-id="73157-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="73157-119">**Attribute**</span></span>|<span data-ttu-id="73157-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="73157-120">**Type**</span></span>|<span data-ttu-id="73157-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="73157-121">**Required**</span></span>|<span data-ttu-id="73157-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73157-122">**Description**</span></span>|<span data-ttu-id="73157-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="73157-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73157-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="73157-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="73157-125">XSD: double</span><span class="sxs-lookup"><span data-stu-id="73157-125">xsd:double</span></span>  <br/> |<span data-ttu-id="73157-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-126">optional</span></span>  <br/> ||<span data-ttu-id="73157-127">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="73157-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="73157-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="73157-128">CompressionType</span></span>  <br/> |<span data-ttu-id="73157-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="73157-129">xsd:token</span></span>  <br/> |<span data-ttu-id="73157-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-130">optional</span></span>  <br/> ||<span data-ttu-id="73157-131">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="73157-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="73157-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="73157-132">ExtentX</span></span>  <br/> |<span data-ttu-id="73157-133">XSD: double</span><span class="sxs-lookup"><span data-stu-id="73157-133">xsd:double</span></span>  <br/> |<span data-ttu-id="73157-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-134">optional</span></span>  <br/> ||<span data-ttu-id="73157-135">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="73157-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="73157-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="73157-136">ExtentY</span></span>  <br/> |<span data-ttu-id="73157-137">XSD: double</span><span class="sxs-lookup"><span data-stu-id="73157-137">xsd:double</span></span>  <br/> |<span data-ttu-id="73157-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-138">optional</span></span>  <br/> ||<span data-ttu-id="73157-139">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="73157-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="73157-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="73157-140">ForeignType</span></span>  <br/> |<span data-ttu-id="73157-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="73157-141">xsd:token</span></span>  <br/> |<span data-ttu-id="73157-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="73157-142">required</span></span>  <br/> ||<span data-ttu-id="73157-143">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="73157-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="73157-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="73157-144">MappingMode</span></span>  <br/> |<span data-ttu-id="73157-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="73157-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="73157-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-146">optional</span></span>  <br/> ||<span data-ttu-id="73157-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="73157-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="73157-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="73157-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="73157-149">XSD: double</span><span class="sxs-lookup"><span data-stu-id="73157-149">xsd:double</span></span>  <br/> |<span data-ttu-id="73157-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-150">optional</span></span>  <br/> ||<span data-ttu-id="73157-151">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="73157-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="73157-152">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="73157-152">ObjectType</span></span>  <br/> |<span data-ttu-id="73157-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="73157-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="73157-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-154">optional</span></span>  <br/> ||<span data-ttu-id="73157-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="73157-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="73157-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="73157-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="73157-157">XSD: double</span><span class="sxs-lookup"><span data-stu-id="73157-157">xsd:double</span></span>  <br/> |<span data-ttu-id="73157-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-158">optional</span></span>  <br/> ||<span data-ttu-id="73157-159">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="73157-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="73157-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="73157-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="73157-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="73157-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="73157-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="73157-162">optional</span></span>  <br/> ||<span data-ttu-id="73157-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="73157-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

