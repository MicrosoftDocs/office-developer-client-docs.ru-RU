---
title: DataRecordSet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813550"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="09227-102">DataRecordSet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="09227-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="09227-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="09227-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09227-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="09227-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09227-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="09227-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09227-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="09227-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09227-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="09227-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09227-108">Нет</span><span class="sxs-lookup"><span data-stu-id="09227-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09227-109">Определение</span><span class="sxs-lookup"><span data-stu-id="09227-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="09227-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="09227-110">Elements and attributes</span></span>

<span data-ttu-id="09227-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="09227-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09227-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09227-112">Child elements</span></span>

|<span data-ttu-id="09227-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="09227-113">**Element**</span></span>|<span data-ttu-id="09227-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="09227-114">**Type**</span></span>|<span data-ttu-id="09227-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09227-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09227-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="09227-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="09227-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="09227-118">Объектам DataColumn</span><span class="sxs-lookup"><span data-stu-id="09227-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="09227-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="09227-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="09227-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="09227-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="09227-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="09227-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="09227-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="09227-124">Rel</span><span class="sxs-lookup"><span data-stu-id="09227-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="09227-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="09227-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="09227-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09227-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="09227-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="09227-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="09227-128">Attributes</span></span>

|<span data-ttu-id="09227-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="09227-129">**Attribute**</span></span>|<span data-ttu-id="09227-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="09227-130">**Type**</span></span>|<span data-ttu-id="09227-131">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="09227-131">**Required**</span></span>|<span data-ttu-id="09227-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09227-132">**Description**</span></span>|<span data-ttu-id="09227-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="09227-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09227-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="09227-134">Checksum</span></span>  <br/> |<span data-ttu-id="09227-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-136">optional</span></span>  <br/> ||<span data-ttu-id="09227-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-138">Команда</span><span class="sxs-lookup"><span data-stu-id="09227-138">Command</span></span>  <br/> |<span data-ttu-id="09227-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="09227-139">xsd:string</span></span>  <br/> |<span data-ttu-id="09227-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-140">optional</span></span>  <br/> ||<span data-ttu-id="09227-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="09227-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09227-142">ConnectionID содержит</span><span class="sxs-lookup"><span data-stu-id="09227-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="09227-143">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-144">optional</span></span>  <br/> ||<span data-ttu-id="09227-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-146">ID</span><span class="sxs-lookup"><span data-stu-id="09227-146">ID</span></span>  <br/> |<span data-ttu-id="09227-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="09227-148">required</span></span>  <br/> ||<span data-ttu-id="09227-149">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-150">Имя</span><span class="sxs-lookup"><span data-stu-id="09227-150">Name</span></span>  <br/> |<span data-ttu-id="09227-151">XSD:String</span><span class="sxs-lookup"><span data-stu-id="09227-151">xsd:string</span></span>  <br/> |<span data-ttu-id="09227-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-152">optional</span></span>  <br/> ||<span data-ttu-id="09227-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="09227-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09227-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="09227-154">NextRowID</span></span>  <br/> |<span data-ttu-id="09227-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-156">optional</span></span>  <br/> ||<span data-ttu-id="09227-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-158">Options</span><span class="sxs-lookup"><span data-stu-id="09227-158">Options</span></span>  <br/> |<span data-ttu-id="09227-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-160">optional</span></span>  <br/> ||<span data-ttu-id="09227-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="09227-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="09227-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-164">optional</span></span>  <br/> ||<span data-ttu-id="09227-165">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="09227-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="09227-167">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="09227-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="09227-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-168">optional</span></span>  <br/> ||<span data-ttu-id="09227-169">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="09227-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="09227-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="09227-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="09227-171">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="09227-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="09227-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-172">optional</span></span>  <br/> ||<span data-ttu-id="09227-173">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="09227-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="09227-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="09227-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="09227-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09227-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09227-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-176">optional</span></span>  <br/> ||<span data-ttu-id="09227-177">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09227-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09227-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="09227-178">RowOrder</span></span>  <br/> |<span data-ttu-id="09227-179">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="09227-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="09227-180">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-180">optional</span></span>  <br/> ||<span data-ttu-id="09227-181">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="09227-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="09227-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="09227-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="09227-183">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="09227-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="09227-184">необязательный</span><span class="sxs-lookup"><span data-stu-id="09227-184">optional</span></span>  <br/> ||<span data-ttu-id="09227-185">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="09227-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

