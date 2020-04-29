---
title: Элемент RuleSet (RuleSets_Type complexType) (XML для Visio)
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
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="2b836-103">Элемент RuleSet (RuleSets_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="2b836-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2b836-104">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="2b836-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b836-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2b836-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b836-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="2b836-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2b836-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="2b836-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2b836-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2b836-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2b836-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2b836-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2b836-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2b836-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2b836-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="2b836-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2b836-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="2b836-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b836-113">Определение</span><span class="sxs-lookup"><span data-stu-id="2b836-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2b836-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b836-114">Elements and attributes</span></span>

<span data-ttu-id="2b836-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2b836-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2b836-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2b836-116">Parent elements</span></span>

|<span data-ttu-id="2b836-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2b836-117">**Element**</span></span>|<span data-ttu-id="2b836-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b836-118">**Type**</span></span>|<span data-ttu-id="2b836-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b836-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b836-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="2b836-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b836-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="2b836-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b836-122">Включает элемент **RuleSet** для каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="2b836-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2b836-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2b836-123">Child elements</span></span>

|<span data-ttu-id="2b836-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2b836-124">**Element**</span></span>|<span data-ttu-id="2b836-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b836-125">**Type**</span></span>|<span data-ttu-id="2b836-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b836-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b836-127">Rule</span><span class="sxs-lookup"><span data-stu-id="2b836-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b836-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="2b836-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b836-129">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="2b836-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="2b836-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="2b836-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b836-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="2b836-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b836-132">Задает свойства набора правил.</span><span class="sxs-lookup"><span data-stu-id="2b836-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2b836-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b836-133">Attributes</span></span>

|<span data-ttu-id="2b836-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="2b836-134">**Attribute**</span></span>|<span data-ttu-id="2b836-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b836-135">**Type**</span></span>|<span data-ttu-id="2b836-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="2b836-136">**Required**</span></span>|<span data-ttu-id="2b836-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b836-137">**Description**</span></span>|<span data-ttu-id="2b836-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="2b836-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b836-139">Описание</span><span class="sxs-lookup"><span data-stu-id="2b836-139">Description</span></span>  <br/> |<span data-ttu-id="2b836-140">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2b836-140">xsd:string</span></span>  <br/> |<span data-ttu-id="2b836-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="2b836-141">optional</span></span>  <br/> |<span data-ttu-id="2b836-142">Задает описание, которое отображается в пользовательском интерфейсе для набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="2b836-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="2b836-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="2b836-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="2b836-144">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2b836-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b836-145">Включен</span><span class="sxs-lookup"><span data-stu-id="2b836-145">Enabled</span></span>  <br/> |<span data-ttu-id="2b836-146">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="2b836-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2b836-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="2b836-147">optional</span></span>  <br/> |<span data-ttu-id="2b836-148">Указывает, проверяются ли правила в указанном наборе правил проверки при запуске проверки для текущего документа.</span><span class="sxs-lookup"><span data-stu-id="2b836-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="2b836-149">Значение по умолчанию — True.</span><span class="sxs-lookup"><span data-stu-id="2b836-149">Default is True.</span></span>  <br/> |<span data-ttu-id="2b836-150">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="2b836-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2b836-151">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="2b836-151">ID</span></span>  <br/> |<span data-ttu-id="2b836-152">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="2b836-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2b836-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2b836-153">required</span></span>  <br/> |<span data-ttu-id="2b836-154">Задает уникальный идентификатор набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="2b836-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="2b836-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="2b836-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2b836-156">Имя</span><span class="sxs-lookup"><span data-stu-id="2b836-156">Name</span></span>  <br/> |<span data-ttu-id="2b836-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2b836-157">xsd:string</span></span>  <br/> |<span data-ttu-id="2b836-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="2b836-158">optional</span></span>  <br/> |<span data-ttu-id="2b836-159">Задает локальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="2b836-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="2b836-160">По умолчанию используется значение атрибута Намеу.</span><span class="sxs-lookup"><span data-stu-id="2b836-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="2b836-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2b836-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2b836-162">NameU</span><span class="sxs-lookup"><span data-stu-id="2b836-162">NameU</span></span>  <br/> |<span data-ttu-id="2b836-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="2b836-163">xsd:string</span></span>  <br/> |<span data-ttu-id="2b836-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2b836-164">required</span></span>  <br/> |<span data-ttu-id="2b836-165">Задает универсальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="2b836-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="2b836-166">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="2b836-166">Values of the xsd:string type.</span></span>  <br/> |
   

