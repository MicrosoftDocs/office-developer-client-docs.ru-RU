---
title: Rule_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393511"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="daf50-102">Rule_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="daf50-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="daf50-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="daf50-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daf50-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="daf50-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="daf50-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="daf50-105">**Schema file**</span></span> <br/> |<span data-ttu-id="daf50-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="daf50-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="daf50-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="daf50-107">**Extension base**</span></span> <br/> |<span data-ttu-id="daf50-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="daf50-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="daf50-109">Определение</span><span class="sxs-lookup"><span data-stu-id="daf50-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="daf50-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="daf50-110">Elements and attributes</span></span>

<span data-ttu-id="daf50-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="daf50-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="daf50-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="daf50-112">Child elements</span></span>

|<span data-ttu-id="daf50-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="daf50-113">**Element**</span></span>|<span data-ttu-id="daf50-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="daf50-114">**Type**</span></span>|<span data-ttu-id="daf50-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="daf50-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="daf50-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="daf50-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="daf50-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="daf50-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="daf50-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="daf50-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="daf50-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="daf50-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="daf50-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="daf50-120">Attributes</span></span>

|<span data-ttu-id="daf50-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="daf50-121">**Attribute**</span></span>|<span data-ttu-id="daf50-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="daf50-122">**Type**</span></span>|<span data-ttu-id="daf50-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="daf50-123">**Required**</span></span>|<span data-ttu-id="daf50-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="daf50-124">**Description**</span></span>|<span data-ttu-id="daf50-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="daf50-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="daf50-126">Категория</span><span class="sxs-lookup"><span data-stu-id="daf50-126">Category</span></span>  <br/> |<span data-ttu-id="daf50-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="daf50-127">xsd:string</span></span>  <br/> |<span data-ttu-id="daf50-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-128">optional</span></span>  <br/> ||<span data-ttu-id="daf50-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="daf50-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="daf50-130">Описание</span><span class="sxs-lookup"><span data-stu-id="daf50-130">Description</span></span>  <br/> |<span data-ttu-id="daf50-131">XSD:String</span><span class="sxs-lookup"><span data-stu-id="daf50-131">xsd:string</span></span>  <br/> |<span data-ttu-id="daf50-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-132">optional</span></span>  <br/> ||<span data-ttu-id="daf50-133">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="daf50-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="daf50-134">ID</span><span class="sxs-lookup"><span data-stu-id="daf50-134">ID</span></span>  <br/> |<span data-ttu-id="daf50-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="daf50-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="daf50-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-136">required</span></span>  <br/> ||<span data-ttu-id="daf50-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="daf50-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="daf50-138">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="daf50-138">Ignored</span></span>  <br/> |<span data-ttu-id="daf50-139">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="daf50-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="daf50-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-140">optional</span></span>  <br/> ||<span data-ttu-id="daf50-141">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="daf50-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="daf50-142">NameU</span><span class="sxs-lookup"><span data-stu-id="daf50-142">NameU</span></span>  <br/> |<span data-ttu-id="daf50-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="daf50-143">xsd:string</span></span>  <br/> |<span data-ttu-id="daf50-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-144">required</span></span>  <br/> ||<span data-ttu-id="daf50-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="daf50-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="daf50-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="daf50-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="daf50-147">XSD: int</span><span class="sxs-lookup"><span data-stu-id="daf50-147">xsd:int</span></span>  <br/> |<span data-ttu-id="daf50-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="daf50-148">optional</span></span>  <br/> ||<span data-ttu-id="daf50-149">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="daf50-149">Values of the xsd:int type.</span></span>  <br/> |
   

