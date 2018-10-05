---
title: Элемент RuleFilter (Rule_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396731"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="117e7-103">Элемент RuleFilter (Rule_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="117e7-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="117e7-104">Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="117e7-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="117e7-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="117e7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="117e7-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="117e7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="117e7-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="117e7-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="117e7-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="117e7-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="117e7-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="117e7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="117e7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="117e7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="117e7-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="117e7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="117e7-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="117e7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="117e7-113">Определение</span><span class="sxs-lookup"><span data-stu-id="117e7-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="117e7-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="117e7-114">Elements and attributes</span></span>

<span data-ttu-id="117e7-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="117e7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="117e7-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="117e7-116">Parent elements</span></span>

|<span data-ttu-id="117e7-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="117e7-117">**Element**</span></span>|<span data-ttu-id="117e7-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="117e7-118">**Type**</span></span>|<span data-ttu-id="117e7-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="117e7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="117e7-120">Rule</span><span class="sxs-lookup"><span data-stu-id="117e7-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="117e7-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="117e7-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="117e7-122">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="117e7-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="117e7-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="117e7-123">Child elements</span></span>

<span data-ttu-id="117e7-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="117e7-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="117e7-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="117e7-125">Attributes</span></span>

|<span data-ttu-id="117e7-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="117e7-126">**Attribute**</span></span>|<span data-ttu-id="117e7-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="117e7-127">**Type**</span></span>|<span data-ttu-id="117e7-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="117e7-128">**Required**</span></span>|<span data-ttu-id="117e7-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="117e7-129">**Description**</span></span>|<span data-ttu-id="117e7-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="117e7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="117e7-131">Формула</span><span class="sxs-lookup"><span data-stu-id="117e7-131">Formula</span></span>  <br/> |<span data-ttu-id="117e7-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="117e7-132">xsd:string</span></span>  <br/> |<span data-ttu-id="117e7-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="117e7-133">optional</span></span>  <br/> |<span data-ttu-id="117e7-134">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="117e7-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="117e7-135">Значения xsd:string.</span><span class="sxs-lookup"><span data-stu-id="117e7-135">Values of the xsd:string.</span></span>  <br/> |
   

