---
title: Элемент RuleTest (Rule_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Задает логическое выражение, которое определяет, удовлетворяет ли целевой объект правила проверки.
ms.openlocfilehash: 8fd37040bec383ab61edfa62a09bb766ed8cd3c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384852"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="835e0-103">Элемент RuleTest (Rule_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="835e0-103">RuleTest element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="835e0-104">Задает логическое выражение, которое определяет, удовлетворяет ли целевой объект правила проверки.</span><span class="sxs-lookup"><span data-stu-id="835e0-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="835e0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="835e0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="835e0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="835e0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="835e0-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="835e0-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="835e0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="835e0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="835e0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="835e0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="835e0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="835e0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="835e0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="835e0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="835e0-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="835e0-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="835e0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="835e0-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="835e0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="835e0-114">Elements and attributes</span></span>

<span data-ttu-id="835e0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="835e0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="835e0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="835e0-116">Parent elements</span></span>

|<span data-ttu-id="835e0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="835e0-117">**Element**</span></span>|<span data-ttu-id="835e0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="835e0-118">**Type**</span></span>|<span data-ttu-id="835e0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="835e0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="835e0-120">Rule</span><span class="sxs-lookup"><span data-stu-id="835e0-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="835e0-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="835e0-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="835e0-122">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="835e0-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="835e0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="835e0-123">Child elements</span></span>

<span data-ttu-id="835e0-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="835e0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="835e0-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="835e0-125">Attributes</span></span>

|<span data-ttu-id="835e0-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="835e0-126">**Attribute**</span></span>|<span data-ttu-id="835e0-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="835e0-127">**Type**</span></span>|<span data-ttu-id="835e0-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="835e0-128">**Required**</span></span>|<span data-ttu-id="835e0-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="835e0-129">**Description**</span></span>|<span data-ttu-id="835e0-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="835e0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="835e0-131">Формула</span><span class="sxs-lookup"><span data-stu-id="835e0-131">Formula</span></span>  <br/> |<span data-ttu-id="835e0-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="835e0-132">xsd:string</span></span>  <br/> |<span data-ttu-id="835e0-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="835e0-133">optional</span></span>  <br/> |<span data-ttu-id="835e0-134">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="835e0-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="835e0-135">Значения xsd:string.</span><span class="sxs-lookup"><span data-stu-id="835e0-135">Values of the xsd:string.</span></span>  <br/> |
   

