---
title: Фореигндата_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346013"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="c1243-102">Фореигндата_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c1243-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c1243-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c1243-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1243-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c1243-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c1243-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c1243-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c1243-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c1243-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c1243-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="c1243-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c1243-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="c1243-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1243-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c1243-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c1243-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c1243-110">Elements and attributes</span></span>

<span data-ttu-id="c1243-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c1243-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c1243-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c1243-112">Child elements</span></span>

|<span data-ttu-id="c1243-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c1243-113">**Element**</span></span>|<span data-ttu-id="c1243-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c1243-114">**Type**</span></span>|<span data-ttu-id="c1243-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1243-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1243-116">Rel</span><span class="sxs-lookup"><span data-stu-id="c1243-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1243-117">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="c1243-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c1243-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c1243-118">Attributes</span></span>

|<span data-ttu-id="c1243-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c1243-119">**Attribute**</span></span>|<span data-ttu-id="c1243-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c1243-120">**Type**</span></span>|<span data-ttu-id="c1243-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c1243-121">**Required**</span></span>|<span data-ttu-id="c1243-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1243-122">**Description**</span></span>|<span data-ttu-id="c1243-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c1243-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1243-124">Компрессионлевел</span><span class="sxs-lookup"><span data-stu-id="c1243-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="c1243-125">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c1243-125">xsd:double</span></span>  <br/> |<span data-ttu-id="c1243-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-126">optional</span></span>  <br/> ||<span data-ttu-id="c1243-127">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="c1243-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c1243-128">Компрессионтипе</span><span class="sxs-lookup"><span data-stu-id="c1243-128">CompressionType</span></span>  <br/> |<span data-ttu-id="c1243-129">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="c1243-129">xsd:token</span></span>  <br/> |<span data-ttu-id="c1243-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-130">optional</span></span>  <br/> ||<span data-ttu-id="c1243-131">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="c1243-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c1243-132">Екстенткс</span><span class="sxs-lookup"><span data-stu-id="c1243-132">ExtentX</span></span>  <br/> |<span data-ttu-id="c1243-133">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c1243-133">xsd:double</span></span>  <br/> |<span data-ttu-id="c1243-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-134">optional</span></span>  <br/> ||<span data-ttu-id="c1243-135">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="c1243-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c1243-136">Экстент</span><span class="sxs-lookup"><span data-stu-id="c1243-136">ExtentY</span></span>  <br/> |<span data-ttu-id="c1243-137">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c1243-137">xsd:double</span></span>  <br/> |<span data-ttu-id="c1243-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-138">optional</span></span>  <br/> ||<span data-ttu-id="c1243-139">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="c1243-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c1243-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="c1243-140">ForeignType</span></span>  <br/> |<span data-ttu-id="c1243-141">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="c1243-141">xsd:token</span></span>  <br/> |<span data-ttu-id="c1243-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-142">required</span></span>  <br/> ||<span data-ttu-id="c1243-143">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="c1243-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c1243-144">Маппингмоде</span><span class="sxs-lookup"><span data-stu-id="c1243-144">MappingMode</span></span>  <br/> |<span data-ttu-id="c1243-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c1243-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c1243-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-146">optional</span></span>  <br/> ||<span data-ttu-id="c1243-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c1243-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c1243-148">Обжексеигхт</span><span class="sxs-lookup"><span data-stu-id="c1243-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="c1243-149">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c1243-149">xsd:double</span></span>  <br/> |<span data-ttu-id="c1243-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-150">optional</span></span>  <br/> ||<span data-ttu-id="c1243-151">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="c1243-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c1243-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="c1243-152">ObjectType</span></span>  <br/> |<span data-ttu-id="c1243-153">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c1243-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1243-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-154">optional</span></span>  <br/> ||<span data-ttu-id="c1243-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c1243-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c1243-156">Обжектвидс</span><span class="sxs-lookup"><span data-stu-id="c1243-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="c1243-157">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="c1243-157">xsd:double</span></span>  <br/> |<span data-ttu-id="c1243-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-158">optional</span></span>  <br/> ||<span data-ttu-id="c1243-159">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="c1243-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c1243-160">Шовасикон</span><span class="sxs-lookup"><span data-stu-id="c1243-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="c1243-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="c1243-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c1243-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="c1243-162">optional</span></span>  <br/> ||<span data-ttu-id="c1243-163">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="c1243-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

