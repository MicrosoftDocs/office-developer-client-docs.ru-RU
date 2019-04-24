---
title: Элемент RuleSets (Валидатион_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Включает элемент RuleSet для каждого набора правил проверки в документе.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319049"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="b0b8a-103">Элемент RuleSets (Валидатион_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="b0b8a-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b0b8a-104">Включает элемент **RuleSet** для каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="b0b8a-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b0b8a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b0b8a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0b8a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b0b8a-107">Рулесетс_типе</span><span class="sxs-lookup"><span data-stu-id="b0b8a-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b0b8a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b0b8a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b0b8a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b0b8a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b0b8a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b0b8a-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="b0b8a-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b0b8a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b0b8a-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b0b8a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b0b8a-114">Elements and attributes</span></span>

<span data-ttu-id="b0b8a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b0b8a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b0b8a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b0b8a-116">Parent elements</span></span>

|<span data-ttu-id="b0b8a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-117">**Element**</span></span>|<span data-ttu-id="b0b8a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-118">**Type**</span></span>|<span data-ttu-id="b0b8a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b0b8a-120">Validation</span><span class="sxs-lookup"><span data-stu-id="b0b8a-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="b0b8a-121">Валидатион_типе</span><span class="sxs-lookup"><span data-stu-id="b0b8a-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b0b8a-122">Сохраняет сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="b0b8a-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0b8a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b0b8a-123">Child elements</span></span>

|<span data-ttu-id="b0b8a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-124">**Element**</span></span>|<span data-ttu-id="b0b8a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-125">**Type**</span></span>|<span data-ttu-id="b0b8a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0b8a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b0b8a-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="b0b8a-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b0b8a-128">Рулесет_типе</span><span class="sxs-lookup"><span data-stu-id="b0b8a-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b0b8a-129">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="b0b8a-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b0b8a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b0b8a-130">Attributes</span></span>

<span data-ttu-id="b0b8a-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="b0b8a-131">None.</span></span>
  

