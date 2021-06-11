---
title: Элемент RuleSets (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Включает элемент RuleSet для каждого правила проверки, за набором в документе.
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541577"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="8f288-103">Элемент RuleSets (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8f288-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8f288-104">Включает элемент **RuleSet** для каждого правила проверки, за набором в документе.</span><span class="sxs-lookup"><span data-stu-id="8f288-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8f288-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f288-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f288-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8f288-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8f288-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="8f288-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8f288-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8f288-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8f288-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8f288-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8f288-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8f288-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8f288-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="8f288-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8f288-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="8f288-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f288-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8f288-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8f288-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f288-114">Elements and attributes</span></span>

<span data-ttu-id="8f288-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8f288-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8f288-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8f288-116">Parent elements</span></span>

|<span data-ttu-id="8f288-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f288-117">**Element**</span></span>|<span data-ttu-id="8f288-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f288-118">**Type**</span></span>|<span data-ttu-id="8f288-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f288-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f288-120">Validation</span><span class="sxs-lookup"><span data-stu-id="8f288-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="8f288-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="8f288-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f288-122">Сохраняет сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="8f288-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f288-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8f288-123">Child elements</span></span>

|<span data-ttu-id="8f288-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f288-124">**Element**</span></span>|<span data-ttu-id="8f288-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f288-125">**Type**</span></span>|<span data-ttu-id="8f288-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f288-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f288-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="8f288-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f288-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="8f288-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f288-129">Представляет один набор правил проверки диаграммы.</span><span class="sxs-lookup"><span data-stu-id="8f288-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8f288-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f288-130">Attributes</span></span>

<span data-ttu-id="8f288-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="8f288-131">None.</span></span>
  

