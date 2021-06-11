---
title: Rule_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541717"
---
# <a name="rule_type-complextype-visio-xml"></a><span data-ttu-id="fb3d9-102">Rule_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fb3d9-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fb3d9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="fb3d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb3d9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fb3d9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fb3d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fb3d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fb3d9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fb3d9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fb3d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb3d9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="fb3d9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fb3d9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb3d9-110">Elements and attributes</span></span>

<span data-ttu-id="fb3d9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fb3d9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fb3d9-112">Child elements</span></span>

|<span data-ttu-id="fb3d9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-113">**Element**</span></span>|<span data-ttu-id="fb3d9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-114">**Type**</span></span>|<span data-ttu-id="fb3d9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb3d9-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="fb3d9-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb3d9-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="fb3d9-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="fb3d9-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="fb3d9-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb3d9-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="fb3d9-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fb3d9-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fb3d9-120">Attributes</span></span>

|<span data-ttu-id="fb3d9-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-121">**Attribute**</span></span>|<span data-ttu-id="fb3d9-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-122">**Type**</span></span>|<span data-ttu-id="fb3d9-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-123">**Required**</span></span>|<span data-ttu-id="fb3d9-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-124">**Description**</span></span>|<span data-ttu-id="fb3d9-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fb3d9-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb3d9-126">Category</span><span class="sxs-lookup"><span data-stu-id="fb3d9-126">Category</span></span>  <br/> |<span data-ttu-id="fb3d9-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fb3d9-127">xsd:string</span></span>  <br/> |<span data-ttu-id="fb3d9-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-128">optional</span></span>  <br/> ||<span data-ttu-id="fb3d9-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fb3d9-130">Описание</span><span class="sxs-lookup"><span data-stu-id="fb3d9-130">Description</span></span>  <br/> |<span data-ttu-id="fb3d9-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fb3d9-131">xsd:string</span></span>  <br/> |<span data-ttu-id="fb3d9-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-132">optional</span></span>  <br/> ||<span data-ttu-id="fb3d9-133">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fb3d9-134">ID</span><span class="sxs-lookup"><span data-stu-id="fb3d9-134">ID</span></span>  <br/> |<span data-ttu-id="fb3d9-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fb3d9-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fb3d9-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-136">required</span></span>  <br/> ||<span data-ttu-id="fb3d9-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fb3d9-138">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="fb3d9-138">Ignored</span></span>  <br/> |<span data-ttu-id="fb3d9-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fb3d9-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fb3d9-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-140">optional</span></span>  <br/> ||<span data-ttu-id="fb3d9-141">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fb3d9-142">NameU</span><span class="sxs-lookup"><span data-stu-id="fb3d9-142">NameU</span></span>  <br/> |<span data-ttu-id="fb3d9-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fb3d9-143">xsd:string</span></span>  <br/> |<span data-ttu-id="fb3d9-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-144">required</span></span>  <br/> ||<span data-ttu-id="fb3d9-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fb3d9-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="fb3d9-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="fb3d9-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="fb3d9-147">xsd:int</span></span>  <br/> |<span data-ttu-id="fb3d9-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="fb3d9-148">optional</span></span>  <br/> ||<span data-ttu-id="fb3d9-149">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="fb3d9-149">Values of the xsd:int type.</span></span>  <br/> |
   

