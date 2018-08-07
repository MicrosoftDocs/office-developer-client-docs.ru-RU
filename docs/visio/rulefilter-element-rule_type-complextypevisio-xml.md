---
title: Элемент RuleFilter (Rule_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814683"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="fbb69-103">Элемент RuleFilter (Rule_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="fbb69-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fbb69-104">Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="fbb69-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbb69-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fbb69-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbb69-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fbb69-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fbb69-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="fbb69-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fbb69-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fbb69-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fbb69-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fbb69-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fbb69-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fbb69-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fbb69-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fbb69-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fbb69-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="fbb69-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbb69-113">Определение</span><span class="sxs-lookup"><span data-stu-id="fbb69-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbb69-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fbb69-114">Elements and attributes</span></span>

<span data-ttu-id="fbb69-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="fbb69-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbb69-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fbb69-116">Parent elements</span></span>

|<span data-ttu-id="fbb69-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fbb69-117">**Element**</span></span>|<span data-ttu-id="fbb69-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fbb69-118">**Type**</span></span>|<span data-ttu-id="fbb69-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbb69-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbb69-120">Rule</span><span class="sxs-lookup"><span data-stu-id="fbb69-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fbb69-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="fbb69-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbb69-122">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="fbb69-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbb69-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fbb69-123">Child elements</span></span>

<span data-ttu-id="fbb69-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="fbb69-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbb69-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fbb69-125">Attributes</span></span>

|<span data-ttu-id="fbb69-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fbb69-126">**Attribute**</span></span>|<span data-ttu-id="fbb69-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fbb69-127">**Type**</span></span>|<span data-ttu-id="fbb69-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="fbb69-128">**Required**</span></span>|<span data-ttu-id="fbb69-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbb69-129">**Description**</span></span>|<span data-ttu-id="fbb69-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fbb69-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fbb69-131">Формула</span><span class="sxs-lookup"><span data-stu-id="fbb69-131">Formula</span></span>  <br/> |<span data-ttu-id="fbb69-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="fbb69-132">xsd:string</span></span>  <br/> |<span data-ttu-id="fbb69-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="fbb69-133">optional</span></span>  <br/> |<span data-ttu-id="fbb69-134">Представляет элемент формулы.</span><span class="sxs-lookup"><span data-stu-id="fbb69-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="fbb69-135">Значения xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fbb69-135">Values of the xsd:string.</span></span>  <br/> |
   

