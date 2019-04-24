---
title: Рулесет_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307744"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="a3d20-102">Рулесет_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a3d20-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a3d20-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a3d20-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3d20-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a3d20-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a3d20-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a3d20-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a3d20-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a3d20-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a3d20-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a3d20-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a3d20-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a3d20-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3d20-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a3d20-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a3d20-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a3d20-110">Elements and attributes</span></span>

<span data-ttu-id="a3d20-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a3d20-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a3d20-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a3d20-112">Child elements</span></span>

|<span data-ttu-id="a3d20-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a3d20-113">**Element**</span></span>|<span data-ttu-id="a3d20-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a3d20-114">**Type**</span></span>|<span data-ttu-id="a3d20-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a3d20-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3d20-116">Rule</span><span class="sxs-lookup"><span data-stu-id="a3d20-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3d20-117">Руле_типе</span><span class="sxs-lookup"><span data-stu-id="a3d20-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a3d20-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="a3d20-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3d20-119">Рулесетфлагс_типе</span><span class="sxs-lookup"><span data-stu-id="a3d20-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a3d20-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a3d20-120">Attributes</span></span>

|<span data-ttu-id="a3d20-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a3d20-121">**Attribute**</span></span>|<span data-ttu-id="a3d20-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a3d20-122">**Type**</span></span>|<span data-ttu-id="a3d20-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a3d20-123">**Required**</span></span>|<span data-ttu-id="a3d20-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a3d20-124">**Description**</span></span>|<span data-ttu-id="a3d20-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a3d20-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3d20-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a3d20-126">Description</span></span>  <br/> |<span data-ttu-id="a3d20-127">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a3d20-127">xsd:string</span></span>  <br/> |<span data-ttu-id="a3d20-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="a3d20-128">optional</span></span>  <br/> ||<span data-ttu-id="a3d20-129">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a3d20-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3d20-130">Включена</span><span class="sxs-lookup"><span data-stu-id="a3d20-130">Enabled</span></span>  <br/> |<span data-ttu-id="a3d20-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d20-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a3d20-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="a3d20-132">optional</span></span>  <br/> ||<span data-ttu-id="a3d20-133">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a3d20-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a3d20-134">ИД</span><span class="sxs-lookup"><span data-stu-id="a3d20-134">ID</span></span>  <br/> |<span data-ttu-id="a3d20-135">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a3d20-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3d20-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a3d20-136">required</span></span>  <br/> ||<span data-ttu-id="a3d20-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a3d20-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3d20-138">Имя</span><span class="sxs-lookup"><span data-stu-id="a3d20-138">Name</span></span>  <br/> |<span data-ttu-id="a3d20-139">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a3d20-139">xsd:string</span></span>  <br/> |<span data-ttu-id="a3d20-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="a3d20-140">optional</span></span>  <br/> ||<span data-ttu-id="a3d20-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a3d20-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3d20-142">NameU</span><span class="sxs-lookup"><span data-stu-id="a3d20-142">NameU</span></span>  <br/> |<span data-ttu-id="a3d20-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a3d20-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a3d20-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a3d20-144">required</span></span>  <br/> ||<span data-ttu-id="a3d20-145">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a3d20-145">Values of the xsd:string type.</span></span>  <br/> |
   

