---
title: Шапешит_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542060"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="72fc4-102">Шапешит_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="72fc4-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="72fc4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="72fc4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72fc4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="72fc4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72fc4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="72fc4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72fc4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="72fc4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72fc4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="72fc4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72fc4-108">Шит_типе</span><span class="sxs-lookup"><span data-stu-id="72fc4-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72fc4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="72fc4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="72fc4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="72fc4-110">Elements and attributes</span></span>

<span data-ttu-id="72fc4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="72fc4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72fc4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="72fc4-112">Child elements</span></span>

|<span data-ttu-id="72fc4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="72fc4-113">**Element**</span></span>|<span data-ttu-id="72fc4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72fc4-114">**Type**</span></span>|<span data-ttu-id="72fc4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72fc4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72fc4-116">Data1</span><span class="sxs-lookup"><span data-stu-id="72fc4-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="72fc4-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="72fc4-118">Data2</span><span class="sxs-lookup"><span data-stu-id="72fc4-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="72fc4-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="72fc4-120">Data3</span><span class="sxs-lookup"><span data-stu-id="72fc4-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="72fc4-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="72fc4-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="72fc4-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-123">Фореигндата_типе</span><span class="sxs-lookup"><span data-stu-id="72fc4-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="72fc4-124">Фигуры</span><span class="sxs-lookup"><span data-stu-id="72fc4-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-125">Шапес_типе</span><span class="sxs-lookup"><span data-stu-id="72fc4-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="72fc4-126">Text</span><span class="sxs-lookup"><span data-stu-id="72fc4-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72fc4-127">Текст_типе</span><span class="sxs-lookup"><span data-stu-id="72fc4-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="72fc4-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="72fc4-128">Attributes</span></span>

|<span data-ttu-id="72fc4-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="72fc4-129">**Attribute**</span></span>|<span data-ttu-id="72fc4-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72fc4-130">**Type**</span></span>|<span data-ttu-id="72fc4-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="72fc4-131">**Required**</span></span>|<span data-ttu-id="72fc4-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72fc4-132">**Description**</span></span>|<span data-ttu-id="72fc4-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="72fc4-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="72fc4-134">Del</span><span class="sxs-lookup"><span data-stu-id="72fc4-134">Del</span></span>  <br/> |<span data-ttu-id="72fc4-135">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="72fc4-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="72fc4-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-136">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-137">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="72fc4-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-138">ID</span><span class="sxs-lookup"><span data-stu-id="72fc4-138">ID</span></span>  <br/> |<span data-ttu-id="72fc4-139">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="72fc4-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72fc4-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-140">required</span></span>  <br/> ||<span data-ttu-id="72fc4-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="72fc4-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-142">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="72fc4-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="72fc4-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="72fc4-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="72fc4-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-144">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="72fc4-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-146">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="72fc4-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="72fc4-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="72fc4-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="72fc4-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-148">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-149">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="72fc4-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-150">Master</span><span class="sxs-lookup"><span data-stu-id="72fc4-150">Master</span></span>  <br/> |<span data-ttu-id="72fc4-151">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="72fc4-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72fc4-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-152">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-153">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="72fc4-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="72fc4-154">MasterShape</span></span>  <br/> |<span data-ttu-id="72fc4-155">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="72fc4-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72fc4-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-156">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-157">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="72fc4-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-158">Имя</span><span class="sxs-lookup"><span data-stu-id="72fc4-158">Name</span></span>  <br/> |<span data-ttu-id="72fc4-159">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="72fc4-159">xsd:string</span></span>  <br/> |<span data-ttu-id="72fc4-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-160">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="72fc4-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-162">NameU</span><span class="sxs-lookup"><span data-stu-id="72fc4-162">NameU</span></span>  <br/> |<span data-ttu-id="72fc4-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="72fc4-163">xsd:string</span></span>  <br/> |<span data-ttu-id="72fc4-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-164">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-165">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="72fc4-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-166">Оригиналид</span><span class="sxs-lookup"><span data-stu-id="72fc4-166">OriginalID</span></span>  <br/> |<span data-ttu-id="72fc4-167">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="72fc4-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="72fc4-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-168">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-169">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="72fc4-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-170">Тип</span><span class="sxs-lookup"><span data-stu-id="72fc4-170">Type</span></span>  <br/> |<span data-ttu-id="72fc4-171">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="72fc4-171">xsd:token</span></span>  <br/> |<span data-ttu-id="72fc4-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-172">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-173">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="72fc4-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="72fc4-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="72fc4-174">UniqueID</span></span>  <br/> |<span data-ttu-id="72fc4-175">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="72fc4-175">xsd:string</span></span>  <br/> |<span data-ttu-id="72fc4-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="72fc4-176">optional</span></span>  <br/> ||<span data-ttu-id="72fc4-177">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="72fc4-177">Values of the xsd:string type.</span></span>  <br/> |
   

