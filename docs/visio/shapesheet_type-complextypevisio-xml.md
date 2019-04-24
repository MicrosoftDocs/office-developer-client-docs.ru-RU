---
title: Шапешит_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349135"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ec78c-102">Шапешит_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ec78c-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec78c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ec78c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec78c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ec78c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec78c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ec78c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec78c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec78c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec78c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ec78c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec78c-108">Шит_типе</span><span class="sxs-lookup"><span data-stu-id="ec78c-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec78c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ec78c-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ec78c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec78c-110">Elements and attributes</span></span>

<span data-ttu-id="ec78c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ec78c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec78c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec78c-112">Child elements</span></span>

|<span data-ttu-id="ec78c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ec78c-113">**Element**</span></span>|<span data-ttu-id="ec78c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec78c-114">**Type**</span></span>|<span data-ttu-id="ec78c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec78c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec78c-116">Data1</span><span class="sxs-lookup"><span data-stu-id="ec78c-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="ec78c-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec78c-118">Data2</span><span class="sxs-lookup"><span data-stu-id="ec78c-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="ec78c-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec78c-120">Data3</span><span class="sxs-lookup"><span data-stu-id="ec78c-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="ec78c-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec78c-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="ec78c-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-123">Фореигндата_типе</span><span class="sxs-lookup"><span data-stu-id="ec78c-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec78c-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="ec78c-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-125">Шапес_типе</span><span class="sxs-lookup"><span data-stu-id="ec78c-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec78c-126">Text</span><span class="sxs-lookup"><span data-stu-id="ec78c-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec78c-127">Текст_типе</span><span class="sxs-lookup"><span data-stu-id="ec78c-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec78c-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec78c-128">Attributes</span></span>

|<span data-ttu-id="ec78c-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ec78c-129">**Attribute**</span></span>|<span data-ttu-id="ec78c-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec78c-130">**Type**</span></span>|<span data-ttu-id="ec78c-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ec78c-131">**Required**</span></span>|<span data-ttu-id="ec78c-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec78c-132">**Description**</span></span>|<span data-ttu-id="ec78c-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ec78c-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec78c-134">Del</span><span class="sxs-lookup"><span data-stu-id="ec78c-134">Del</span></span>  <br/> |<span data-ttu-id="ec78c-135">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec78c-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec78c-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-136">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-137">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec78c-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-138">ИД</span><span class="sxs-lookup"><span data-stu-id="ec78c-138">ID</span></span>  <br/> |<span data-ttu-id="ec78c-139">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec78c-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec78c-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-140">required</span></span>  <br/> ||<span data-ttu-id="ec78c-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec78c-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-142">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="ec78c-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="ec78c-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec78c-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec78c-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-144">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec78c-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-146">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="ec78c-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ec78c-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec78c-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec78c-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-148">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-149">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec78c-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-150">Master</span><span class="sxs-lookup"><span data-stu-id="ec78c-150">Master</span></span>  <br/> |<span data-ttu-id="ec78c-151">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec78c-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec78c-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-152">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-153">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec78c-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="ec78c-154">MasterShape</span></span>  <br/> |<span data-ttu-id="ec78c-155">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec78c-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec78c-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-156">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-157">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec78c-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-158">Имя</span><span class="sxs-lookup"><span data-stu-id="ec78c-158">Name</span></span>  <br/> |<span data-ttu-id="ec78c-159">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec78c-159">xsd:string</span></span>  <br/> |<span data-ttu-id="ec78c-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-160">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec78c-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-162">NameU</span><span class="sxs-lookup"><span data-stu-id="ec78c-162">NameU</span></span>  <br/> |<span data-ttu-id="ec78c-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec78c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ec78c-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-164">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-165">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec78c-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-166">Оригиналид</span><span class="sxs-lookup"><span data-stu-id="ec78c-166">OriginalID</span></span>  <br/> |<span data-ttu-id="ec78c-167">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec78c-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec78c-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-168">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-169">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec78c-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-170">Тип</span><span class="sxs-lookup"><span data-stu-id="ec78c-170">Type</span></span>  <br/> |<span data-ttu-id="ec78c-171">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="ec78c-171">xsd:token</span></span>  <br/> |<span data-ttu-id="ec78c-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-172">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-173">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="ec78c-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ec78c-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ec78c-174">UniqueID</span></span>  <br/> |<span data-ttu-id="ec78c-175">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec78c-175">xsd:string</span></span>  <br/> |<span data-ttu-id="ec78c-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec78c-176">optional</span></span>  <br/> ||<span data-ttu-id="ec78c-177">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec78c-177">Values of the xsd:string type.</span></span>  <br/> |
   

