---
title: ForeignData_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539865"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="e84fd-102">ForeignData_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="e84fd-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e84fd-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e84fd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e84fd-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e84fd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e84fd-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e84fd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e84fd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e84fd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e84fd-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e84fd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e84fd-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="e84fd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e84fd-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e84fd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e84fd-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e84fd-110">Elements and attributes</span></span>

<span data-ttu-id="e84fd-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e84fd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e84fd-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e84fd-112">Child elements</span></span>

|<span data-ttu-id="e84fd-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e84fd-113">**Element**</span></span>|<span data-ttu-id="e84fd-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e84fd-114">**Type**</span></span>|<span data-ttu-id="e84fd-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e84fd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e84fd-116">Rel</span><span class="sxs-lookup"><span data-stu-id="e84fd-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e84fd-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="e84fd-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e84fd-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e84fd-118">Attributes</span></span>

|<span data-ttu-id="e84fd-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e84fd-119">**Attribute**</span></span>|<span data-ttu-id="e84fd-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e84fd-120">**Type**</span></span>|<span data-ttu-id="e84fd-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e84fd-121">**Required**</span></span>|<span data-ttu-id="e84fd-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e84fd-122">**Description**</span></span>|<span data-ttu-id="e84fd-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e84fd-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e84fd-124">компрессионлевел</span><span class="sxs-lookup"><span data-stu-id="e84fd-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="e84fd-125">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="e84fd-125">xsd:double</span></span>  <br/> |<span data-ttu-id="e84fd-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-126">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-127">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="e84fd-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-128">компрессионтипе</span><span class="sxs-lookup"><span data-stu-id="e84fd-128">CompressionType</span></span>  <br/> |<span data-ttu-id="e84fd-129">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="e84fd-129">xsd:token</span></span>  <br/> |<span data-ttu-id="e84fd-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-130">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-131">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="e84fd-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-132">екстенткс</span><span class="sxs-lookup"><span data-stu-id="e84fd-132">ExtentX</span></span>  <br/> |<span data-ttu-id="e84fd-133">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="e84fd-133">xsd:double</span></span>  <br/> |<span data-ttu-id="e84fd-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-134">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-135">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="e84fd-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-136">Экстент</span><span class="sxs-lookup"><span data-stu-id="e84fd-136">ExtentY</span></span>  <br/> |<span data-ttu-id="e84fd-137">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="e84fd-137">xsd:double</span></span>  <br/> |<span data-ttu-id="e84fd-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-138">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-139">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="e84fd-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="e84fd-140">ForeignType</span></span>  <br/> |<span data-ttu-id="e84fd-141">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="e84fd-141">xsd:token</span></span>  <br/> |<span data-ttu-id="e84fd-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-142">required</span></span>  <br/> ||<span data-ttu-id="e84fd-143">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="e84fd-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-144">маппингмоде</span><span class="sxs-lookup"><span data-stu-id="e84fd-144">MappingMode</span></span>  <br/> |<span data-ttu-id="e84fd-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e84fd-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e84fd-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-146">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="e84fd-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-148">обжексеигхт</span><span class="sxs-lookup"><span data-stu-id="e84fd-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="e84fd-149">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="e84fd-149">xsd:double</span></span>  <br/> |<span data-ttu-id="e84fd-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-150">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-151">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="e84fd-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="e84fd-152">ObjectType</span></span>  <br/> |<span data-ttu-id="e84fd-153">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e84fd-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e84fd-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-154">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e84fd-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-156">обжектвидс</span><span class="sxs-lookup"><span data-stu-id="e84fd-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="e84fd-157">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="e84fd-157">xsd:double</span></span>  <br/> |<span data-ttu-id="e84fd-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-158">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-159">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="e84fd-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e84fd-160">шовасикон</span><span class="sxs-lookup"><span data-stu-id="e84fd-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="e84fd-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="e84fd-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e84fd-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="e84fd-162">optional</span></span>  <br/> ||<span data-ttu-id="e84fd-163">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e84fd-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

