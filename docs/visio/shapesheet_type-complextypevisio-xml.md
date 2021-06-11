---
title: ShapeSheet_Type ComplexType (Visio XML)
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
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="be236-102">ShapeSheet_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="be236-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="be236-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="be236-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be236-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="be236-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="be236-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="be236-105">**Schema file**</span></span> <br/> |<span data-ttu-id="be236-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="be236-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="be236-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="be236-107">**Extension base**</span></span> <br/> |<span data-ttu-id="be236-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="be236-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be236-109">Определение</span><span class="sxs-lookup"><span data-stu-id="be236-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="be236-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="be236-110">Elements and attributes</span></span>

<span data-ttu-id="be236-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="be236-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="be236-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="be236-112">Child elements</span></span>

|<span data-ttu-id="be236-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="be236-113">**Element**</span></span>|<span data-ttu-id="be236-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="be236-114">**Type**</span></span>|<span data-ttu-id="be236-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be236-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be236-116">Data1</span><span class="sxs-lookup"><span data-stu-id="be236-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="be236-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be236-118">Data2</span><span class="sxs-lookup"><span data-stu-id="be236-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="be236-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be236-120">Data3</span><span class="sxs-lookup"><span data-stu-id="be236-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="be236-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be236-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="be236-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="be236-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be236-124">Фигуры</span><span class="sxs-lookup"><span data-stu-id="be236-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="be236-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be236-126">Text</span><span class="sxs-lookup"><span data-stu-id="be236-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be236-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="be236-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="be236-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be236-128">Attributes</span></span>

|<span data-ttu-id="be236-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="be236-129">**Attribute**</span></span>|<span data-ttu-id="be236-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="be236-130">**Type**</span></span>|<span data-ttu-id="be236-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="be236-131">**Required**</span></span>|<span data-ttu-id="be236-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be236-132">**Description**</span></span>|<span data-ttu-id="be236-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="be236-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="be236-134">Del</span><span class="sxs-lookup"><span data-stu-id="be236-134">Del</span></span>  <br/> |<span data-ttu-id="be236-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="be236-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="be236-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-136">optional</span></span>  <br/> ||<span data-ttu-id="be236-137">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="be236-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="be236-138">ID</span><span class="sxs-lookup"><span data-stu-id="be236-138">ID</span></span>  <br/> |<span data-ttu-id="be236-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="be236-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="be236-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="be236-140">required</span></span>  <br/> ||<span data-ttu-id="be236-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="be236-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="be236-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="be236-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="be236-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="be236-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="be236-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-144">optional</span></span>  <br/> ||<span data-ttu-id="be236-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="be236-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="be236-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="be236-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="be236-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="be236-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="be236-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-148">optional</span></span>  <br/> ||<span data-ttu-id="be236-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="be236-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="be236-150">Master</span><span class="sxs-lookup"><span data-stu-id="be236-150">Master</span></span>  <br/> |<span data-ttu-id="be236-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="be236-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="be236-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-152">optional</span></span>  <br/> ||<span data-ttu-id="be236-153">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="be236-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="be236-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="be236-154">MasterShape</span></span>  <br/> |<span data-ttu-id="be236-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="be236-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="be236-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-156">optional</span></span>  <br/> ||<span data-ttu-id="be236-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="be236-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="be236-158">Имя</span><span class="sxs-lookup"><span data-stu-id="be236-158">Name</span></span>  <br/> |<span data-ttu-id="be236-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="be236-159">xsd:string</span></span>  <br/> |<span data-ttu-id="be236-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-160">optional</span></span>  <br/> ||<span data-ttu-id="be236-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="be236-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="be236-162">NameU</span><span class="sxs-lookup"><span data-stu-id="be236-162">NameU</span></span>  <br/> |<span data-ttu-id="be236-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="be236-163">xsd:string</span></span>  <br/> |<span data-ttu-id="be236-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-164">optional</span></span>  <br/> ||<span data-ttu-id="be236-165">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="be236-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="be236-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="be236-166">OriginalID</span></span>  <br/> |<span data-ttu-id="be236-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="be236-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="be236-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-168">optional</span></span>  <br/> ||<span data-ttu-id="be236-169">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="be236-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="be236-170">Тип</span><span class="sxs-lookup"><span data-stu-id="be236-170">Type</span></span>  <br/> |<span data-ttu-id="be236-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="be236-171">xsd:token</span></span>  <br/> |<span data-ttu-id="be236-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-172">optional</span></span>  <br/> ||<span data-ttu-id="be236-173">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="be236-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="be236-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="be236-174">UniqueID</span></span>  <br/> |<span data-ttu-id="be236-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="be236-175">xsd:string</span></span>  <br/> |<span data-ttu-id="be236-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="be236-176">optional</span></span>  <br/> ||<span data-ttu-id="be236-177">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="be236-177">Values of the xsd:string type.</span></span>  <br/> |
   

