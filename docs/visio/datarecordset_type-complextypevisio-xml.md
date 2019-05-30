---
title: Датарекордсет_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 132261ae823d1749676b7bdc28cdd1cb94f6ef5b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539146"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="f8419-102">Датарекордсет_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="f8419-102">DataRecordSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f8419-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f8419-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8419-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f8419-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f8419-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f8419-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f8419-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f8419-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f8419-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f8419-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f8419-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f8419-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8419-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f8419-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f8419-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8419-110">Elements and attributes</span></span>

<span data-ttu-id="f8419-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f8419-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f8419-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f8419-112">Child elements</span></span>

|<span data-ttu-id="f8419-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f8419-113">**Element**</span></span>|<span data-ttu-id="f8419-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f8419-114">**Type**</span></span>|<span data-ttu-id="f8419-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8419-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f8419-116">Аутолинккомпарисон</span><span class="sxs-lookup"><span data-stu-id="f8419-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-117">Аутолинккомпарисон_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f8419-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="f8419-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-119">Датаколумнс_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f8419-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f8419-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-121">Примарикэй_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f8419-122">Рефрешконфликт</span><span class="sxs-lookup"><span data-stu-id="f8419-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-123">Рефрешконфликт_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f8419-124">Rel</span><span class="sxs-lookup"><span data-stu-id="f8419-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-125">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f8419-126">Ровмап</span><span class="sxs-lookup"><span data-stu-id="f8419-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8419-127">Ровмап_типе</span><span class="sxs-lookup"><span data-stu-id="f8419-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f8419-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8419-128">Attributes</span></span>

|<span data-ttu-id="f8419-129">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f8419-129">**Attribute**</span></span>|<span data-ttu-id="f8419-130">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f8419-130">**Type**</span></span>|<span data-ttu-id="f8419-131">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f8419-131">**Required**</span></span>|<span data-ttu-id="f8419-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8419-132">**Description**</span></span>|<span data-ttu-id="f8419-133">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f8419-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8419-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="f8419-134">Checksum</span></span>  <br/> |<span data-ttu-id="f8419-135">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-136">optional</span></span>  <br/> ||<span data-ttu-id="f8419-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-138">Command</span><span class="sxs-lookup"><span data-stu-id="f8419-138">Command</span></span>  <br/> |<span data-ttu-id="f8419-139">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f8419-139">xsd:string</span></span>  <br/> |<span data-ttu-id="f8419-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-140">optional</span></span>  <br/> ||<span data-ttu-id="f8419-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f8419-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f8419-142">Коннектионид</span><span class="sxs-lookup"><span data-stu-id="f8419-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="f8419-143">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-144">optional</span></span>  <br/> ||<span data-ttu-id="f8419-145">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-146">ID</span><span class="sxs-lookup"><span data-stu-id="f8419-146">ID</span></span>  <br/> |<span data-ttu-id="f8419-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-148">required</span></span>  <br/> ||<span data-ttu-id="f8419-149">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-150">Имя</span><span class="sxs-lookup"><span data-stu-id="f8419-150">Name</span></span>  <br/> |<span data-ttu-id="f8419-151">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f8419-151">xsd:string</span></span>  <br/> |<span data-ttu-id="f8419-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-152">optional</span></span>  <br/> ||<span data-ttu-id="f8419-153">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f8419-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f8419-154">Некстровид</span><span class="sxs-lookup"><span data-stu-id="f8419-154">NextRowID</span></span>  <br/> |<span data-ttu-id="f8419-155">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-156">optional</span></span>  <br/> ||<span data-ttu-id="f8419-157">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-158">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8419-158">Options</span></span>  <br/> |<span data-ttu-id="f8419-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-160">optional</span></span>  <br/> ||<span data-ttu-id="f8419-161">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="f8419-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="f8419-163">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-164">optional</span></span>  <br/> ||<span data-ttu-id="f8419-165">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-166">РефрешнореконЦилиатионуи</span><span class="sxs-lookup"><span data-stu-id="f8419-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="f8419-167">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f8419-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f8419-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-168">optional</span></span>  <br/> ||<span data-ttu-id="f8419-169">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f8419-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f8419-170">Рефрешовервритеалл</span><span class="sxs-lookup"><span data-stu-id="f8419-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="f8419-171">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f8419-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f8419-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-172">optional</span></span>  <br/> ||<span data-ttu-id="f8419-173">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f8419-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f8419-174">Реплацелинкс</span><span class="sxs-lookup"><span data-stu-id="f8419-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="f8419-175">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f8419-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8419-176">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-176">optional</span></span>  <br/> ||<span data-ttu-id="f8419-177">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f8419-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8419-178">Ровордер</span><span class="sxs-lookup"><span data-stu-id="f8419-178">RowOrder</span></span>  <br/> |<span data-ttu-id="f8419-179">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f8419-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f8419-180">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-180">optional</span></span>  <br/> ||<span data-ttu-id="f8419-181">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f8419-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f8419-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="f8419-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="f8419-183">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="f8419-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="f8419-184">необязательный</span><span class="sxs-lookup"><span data-stu-id="f8419-184">optional</span></span>  <br/> ||<span data-ttu-id="f8419-185">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="f8419-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

