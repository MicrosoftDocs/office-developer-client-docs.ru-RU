---
title: Элемент RuleSet (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Представляет один набор правил проверки схемы.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541640"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="4aea3-103">Элемент RuleSet (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4aea3-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4aea3-104">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="4aea3-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4aea3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4aea3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4aea3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4aea3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4aea3-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="4aea3-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4aea3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4aea3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4aea3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4aea3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4aea3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4aea3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4aea3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4aea3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4aea3-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="4aea3-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4aea3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4aea3-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4aea3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4aea3-114">Elements and attributes</span></span>

<span data-ttu-id="4aea3-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4aea3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4aea3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4aea3-116">Parent elements</span></span>

|<span data-ttu-id="4aea3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4aea3-117">**Element**</span></span>|<span data-ttu-id="4aea3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4aea3-118">**Type**</span></span>|<span data-ttu-id="4aea3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4aea3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4aea3-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="4aea3-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4aea3-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="4aea3-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4aea3-122">Включает элемент **RuleSet для** каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="4aea3-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4aea3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4aea3-123">Child elements</span></span>

|<span data-ttu-id="4aea3-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4aea3-124">**Element**</span></span>|<span data-ttu-id="4aea3-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4aea3-125">**Type**</span></span>|<span data-ttu-id="4aea3-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4aea3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4aea3-127">Rule</span><span class="sxs-lookup"><span data-stu-id="4aea3-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4aea3-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="4aea3-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4aea3-129">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="4aea3-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="4aea3-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="4aea3-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4aea3-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="4aea3-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4aea3-132">Указывает свойства набора правил.</span><span class="sxs-lookup"><span data-stu-id="4aea3-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4aea3-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4aea3-133">Attributes</span></span>

|<span data-ttu-id="4aea3-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4aea3-134">**Attribute**</span></span>|<span data-ttu-id="4aea3-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4aea3-135">**Type**</span></span>|<span data-ttu-id="4aea3-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4aea3-136">**Required**</span></span>|<span data-ttu-id="4aea3-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4aea3-137">**Description**</span></span>|<span data-ttu-id="4aea3-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4aea3-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4aea3-139">Описание</span><span class="sxs-lookup"><span data-stu-id="4aea3-139">Description</span></span>  <br/> |<span data-ttu-id="4aea3-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4aea3-140">xsd:string</span></span>  <br/> |<span data-ttu-id="4aea3-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="4aea3-141">optional</span></span>  <br/> |<span data-ttu-id="4aea3-142">Указывает описание, которое отображается в пользовательском интерфейсе для набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="4aea3-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="4aea3-143">По умолчанию это пустая строка.</span><span class="sxs-lookup"><span data-stu-id="4aea3-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="4aea3-144">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4aea3-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4aea3-145">Включено</span><span class="sxs-lookup"><span data-stu-id="4aea3-145">Enabled</span></span>  <br/> |<span data-ttu-id="4aea3-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4aea3-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4aea3-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="4aea3-147">optional</span></span>  <br/> |<span data-ttu-id="4aea3-148">Указывает, проверяются ли правила в указанном наборе правил проверки при запуске проверки для текущего документа.</span><span class="sxs-lookup"><span data-stu-id="4aea3-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="4aea3-149">Значение по умолчанию — True.</span><span class="sxs-lookup"><span data-stu-id="4aea3-149">Default is True.</span></span>  <br/> |<span data-ttu-id="4aea3-150">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4aea3-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4aea3-151">ID</span><span class="sxs-lookup"><span data-stu-id="4aea3-151">ID</span></span>  <br/> |<span data-ttu-id="4aea3-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4aea3-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4aea3-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4aea3-153">required</span></span>  <br/> |<span data-ttu-id="4aea3-154">Указывает уникальный идентификатор набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="4aea3-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="4aea3-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4aea3-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4aea3-156">Имя</span><span class="sxs-lookup"><span data-stu-id="4aea3-156">Name</span></span>  <br/> |<span data-ttu-id="4aea3-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4aea3-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4aea3-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="4aea3-158">optional</span></span>  <br/> |<span data-ttu-id="4aea3-159">Указывает локальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="4aea3-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="4aea3-160">Значение атрибута NameU по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4aea3-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="4aea3-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4aea3-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4aea3-162">NameU</span><span class="sxs-lookup"><span data-stu-id="4aea3-162">NameU</span></span>  <br/> |<span data-ttu-id="4aea3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4aea3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4aea3-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4aea3-164">required</span></span>  <br/> |<span data-ttu-id="4aea3-165">Указывает универсальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="4aea3-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="4aea3-166">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4aea3-166">Values of the xsd:string type.</span></span>  <br/> |
   

