---
title: ForeignData_Type complexType (Visio XML)
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
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="ee832-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ee832-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ee832-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ee832-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee832-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ee832-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ee832-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ee832-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ee832-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ee832-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ee832-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ee832-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ee832-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ee832-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ee832-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ee832-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ee832-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee832-110">Elements and attributes</span></span>

<span data-ttu-id="ee832-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ee832-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ee832-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ee832-112">Child elements</span></span>

|<span data-ttu-id="ee832-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ee832-113">**Element**</span></span>|<span data-ttu-id="ee832-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ee832-114">**Type**</span></span>|<span data-ttu-id="ee832-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee832-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ee832-116">Rel</span><span class="sxs-lookup"><span data-stu-id="ee832-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee832-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ee832-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ee832-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee832-118">Attributes</span></span>

|<span data-ttu-id="ee832-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ee832-119">**Attribute**</span></span>|<span data-ttu-id="ee832-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ee832-120">**Type**</span></span>|<span data-ttu-id="ee832-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ee832-121">**Required**</span></span>|<span data-ttu-id="ee832-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee832-122">**Description**</span></span>|<span data-ttu-id="ee832-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ee832-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee832-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="ee832-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="ee832-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ee832-125">xsd:double</span></span>  <br/> |<span data-ttu-id="ee832-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-126">optional</span></span>  <br/> ||<span data-ttu-id="ee832-127">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ee832-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee832-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="ee832-128">CompressionType</span></span>  <br/> |<span data-ttu-id="ee832-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="ee832-129">xsd:token</span></span>  <br/> |<span data-ttu-id="ee832-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-130">optional</span></span>  <br/> ||<span data-ttu-id="ee832-131">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="ee832-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ee832-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="ee832-132">ExtentX</span></span>  <br/> |<span data-ttu-id="ee832-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ee832-133">xsd:double</span></span>  <br/> |<span data-ttu-id="ee832-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-134">optional</span></span>  <br/> ||<span data-ttu-id="ee832-135">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ee832-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee832-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="ee832-136">ExtentY</span></span>  <br/> |<span data-ttu-id="ee832-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ee832-137">xsd:double</span></span>  <br/> |<span data-ttu-id="ee832-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-138">optional</span></span>  <br/> ||<span data-ttu-id="ee832-139">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ee832-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee832-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="ee832-140">ForeignType</span></span>  <br/> |<span data-ttu-id="ee832-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="ee832-141">xsd:token</span></span>  <br/> |<span data-ttu-id="ee832-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-142">required</span></span>  <br/> ||<span data-ttu-id="ee832-143">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="ee832-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ee832-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="ee832-144">MappingMode</span></span>  <br/> |<span data-ttu-id="ee832-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ee832-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ee832-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-146">optional</span></span>  <br/> ||<span data-ttu-id="ee832-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ee832-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ee832-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="ee832-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="ee832-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ee832-149">xsd:double</span></span>  <br/> |<span data-ttu-id="ee832-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-150">optional</span></span>  <br/> ||<span data-ttu-id="ee832-151">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ee832-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee832-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="ee832-152">ObjectType</span></span>  <br/> |<span data-ttu-id="ee832-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ee832-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee832-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-154">optional</span></span>  <br/> ||<span data-ttu-id="ee832-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ee832-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee832-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="ee832-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="ee832-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="ee832-157">xsd:double</span></span>  <br/> |<span data-ttu-id="ee832-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-158">optional</span></span>  <br/> ||<span data-ttu-id="ee832-159">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="ee832-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee832-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="ee832-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="ee832-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ee832-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ee832-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee832-162">optional</span></span>  <br/> ||<span data-ttu-id="ee832-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ee832-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

