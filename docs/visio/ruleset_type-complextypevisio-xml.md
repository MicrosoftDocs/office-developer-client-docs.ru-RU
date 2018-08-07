---
title: RuleSet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814712"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="f48ee-102">RuleSet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f48ee-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f48ee-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f48ee-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f48ee-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f48ee-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f48ee-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f48ee-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f48ee-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f48ee-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f48ee-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="f48ee-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f48ee-108">Нет</span><span class="sxs-lookup"><span data-stu-id="f48ee-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f48ee-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f48ee-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f48ee-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f48ee-110">Elements and attributes</span></span>

<span data-ttu-id="f48ee-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f48ee-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f48ee-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f48ee-112">Child elements</span></span>

|<span data-ttu-id="f48ee-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f48ee-113">**Element**</span></span>|<span data-ttu-id="f48ee-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f48ee-114">**Type**</span></span>|<span data-ttu-id="f48ee-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f48ee-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f48ee-116">Rule</span><span class="sxs-lookup"><span data-stu-id="f48ee-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f48ee-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="f48ee-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f48ee-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="f48ee-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f48ee-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="f48ee-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f48ee-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f48ee-120">Attributes</span></span>

|<span data-ttu-id="f48ee-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f48ee-121">**Attribute**</span></span>|<span data-ttu-id="f48ee-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f48ee-122">**Type**</span></span>|<span data-ttu-id="f48ee-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="f48ee-123">**Required**</span></span>|<span data-ttu-id="f48ee-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f48ee-124">**Description**</span></span>|<span data-ttu-id="f48ee-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f48ee-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f48ee-126">Описание</span><span class="sxs-lookup"><span data-stu-id="f48ee-126">Description</span></span>  <br/> |<span data-ttu-id="f48ee-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f48ee-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f48ee-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="f48ee-128">optional</span></span>  <br/> ||<span data-ttu-id="f48ee-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f48ee-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f48ee-130">Включена</span><span class="sxs-lookup"><span data-stu-id="f48ee-130">Enabled</span></span>  <br/> |<span data-ttu-id="f48ee-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f48ee-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f48ee-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="f48ee-132">optional</span></span>  <br/> ||<span data-ttu-id="f48ee-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f48ee-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f48ee-134">ID</span><span class="sxs-lookup"><span data-stu-id="f48ee-134">ID</span></span>  <br/> |<span data-ttu-id="f48ee-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f48ee-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f48ee-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f48ee-136">required</span></span>  <br/> ||<span data-ttu-id="f48ee-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f48ee-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f48ee-138">Имя</span><span class="sxs-lookup"><span data-stu-id="f48ee-138">Name</span></span>  <br/> |<span data-ttu-id="f48ee-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f48ee-139">xsd:string</span></span>  <br/> |<span data-ttu-id="f48ee-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="f48ee-140">optional</span></span>  <br/> ||<span data-ttu-id="f48ee-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f48ee-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f48ee-142">NameU</span><span class="sxs-lookup"><span data-stu-id="f48ee-142">NameU</span></span>  <br/> |<span data-ttu-id="f48ee-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f48ee-143">xsd:string</span></span>  <br/> |<span data-ttu-id="f48ee-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f48ee-144">required</span></span>  <br/> ||<span data-ttu-id="f48ee-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f48ee-145">Values of the xsd:string type.</span></span>  <br/> |
   

