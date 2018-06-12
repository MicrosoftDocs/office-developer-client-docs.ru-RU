---
title: Наборы правил элемент (Validation_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Включает в себя элемент набора правил для каждого правила проверки, задайте в документе.
ms.openlocfilehash: 84d64a8539f1b83c16a96a61ea68e9b2660c9036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814714"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="db23f-103">Наборы правил элемент (Validation_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="db23f-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="db23f-104">Включает в себя элемент **набора правил** для каждого правила проверки, задайте в документе.</span><span class="sxs-lookup"><span data-stu-id="db23f-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="db23f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="db23f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db23f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="db23f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="db23f-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="db23f-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="db23f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="db23f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="db23f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="db23f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="db23f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="db23f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="db23f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="db23f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="db23f-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="db23f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db23f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="db23f-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="db23f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="db23f-114">Elements and attributes</span></span>

<span data-ttu-id="db23f-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="db23f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="db23f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="db23f-116">Parent elements</span></span>

|<span data-ttu-id="db23f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="db23f-117">**Element**</span></span>|<span data-ttu-id="db23f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="db23f-118">**Type**</span></span>|<span data-ttu-id="db23f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db23f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db23f-120">Проверка</span><span class="sxs-lookup"><span data-stu-id="db23f-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="db23f-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="db23f-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="db23f-122">Сохранение информации о проверки схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="db23f-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="db23f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="db23f-123">Child elements</span></span>

|<span data-ttu-id="db23f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="db23f-124">**Element**</span></span>|<span data-ttu-id="db23f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="db23f-125">**Type**</span></span>|<span data-ttu-id="db23f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db23f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db23f-127">Набор правил</span><span class="sxs-lookup"><span data-stu-id="db23f-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="db23f-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="db23f-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="db23f-129">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="db23f-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="db23f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="db23f-130">Attributes</span></span>

<span data-ttu-id="db23f-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="db23f-131">None.</span></span>
  

