---
title: RuleSet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393623"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="75a6b-102">RuleSet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="75a6b-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="75a6b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="75a6b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75a6b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="75a6b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="75a6b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="75a6b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="75a6b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="75a6b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="75a6b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="75a6b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="75a6b-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="75a6b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75a6b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="75a6b-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75a6b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="75a6b-110">Elements and attributes</span></span>

<span data-ttu-id="75a6b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="75a6b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75a6b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="75a6b-112">Child elements</span></span>

|<span data-ttu-id="75a6b-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="75a6b-113">**Element**</span></span>|<span data-ttu-id="75a6b-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="75a6b-114">**Type**</span></span>|<span data-ttu-id="75a6b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75a6b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75a6b-116">Rule</span><span class="sxs-lookup"><span data-stu-id="75a6b-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75a6b-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="75a6b-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="75a6b-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="75a6b-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75a6b-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="75a6b-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="75a6b-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="75a6b-120">Attributes</span></span>

|<span data-ttu-id="75a6b-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="75a6b-121">**Attribute**</span></span>|<span data-ttu-id="75a6b-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="75a6b-122">**Type**</span></span>|<span data-ttu-id="75a6b-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="75a6b-123">**Required**</span></span>|<span data-ttu-id="75a6b-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75a6b-124">**Description**</span></span>|<span data-ttu-id="75a6b-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="75a6b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75a6b-126">Описание</span><span class="sxs-lookup"><span data-stu-id="75a6b-126">Description</span></span>  <br/> |<span data-ttu-id="75a6b-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="75a6b-127">xsd:string</span></span>  <br/> |<span data-ttu-id="75a6b-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="75a6b-128">optional</span></span>  <br/> ||<span data-ttu-id="75a6b-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75a6b-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75a6b-130">Включена</span><span class="sxs-lookup"><span data-stu-id="75a6b-130">Enabled</span></span>  <br/> |<span data-ttu-id="75a6b-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="75a6b-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="75a6b-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="75a6b-132">optional</span></span>  <br/> ||<span data-ttu-id="75a6b-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="75a6b-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="75a6b-134">ID</span><span class="sxs-lookup"><span data-stu-id="75a6b-134">ID</span></span>  <br/> |<span data-ttu-id="75a6b-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="75a6b-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75a6b-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="75a6b-136">required</span></span>  <br/> ||<span data-ttu-id="75a6b-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="75a6b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75a6b-138">Имя</span><span class="sxs-lookup"><span data-stu-id="75a6b-138">Name</span></span>  <br/> |<span data-ttu-id="75a6b-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="75a6b-139">xsd:string</span></span>  <br/> |<span data-ttu-id="75a6b-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="75a6b-140">optional</span></span>  <br/> ||<span data-ttu-id="75a6b-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75a6b-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75a6b-142">NameU</span><span class="sxs-lookup"><span data-stu-id="75a6b-142">NameU</span></span>  <br/> |<span data-ttu-id="75a6b-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="75a6b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="75a6b-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="75a6b-144">required</span></span>  <br/> ||<span data-ttu-id="75a6b-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75a6b-145">Values of the xsd:string type.</span></span>  <br/> |
   

