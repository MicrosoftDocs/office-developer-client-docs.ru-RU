---
title: Элемент Validation (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Сохраняет сведения о проверке схемы для документа.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329086"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="75f20-103">Элемент Validation (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="75f20-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="75f20-104">Сохраняет сведения о проверке схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="75f20-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75f20-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="75f20-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75f20-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="75f20-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75f20-107">Валидатион_типе</span><span class="sxs-lookup"><span data-stu-id="75f20-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75f20-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="75f20-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75f20-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="75f20-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75f20-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="75f20-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75f20-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="75f20-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75f20-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="75f20-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75f20-113">Определение</span><span class="sxs-lookup"><span data-stu-id="75f20-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75f20-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="75f20-114">Elements and attributes</span></span>

<span data-ttu-id="75f20-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="75f20-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75f20-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="75f20-116">Parent elements</span></span>

<span data-ttu-id="75f20-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="75f20-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75f20-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="75f20-118">Child elements</span></span>

|<span data-ttu-id="75f20-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="75f20-119">**Element**</span></span>|<span data-ttu-id="75f20-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="75f20-120">**Type**</span></span>|<span data-ttu-id="75f20-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75f20-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75f20-122">Issues</span><span class="sxs-lookup"><span data-stu-id="75f20-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75f20-123">Иссуес_типе</span><span class="sxs-lookup"><span data-stu-id="75f20-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75f20-124">Содержит все элементы **issue** для документа.</span><span class="sxs-lookup"><span data-stu-id="75f20-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="75f20-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="75f20-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75f20-126">Рулесетс_типе</span><span class="sxs-lookup"><span data-stu-id="75f20-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75f20-127">Включает элемент **RuleSet** для каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="75f20-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="75f20-128">Валидатионпропертиес</span><span class="sxs-lookup"><span data-stu-id="75f20-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75f20-129">Валидатионпропертиес_типе</span><span class="sxs-lookup"><span data-stu-id="75f20-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75f20-130">Инкапсулирует свойства, связанные с проверкой документа.</span><span class="sxs-lookup"><span data-stu-id="75f20-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="75f20-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="75f20-131">Attributes</span></span>

<span data-ttu-id="75f20-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="75f20-132">None.</span></span>
  

