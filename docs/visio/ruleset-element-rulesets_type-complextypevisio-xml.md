---
title: Элемент RuleSet (Рулесетс_типе complexType) (XML для Visio)
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
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="f1b57-103">Элемент RuleSet (Рулесетс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="f1b57-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f1b57-104">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="f1b57-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1b57-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f1b57-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1b57-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f1b57-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f1b57-107">Рулесет_типе</span><span class="sxs-lookup"><span data-stu-id="f1b57-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f1b57-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f1b57-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f1b57-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f1b57-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f1b57-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f1b57-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f1b57-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f1b57-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f1b57-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="f1b57-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1b57-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f1b57-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1b57-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1b57-114">Elements and attributes</span></span>

<span data-ttu-id="f1b57-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f1b57-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f1b57-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f1b57-116">Parent elements</span></span>

|<span data-ttu-id="f1b57-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f1b57-117">**Element**</span></span>|<span data-ttu-id="f1b57-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1b57-118">**Type**</span></span>|<span data-ttu-id="f1b57-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1b57-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1b57-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="f1b57-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1b57-121">Рулесетс_типе</span><span class="sxs-lookup"><span data-stu-id="f1b57-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1b57-122">Включает элемент **RuleSet** для каждого набора правил проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="f1b57-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1b57-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f1b57-123">Child elements</span></span>

|<span data-ttu-id="f1b57-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f1b57-124">**Element**</span></span>|<span data-ttu-id="f1b57-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1b57-125">**Type**</span></span>|<span data-ttu-id="f1b57-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1b57-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1b57-127">Rule</span><span class="sxs-lookup"><span data-stu-id="f1b57-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1b57-128">Руле_типе</span><span class="sxs-lookup"><span data-stu-id="f1b57-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1b57-129">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="f1b57-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="f1b57-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="f1b57-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1b57-131">Рулесетфлагс_типе</span><span class="sxs-lookup"><span data-stu-id="f1b57-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1b57-132">Задает свойства набора правил.</span><span class="sxs-lookup"><span data-stu-id="f1b57-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f1b57-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1b57-133">Attributes</span></span>

|<span data-ttu-id="f1b57-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f1b57-134">**Attribute**</span></span>|<span data-ttu-id="f1b57-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1b57-135">**Type**</span></span>|<span data-ttu-id="f1b57-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f1b57-136">**Required**</span></span>|<span data-ttu-id="f1b57-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1b57-137">**Description**</span></span>|<span data-ttu-id="f1b57-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f1b57-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1b57-139">Описание</span><span class="sxs-lookup"><span data-stu-id="f1b57-139">Description</span></span>  <br/> |<span data-ttu-id="f1b57-140">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f1b57-140">xsd:string</span></span>  <br/> |<span data-ttu-id="f1b57-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="f1b57-141">optional</span></span>  <br/> |<span data-ttu-id="f1b57-142">Задает описание, которое отображается в пользовательском интерфейсе для набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="f1b57-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="f1b57-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f1b57-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="f1b57-144">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f1b57-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f1b57-145">Включен</span><span class="sxs-lookup"><span data-stu-id="f1b57-145">Enabled</span></span>  <br/> |<span data-ttu-id="f1b57-146">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="f1b57-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f1b57-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="f1b57-147">optional</span></span>  <br/> |<span data-ttu-id="f1b57-148">Указывает, проверяются ли правила в указанном наборе правил проверки при запуске проверки для текущего документа.</span><span class="sxs-lookup"><span data-stu-id="f1b57-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="f1b57-149">Значение по умолчанию — True.</span><span class="sxs-lookup"><span data-stu-id="f1b57-149">Default is True.</span></span>  <br/> |<span data-ttu-id="f1b57-150">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f1b57-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f1b57-151">ID</span><span class="sxs-lookup"><span data-stu-id="f1b57-151">ID</span></span>  <br/> |<span data-ttu-id="f1b57-152">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f1b57-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f1b57-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1b57-153">required</span></span>  <br/> |<span data-ttu-id="f1b57-154">Задает уникальный идентификатор набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="f1b57-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f1b57-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f1b57-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f1b57-156">Имя</span><span class="sxs-lookup"><span data-stu-id="f1b57-156">Name</span></span>  <br/> |<span data-ttu-id="f1b57-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f1b57-157">xsd:string</span></span>  <br/> |<span data-ttu-id="f1b57-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="f1b57-158">optional</span></span>  <br/> |<span data-ttu-id="f1b57-159">Задает локальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="f1b57-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="f1b57-160">По умолчанию используется значение атрибута Намеу.</span><span class="sxs-lookup"><span data-stu-id="f1b57-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="f1b57-161">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f1b57-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f1b57-162">NameU</span><span class="sxs-lookup"><span data-stu-id="f1b57-162">NameU</span></span>  <br/> |<span data-ttu-id="f1b57-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="f1b57-163">xsd:string</span></span>  <br/> |<span data-ttu-id="f1b57-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1b57-164">required</span></span>  <br/> |<span data-ttu-id="f1b57-165">Задает универсальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="f1b57-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f1b57-166">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="f1b57-166">Values of the xsd:string type.</span></span>  <br/> |
   

