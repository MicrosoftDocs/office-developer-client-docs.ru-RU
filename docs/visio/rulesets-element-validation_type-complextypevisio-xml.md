---
title: Наборы правил элемент (Validation_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Включает в себя элемент набора правил для каждого правила проверки, задайте в документе.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399643"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="e1100-103">Наборы правил элемент (Validation_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e1100-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e1100-104">Включает в себя элемент **набора правил** для каждого правила проверки, задайте в документе.</span><span class="sxs-lookup"><span data-stu-id="e1100-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e1100-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1100-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1100-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e1100-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e1100-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="e1100-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e1100-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e1100-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e1100-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e1100-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e1100-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e1100-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e1100-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e1100-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e1100-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="e1100-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1100-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e1100-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e1100-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1100-114">Elements and attributes</span></span>

<span data-ttu-id="e1100-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e1100-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e1100-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e1100-116">Parent elements</span></span>

|<span data-ttu-id="e1100-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e1100-117">**Element**</span></span>|<span data-ttu-id="e1100-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1100-118">**Type**</span></span>|<span data-ttu-id="e1100-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1100-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1100-120">Проверка</span><span class="sxs-lookup"><span data-stu-id="e1100-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="e1100-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="e1100-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1100-122">Сохранение информации о проверки схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="e1100-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e1100-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e1100-123">Child elements</span></span>

|<span data-ttu-id="e1100-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e1100-124">**Element**</span></span>|<span data-ttu-id="e1100-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1100-125">**Type**</span></span>|<span data-ttu-id="e1100-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1100-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1100-127">Набор правил</span><span class="sxs-lookup"><span data-stu-id="e1100-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e1100-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="e1100-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1100-129">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="e1100-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e1100-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1100-130">Attributes</span></span>

<span data-ttu-id="e1100-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="e1100-131">None.</span></span>
  

