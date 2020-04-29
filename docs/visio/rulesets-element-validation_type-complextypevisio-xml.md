---
title: Элемент RuleSets (Validation_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Включает элемент RuleSet для каждого набора правил проверки в документе.
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541577"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="ce93d-103">Элемент RuleSets (Validation_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="ce93d-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ce93d-104">Включает элемент **RuleSet** для каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="ce93d-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ce93d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ce93d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce93d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ce93d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ce93d-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="ce93d-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ce93d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ce93d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ce93d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ce93d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ce93d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ce93d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ce93d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ce93d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ce93d-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="ce93d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce93d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ce93d-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ce93d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ce93d-114">Elements and attributes</span></span>

<span data-ttu-id="ce93d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ce93d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ce93d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ce93d-116">Parent elements</span></span>

|<span data-ttu-id="ce93d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ce93d-117">**Element**</span></span>|<span data-ttu-id="ce93d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ce93d-118">**Type**</span></span>|<span data-ttu-id="ce93d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce93d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce93d-120">Validation</span><span class="sxs-lookup"><span data-stu-id="ce93d-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="ce93d-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="ce93d-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce93d-122">Сохраняет сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="ce93d-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ce93d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ce93d-123">Child elements</span></span>

|<span data-ttu-id="ce93d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ce93d-124">**Element**</span></span>|<span data-ttu-id="ce93d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ce93d-125">**Type**</span></span>|<span data-ttu-id="ce93d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce93d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce93d-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="ce93d-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ce93d-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="ce93d-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ce93d-129">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="ce93d-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ce93d-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ce93d-130">Attributes</span></span>

<span data-ttu-id="ce93d-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="ce93d-131">None.</span></span>
  

