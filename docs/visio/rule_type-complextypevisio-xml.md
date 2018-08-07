---
title: Rule_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814699"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="f5786-102">Rule_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f5786-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f5786-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f5786-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5786-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f5786-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f5786-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f5786-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f5786-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f5786-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f5786-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="f5786-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f5786-108">Нет</span><span class="sxs-lookup"><span data-stu-id="f5786-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5786-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f5786-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f5786-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5786-110">Elements and attributes</span></span>

<span data-ttu-id="f5786-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f5786-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f5786-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f5786-112">Child elements</span></span>

|<span data-ttu-id="f5786-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f5786-113">**Element**</span></span>|<span data-ttu-id="f5786-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f5786-114">**Type**</span></span>|<span data-ttu-id="f5786-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5786-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5786-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="f5786-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5786-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="f5786-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f5786-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="f5786-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5786-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="f5786-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f5786-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5786-120">Attributes</span></span>

|<span data-ttu-id="f5786-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f5786-121">**Attribute**</span></span>|<span data-ttu-id="f5786-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f5786-122">**Type**</span></span>|<span data-ttu-id="f5786-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="f5786-123">**Required**</span></span>|<span data-ttu-id="f5786-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5786-124">**Description**</span></span>|<span data-ttu-id="f5786-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f5786-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f5786-126">Категория</span><span class="sxs-lookup"><span data-stu-id="f5786-126">Category</span></span>  <br/> |<span data-ttu-id="f5786-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f5786-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f5786-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-128">optional</span></span>  <br/> ||<span data-ttu-id="f5786-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5786-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5786-130">Описание</span><span class="sxs-lookup"><span data-stu-id="f5786-130">Description</span></span>  <br/> |<span data-ttu-id="f5786-131">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f5786-131">xsd:string</span></span>  <br/> |<span data-ttu-id="f5786-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-132">optional</span></span>  <br/> ||<span data-ttu-id="f5786-133">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5786-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5786-134">ID</span><span class="sxs-lookup"><span data-stu-id="f5786-134">ID</span></span>  <br/> |<span data-ttu-id="f5786-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f5786-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f5786-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-136">required</span></span>  <br/> ||<span data-ttu-id="f5786-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f5786-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f5786-138">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="f5786-138">Ignored</span></span>  <br/> |<span data-ttu-id="f5786-139">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f5786-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f5786-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-140">optional</span></span>  <br/> ||<span data-ttu-id="f5786-141">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f5786-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f5786-142">NameU</span><span class="sxs-lookup"><span data-stu-id="f5786-142">NameU</span></span>  <br/> |<span data-ttu-id="f5786-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f5786-143">xsd:string</span></span>  <br/> |<span data-ttu-id="f5786-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-144">required</span></span>  <br/> ||<span data-ttu-id="f5786-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f5786-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f5786-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="f5786-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="f5786-147">XSD: int</span><span class="sxs-lookup"><span data-stu-id="f5786-147">xsd:int</span></span>  <br/> |<span data-ttu-id="f5786-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5786-148">optional</span></span>  <br/> ||<span data-ttu-id="f5786-149">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="f5786-149">Values of the xsd:int type.</span></span>  <br/> |
   

