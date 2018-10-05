---
title: DataRecordSet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395478"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="5879e-102">DataRecordSet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5879e-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5879e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5879e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5879e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5879e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5879e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5879e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5879e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5879e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5879e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="5879e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5879e-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="5879e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5879e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="5879e-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5879e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5879e-110">Elements and attributes</span></span>

<span data-ttu-id="5879e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5879e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5879e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5879e-112">Child elements</span></span>

|<span data-ttu-id="5879e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5879e-113">**Element**</span></span>|<span data-ttu-id="5879e-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5879e-114">**Type**</span></span>|<span data-ttu-id="5879e-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5879e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5879e-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="5879e-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5879e-118">Объектам DataColumn</span><span class="sxs-lookup"><span data-stu-id="5879e-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5879e-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5879e-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5879e-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="5879e-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5879e-124">Rel</span><span class="sxs-lookup"><span data-stu-id="5879e-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5879e-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="5879e-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5879e-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="5879e-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5879e-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5879e-128">Attributes</span></span>

|<span data-ttu-id="5879e-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5879e-129">**Attribute**</span></span>|<span data-ttu-id="5879e-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5879e-130">**Type**</span></span>|<span data-ttu-id="5879e-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5879e-131">**Required**</span></span>|<span data-ttu-id="5879e-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5879e-132">**Description**</span></span>|<span data-ttu-id="5879e-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5879e-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5879e-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5879e-134">Checksum</span></span>  <br/> |<span data-ttu-id="5879e-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-136">optional</span></span>  <br/> ||<span data-ttu-id="5879e-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-138">Команда</span><span class="sxs-lookup"><span data-stu-id="5879e-138">Command</span></span>  <br/> |<span data-ttu-id="5879e-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5879e-139">xsd:string</span></span>  <br/> |<span data-ttu-id="5879e-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-140">optional</span></span>  <br/> ||<span data-ttu-id="5879e-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5879e-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5879e-142">ConnectionID содержит</span><span class="sxs-lookup"><span data-stu-id="5879e-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="5879e-143">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-144">optional</span></span>  <br/> ||<span data-ttu-id="5879e-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-146">ID</span><span class="sxs-lookup"><span data-stu-id="5879e-146">ID</span></span>  <br/> |<span data-ttu-id="5879e-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-148">required</span></span>  <br/> ||<span data-ttu-id="5879e-149">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-150">Имя</span><span class="sxs-lookup"><span data-stu-id="5879e-150">Name</span></span>  <br/> |<span data-ttu-id="5879e-151">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5879e-151">xsd:string</span></span>  <br/> |<span data-ttu-id="5879e-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-152">optional</span></span>  <br/> ||<span data-ttu-id="5879e-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5879e-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5879e-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="5879e-154">NextRowID</span></span>  <br/> |<span data-ttu-id="5879e-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-156">optional</span></span>  <br/> ||<span data-ttu-id="5879e-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-158">Options</span><span class="sxs-lookup"><span data-stu-id="5879e-158">Options</span></span>  <br/> |<span data-ttu-id="5879e-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-160">optional</span></span>  <br/> ||<span data-ttu-id="5879e-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="5879e-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="5879e-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-164">optional</span></span>  <br/> ||<span data-ttu-id="5879e-165">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="5879e-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="5879e-167">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5879e-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5879e-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-168">optional</span></span>  <br/> ||<span data-ttu-id="5879e-169">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5879e-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5879e-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="5879e-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="5879e-171">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5879e-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5879e-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-172">optional</span></span>  <br/> ||<span data-ttu-id="5879e-173">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5879e-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5879e-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="5879e-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="5879e-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5879e-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5879e-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-176">optional</span></span>  <br/> ||<span data-ttu-id="5879e-177">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5879e-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5879e-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="5879e-178">RowOrder</span></span>  <br/> |<span data-ttu-id="5879e-179">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5879e-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5879e-180">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-180">optional</span></span>  <br/> ||<span data-ttu-id="5879e-181">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5879e-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5879e-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="5879e-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="5879e-183">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="5879e-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5879e-184">необязательный</span><span class="sxs-lookup"><span data-stu-id="5879e-184">optional</span></span>  <br/> ||<span data-ttu-id="5879e-185">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="5879e-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

