---
title: Элемент Рулефилтер (Rule_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541682"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a><span data-ttu-id="9feb0-103">Элемент Рулефилтер (Rule_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="9feb0-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9feb0-104">Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="9feb0-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9feb0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9feb0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9feb0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="9feb0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9feb0-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="9feb0-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9feb0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9feb0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9feb0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9feb0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9feb0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="9feb0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9feb0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="9feb0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9feb0-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="9feb0-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9feb0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="9feb0-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9feb0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9feb0-114">Elements and attributes</span></span>

<span data-ttu-id="9feb0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9feb0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9feb0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9feb0-116">Parent elements</span></span>

|<span data-ttu-id="9feb0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9feb0-117">**Element**</span></span>|<span data-ttu-id="9feb0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9feb0-118">**Type**</span></span>|<span data-ttu-id="9feb0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9feb0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9feb0-120">Rule</span><span class="sxs-lookup"><span data-stu-id="9feb0-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9feb0-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9feb0-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9feb0-122">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="9feb0-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9feb0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9feb0-123">Child elements</span></span>

<span data-ttu-id="9feb0-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="9feb0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9feb0-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9feb0-125">Attributes</span></span>

|<span data-ttu-id="9feb0-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9feb0-126">**Attribute**</span></span>|<span data-ttu-id="9feb0-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9feb0-127">**Type**</span></span>|<span data-ttu-id="9feb0-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9feb0-128">**Required**</span></span>|<span data-ttu-id="9feb0-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9feb0-129">**Description**</span></span>|<span data-ttu-id="9feb0-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9feb0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9feb0-131">Формула</span><span class="sxs-lookup"><span data-stu-id="9feb0-131">Formula</span></span>  <br/> |<span data-ttu-id="9feb0-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9feb0-132">xsd:string</span></span>  <br/> |<span data-ttu-id="9feb0-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="9feb0-133">optional</span></span>  <br/> |<span data-ttu-id="9feb0-134">Представляет формулу элемента.</span><span class="sxs-lookup"><span data-stu-id="9feb0-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="9feb0-135">Значения объекта XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9feb0-135">Values of the xsd:string.</span></span>  <br/> |
   

