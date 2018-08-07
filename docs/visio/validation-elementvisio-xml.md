---
title: Элемент проверки ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Сохранение информации о проверки схемы для документа.
ms.openlocfilehash: f4a7c0893baebb09dccd743c3006a5512dec533d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815121"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="b9645-103">Элемент проверки ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b9645-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="b9645-104">Сохранение информации о проверки схемы для документа.</span><span class="sxs-lookup"><span data-stu-id="b9645-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9645-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b9645-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9645-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b9645-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b9645-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="b9645-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b9645-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b9645-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b9645-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b9645-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b9645-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b9645-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b9645-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b9645-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b9645-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="b9645-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b9645-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b9645-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b9645-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b9645-114">Elements and attributes</span></span>

<span data-ttu-id="b9645-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="b9645-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b9645-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b9645-116">Parent elements</span></span>

<span data-ttu-id="b9645-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="b9645-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9645-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b9645-118">Child elements</span></span>

|<span data-ttu-id="b9645-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b9645-119">**Element**</span></span>|<span data-ttu-id="b9645-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b9645-120">**Type**</span></span>|<span data-ttu-id="b9645-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9645-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b9645-122">Проблемы</span><span class="sxs-lookup"><span data-stu-id="b9645-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9645-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b9645-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9645-124">Содержит все элементы **проблему** для документа.</span><span class="sxs-lookup"><span data-stu-id="b9645-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="b9645-125">Наборы правил</span><span class="sxs-lookup"><span data-stu-id="b9645-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9645-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="b9645-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9645-127">Включает в себя элемент **набора правил** для каждого правила проверки, задайте в документе.</span><span class="sxs-lookup"><span data-stu-id="b9645-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="b9645-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="b9645-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b9645-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="b9645-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b9645-130">Инкапсулирует свойства, которые связаны с проверки документа.</span><span class="sxs-lookup"><span data-stu-id="b9645-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b9645-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b9645-131">Attributes</span></span>

<span data-ttu-id="b9645-132">Нет.</span><span class="sxs-lookup"><span data-stu-id="b9645-132">None.</span></span>
  

