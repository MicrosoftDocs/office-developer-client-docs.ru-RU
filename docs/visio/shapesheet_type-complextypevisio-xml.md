---
title: ShapeSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383634"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="af766-102">ShapeSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="af766-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="af766-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="af766-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af766-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="af766-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="af766-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="af766-105">**Schema file**</span></span> <br/> |<span data-ttu-id="af766-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="af766-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="af766-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="af766-107">**Extension base**</span></span> <br/> |<span data-ttu-id="af766-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="af766-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="af766-109">Определение</span><span class="sxs-lookup"><span data-stu-id="af766-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="af766-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="af766-110">Elements and attributes</span></span>

<span data-ttu-id="af766-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="af766-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="af766-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="af766-112">Child elements</span></span>

|<span data-ttu-id="af766-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="af766-113">**Element**</span></span>|<span data-ttu-id="af766-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="af766-114">**Type**</span></span>|<span data-ttu-id="af766-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="af766-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="af766-116">Бд1</span><span class="sxs-lookup"><span data-stu-id="af766-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="af766-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af766-118">Бд2</span><span class="sxs-lookup"><span data-stu-id="af766-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="af766-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af766-120">Data3</span><span class="sxs-lookup"><span data-stu-id="af766-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="af766-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af766-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="af766-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="af766-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af766-124">Фигур</span><span class="sxs-lookup"><span data-stu-id="af766-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="af766-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="af766-126">Text</span><span class="sxs-lookup"><span data-stu-id="af766-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="af766-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="af766-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="af766-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="af766-128">Attributes</span></span>

|<span data-ttu-id="af766-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="af766-129">**Attribute**</span></span>|<span data-ttu-id="af766-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="af766-130">**Type**</span></span>|<span data-ttu-id="af766-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="af766-131">**Required**</span></span>|<span data-ttu-id="af766-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="af766-132">**Description**</span></span>|<span data-ttu-id="af766-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="af766-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af766-134">DEL</span><span class="sxs-lookup"><span data-stu-id="af766-134">Del</span></span>  <br/> |<span data-ttu-id="af766-135">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="af766-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af766-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-136">optional</span></span>  <br/> ||<span data-ttu-id="af766-137">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="af766-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af766-138">ID</span><span class="sxs-lookup"><span data-stu-id="af766-138">ID</span></span>  <br/> |<span data-ttu-id="af766-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af766-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af766-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="af766-140">required</span></span>  <br/> ||<span data-ttu-id="af766-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af766-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af766-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="af766-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="af766-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="af766-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af766-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-144">optional</span></span>  <br/> ||<span data-ttu-id="af766-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="af766-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af766-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="af766-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="af766-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="af766-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="af766-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-148">optional</span></span>  <br/> ||<span data-ttu-id="af766-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="af766-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="af766-150">Master</span><span class="sxs-lookup"><span data-stu-id="af766-150">Master</span></span>  <br/> |<span data-ttu-id="af766-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af766-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af766-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-152">optional</span></span>  <br/> ||<span data-ttu-id="af766-153">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af766-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af766-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="af766-154">MasterShape</span></span>  <br/> |<span data-ttu-id="af766-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af766-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af766-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-156">optional</span></span>  <br/> ||<span data-ttu-id="af766-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af766-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af766-158">Имя</span><span class="sxs-lookup"><span data-stu-id="af766-158">Name</span></span>  <br/> |<span data-ttu-id="af766-159">XSD:String</span><span class="sxs-lookup"><span data-stu-id="af766-159">xsd:string</span></span>  <br/> |<span data-ttu-id="af766-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-160">optional</span></span>  <br/> ||<span data-ttu-id="af766-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="af766-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="af766-162">NameU</span><span class="sxs-lookup"><span data-stu-id="af766-162">NameU</span></span>  <br/> |<span data-ttu-id="af766-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="af766-163">xsd:string</span></span>  <br/> |<span data-ttu-id="af766-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-164">optional</span></span>  <br/> ||<span data-ttu-id="af766-165">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="af766-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="af766-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="af766-166">OriginalID</span></span>  <br/> |<span data-ttu-id="af766-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="af766-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="af766-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-168">optional</span></span>  <br/> ||<span data-ttu-id="af766-169">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="af766-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="af766-170">Тип</span><span class="sxs-lookup"><span data-stu-id="af766-170">Type</span></span>  <br/> |<span data-ttu-id="af766-171">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="af766-171">xsd:token</span></span>  <br/> |<span data-ttu-id="af766-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-172">optional</span></span>  <br/> ||<span data-ttu-id="af766-173">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="af766-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="af766-174">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="af766-174">UniqueID</span></span>  <br/> |<span data-ttu-id="af766-175">XSD:String</span><span class="sxs-lookup"><span data-stu-id="af766-175">xsd:string</span></span>  <br/> |<span data-ttu-id="af766-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="af766-176">optional</span></span>  <br/> ||<span data-ttu-id="af766-177">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="af766-177">Values of the xsd:string type.</span></span>  <br/> |
   

