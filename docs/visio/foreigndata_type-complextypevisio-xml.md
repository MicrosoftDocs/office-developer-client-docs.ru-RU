---
title: ForeignData_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813819"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="8f3fc-102">ForeignData_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="8f3fc-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8f3fc-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8f3fc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f3fc-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8f3fc-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8f3fc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8f3fc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8f3fc-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8f3fc-108">Нет</span><span class="sxs-lookup"><span data-stu-id="8f3fc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f3fc-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8f3fc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8f3fc-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f3fc-110">Elements and attributes</span></span>

<span data-ttu-id="8f3fc-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8f3fc-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8f3fc-112">Child elements</span></span>

|<span data-ttu-id="8f3fc-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-113">**Element**</span></span>|<span data-ttu-id="8f3fc-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-114">**Type**</span></span>|<span data-ttu-id="8f3fc-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f3fc-116">Rel</span><span class="sxs-lookup"><span data-stu-id="8f3fc-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f3fc-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="8f3fc-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8f3fc-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f3fc-118">Attributes</span></span>

|<span data-ttu-id="8f3fc-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-119">**Attribute**</span></span>|<span data-ttu-id="8f3fc-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-120">**Type**</span></span>|<span data-ttu-id="8f3fc-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-121">**Required**</span></span>|<span data-ttu-id="8f3fc-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-122">**Description**</span></span>|<span data-ttu-id="8f3fc-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8f3fc-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8f3fc-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="8f3fc-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="8f3fc-125">XSD: double</span><span class="sxs-lookup"><span data-stu-id="8f3fc-125">xsd:double</span></span>  <br/> |<span data-ttu-id="8f3fc-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-126">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-127">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="8f3fc-128">CompressionType</span></span>  <br/> |<span data-ttu-id="8f3fc-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="8f3fc-129">xsd:token</span></span>  <br/> |<span data-ttu-id="8f3fc-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-130">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-131">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="8f3fc-132">ExtentX</span></span>  <br/> |<span data-ttu-id="8f3fc-133">XSD: double</span><span class="sxs-lookup"><span data-stu-id="8f3fc-133">xsd:double</span></span>  <br/> |<span data-ttu-id="8f3fc-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-134">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-135">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="8f3fc-136">ExtentY</span></span>  <br/> |<span data-ttu-id="8f3fc-137">XSD: double</span><span class="sxs-lookup"><span data-stu-id="8f3fc-137">xsd:double</span></span>  <br/> |<span data-ttu-id="8f3fc-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-138">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-139">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="8f3fc-140">ForeignType</span></span>  <br/> |<span data-ttu-id="8f3fc-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="8f3fc-141">xsd:token</span></span>  <br/> |<span data-ttu-id="8f3fc-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-142">required</span></span>  <br/> ||<span data-ttu-id="8f3fc-143">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="8f3fc-144">MappingMode</span></span>  <br/> |<span data-ttu-id="8f3fc-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8f3fc-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8f3fc-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-146">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-147">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="8f3fc-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="8f3fc-149">XSD: double</span><span class="sxs-lookup"><span data-stu-id="8f3fc-149">xsd:double</span></span>  <br/> |<span data-ttu-id="8f3fc-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-150">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-151">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-152">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="8f3fc-152">ObjectType</span></span>  <br/> |<span data-ttu-id="8f3fc-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f3fc-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f3fc-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-154">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="8f3fc-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="8f3fc-157">XSD: double</span><span class="sxs-lookup"><span data-stu-id="8f3fc-157">xsd:double</span></span>  <br/> |<span data-ttu-id="8f3fc-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-158">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-159">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="8f3fc-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="8f3fc-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="8f3fc-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8f3fc-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f3fc-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f3fc-162">optional</span></span>  <br/> ||<span data-ttu-id="8f3fc-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f3fc-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

