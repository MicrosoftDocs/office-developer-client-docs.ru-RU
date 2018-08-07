---
title: ShapeSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814802"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="36e88-102">ShapeSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="36e88-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="36e88-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="36e88-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36e88-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="36e88-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36e88-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="36e88-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36e88-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36e88-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36e88-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="36e88-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36e88-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36e88-109">Определение</span><span class="sxs-lookup"><span data-stu-id="36e88-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36e88-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="36e88-110">Elements and attributes</span></span>

<span data-ttu-id="36e88-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="36e88-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36e88-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36e88-112">Child elements</span></span>

|<span data-ttu-id="36e88-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="36e88-113">**Element**</span></span>|<span data-ttu-id="36e88-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="36e88-114">**Type**</span></span>|<span data-ttu-id="36e88-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36e88-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36e88-116">Бд1</span><span class="sxs-lookup"><span data-stu-id="36e88-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e88-118">Бд2</span><span class="sxs-lookup"><span data-stu-id="36e88-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e88-120">Data3</span><span class="sxs-lookup"><span data-stu-id="36e88-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e88-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="36e88-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e88-124">Фигур</span><span class="sxs-lookup"><span data-stu-id="36e88-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="36e88-126">Text</span><span class="sxs-lookup"><span data-stu-id="36e88-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36e88-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="36e88-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36e88-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36e88-128">Attributes</span></span>

|<span data-ttu-id="36e88-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="36e88-129">**Attribute**</span></span>|<span data-ttu-id="36e88-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="36e88-130">**Type**</span></span>|<span data-ttu-id="36e88-131">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="36e88-131">**Required**</span></span>|<span data-ttu-id="36e88-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36e88-132">**Description**</span></span>|<span data-ttu-id="36e88-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="36e88-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="36e88-134">DEL</span><span class="sxs-lookup"><span data-stu-id="36e88-134">Del</span></span>  <br/> |<span data-ttu-id="36e88-135">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="36e88-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="36e88-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-136">optional</span></span>  <br/> ||<span data-ttu-id="36e88-137">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="36e88-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="36e88-138">ID</span><span class="sxs-lookup"><span data-stu-id="36e88-138">ID</span></span>  <br/> |<span data-ttu-id="36e88-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="36e88-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36e88-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-140">required</span></span>  <br/> ||<span data-ttu-id="36e88-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="36e88-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36e88-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="36e88-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="36e88-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="36e88-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="36e88-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-144">optional</span></span>  <br/> ||<span data-ttu-id="36e88-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="36e88-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="36e88-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="36e88-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="36e88-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="36e88-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="36e88-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-148">optional</span></span>  <br/> ||<span data-ttu-id="36e88-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="36e88-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="36e88-150">Master</span><span class="sxs-lookup"><span data-stu-id="36e88-150">Master</span></span>  <br/> |<span data-ttu-id="36e88-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="36e88-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36e88-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-152">optional</span></span>  <br/> ||<span data-ttu-id="36e88-153">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="36e88-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36e88-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="36e88-154">MasterShape</span></span>  <br/> |<span data-ttu-id="36e88-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="36e88-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36e88-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-156">optional</span></span>  <br/> ||<span data-ttu-id="36e88-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="36e88-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36e88-158">Имя</span><span class="sxs-lookup"><span data-stu-id="36e88-158">Name</span></span>  <br/> |<span data-ttu-id="36e88-159">XSD:String</span><span class="sxs-lookup"><span data-stu-id="36e88-159">xsd:string</span></span>  <br/> |<span data-ttu-id="36e88-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-160">optional</span></span>  <br/> ||<span data-ttu-id="36e88-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="36e88-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="36e88-162">NameU</span><span class="sxs-lookup"><span data-stu-id="36e88-162">NameU</span></span>  <br/> |<span data-ttu-id="36e88-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="36e88-163">xsd:string</span></span>  <br/> |<span data-ttu-id="36e88-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-164">optional</span></span>  <br/> ||<span data-ttu-id="36e88-165">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="36e88-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="36e88-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="36e88-166">OriginalID</span></span>  <br/> |<span data-ttu-id="36e88-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="36e88-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36e88-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-168">optional</span></span>  <br/> ||<span data-ttu-id="36e88-169">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="36e88-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36e88-170">Тип</span><span class="sxs-lookup"><span data-stu-id="36e88-170">Type</span></span>  <br/> |<span data-ttu-id="36e88-171">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="36e88-171">xsd:token</span></span>  <br/> |<span data-ttu-id="36e88-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-172">optional</span></span>  <br/> ||<span data-ttu-id="36e88-173">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="36e88-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="36e88-174">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="36e88-174">UniqueID</span></span>  <br/> |<span data-ttu-id="36e88-175">XSD:String</span><span class="sxs-lookup"><span data-stu-id="36e88-175">xsd:string</span></span>  <br/> |<span data-ttu-id="36e88-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="36e88-176">optional</span></span>  <br/> ||<span data-ttu-id="36e88-177">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="36e88-177">Values of the xsd:string type.</span></span>  <br/> |
   

