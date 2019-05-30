---
title: Фореигндата_типе complexType (XML для Visio)
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
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="a0c8a-102">Фореигндата_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="a0c8a-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a0c8a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a0c8a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0c8a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a0c8a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a0c8a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a0c8a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a0c8a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a0c8a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a0c8a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0c8a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a0c8a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a0c8a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a0c8a-110">Elements and attributes</span></span>

<span data-ttu-id="a0c8a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a0c8a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a0c8a-112">Child elements</span></span>

|<span data-ttu-id="a0c8a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-113">**Element**</span></span>|<span data-ttu-id="a0c8a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-114">**Type**</span></span>|<span data-ttu-id="a0c8a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0c8a-116">Rel</span><span class="sxs-lookup"><span data-stu-id="a0c8a-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0c8a-117">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="a0c8a-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a0c8a-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a0c8a-118">Attributes</span></span>

|<span data-ttu-id="a0c8a-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-119">**Attribute**</span></span>|<span data-ttu-id="a0c8a-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-120">**Type**</span></span>|<span data-ttu-id="a0c8a-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-121">**Required**</span></span>|<span data-ttu-id="a0c8a-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-122">**Description**</span></span>|<span data-ttu-id="a0c8a-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a0c8a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a0c8a-124">Компрессионлевел</span><span class="sxs-lookup"><span data-stu-id="a0c8a-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="a0c8a-125">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a0c8a-125">xsd:double</span></span>  <br/> |<span data-ttu-id="a0c8a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-126">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-127">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-128">Компрессионтипе</span><span class="sxs-lookup"><span data-stu-id="a0c8a-128">CompressionType</span></span>  <br/> |<span data-ttu-id="a0c8a-129">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="a0c8a-129">xsd:token</span></span>  <br/> |<span data-ttu-id="a0c8a-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-130">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-131">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-132">Екстенткс</span><span class="sxs-lookup"><span data-stu-id="a0c8a-132">ExtentX</span></span>  <br/> |<span data-ttu-id="a0c8a-133">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a0c8a-133">xsd:double</span></span>  <br/> |<span data-ttu-id="a0c8a-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-134">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-135">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-136">Экстент</span><span class="sxs-lookup"><span data-stu-id="a0c8a-136">ExtentY</span></span>  <br/> |<span data-ttu-id="a0c8a-137">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a0c8a-137">xsd:double</span></span>  <br/> |<span data-ttu-id="a0c8a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-138">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-139">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="a0c8a-140">ForeignType</span></span>  <br/> |<span data-ttu-id="a0c8a-141">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="a0c8a-141">xsd:token</span></span>  <br/> |<span data-ttu-id="a0c8a-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-142">required</span></span>  <br/> ||<span data-ttu-id="a0c8a-143">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-144">Маппингмоде</span><span class="sxs-lookup"><span data-stu-id="a0c8a-144">MappingMode</span></span>  <br/> |<span data-ttu-id="a0c8a-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a0c8a-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a0c8a-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-146">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-148">Обжексеигхт</span><span class="sxs-lookup"><span data-stu-id="a0c8a-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="a0c8a-149">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a0c8a-149">xsd:double</span></span>  <br/> |<span data-ttu-id="a0c8a-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-150">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-151">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="a0c8a-152">ObjectType</span></span>  <br/> |<span data-ttu-id="a0c8a-153">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a0c8a-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a0c8a-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-154">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-156">Обжектвидс</span><span class="sxs-lookup"><span data-stu-id="a0c8a-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="a0c8a-157">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="a0c8a-157">xsd:double</span></span>  <br/> |<span data-ttu-id="a0c8a-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-158">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-159">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a0c8a-160">Шовасикон</span><span class="sxs-lookup"><span data-stu-id="a0c8a-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="a0c8a-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="a0c8a-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a0c8a-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="a0c8a-162">optional</span></span>  <br/> ||<span data-ttu-id="a0c8a-163">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a0c8a-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

