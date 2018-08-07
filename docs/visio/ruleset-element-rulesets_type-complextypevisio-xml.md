---
title: Элемент набора правил (RuleSets_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Представляет один набор правил проверки схемы.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814708"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="dd1e4-103">Элемент набора правил (RuleSets_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="dd1e4-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dd1e4-104">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd1e4-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dd1e4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd1e4-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dd1e4-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="dd1e4-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dd1e4-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dd1e4-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dd1e4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dd1e4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dd1e4-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dd1e4-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="dd1e4-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dd1e4-113">Определение</span><span class="sxs-lookup"><span data-stu-id="dd1e4-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dd1e4-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="dd1e4-114">Elements and attributes</span></span>

<span data-ttu-id="dd1e4-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dd1e4-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dd1e4-116">Parent elements</span></span>

|<span data-ttu-id="dd1e4-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-117">**Element**</span></span>|<span data-ttu-id="dd1e4-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-118">**Type**</span></span>|<span data-ttu-id="dd1e4-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dd1e4-120">Наборы правил</span><span class="sxs-lookup"><span data-stu-id="dd1e4-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dd1e4-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="dd1e4-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dd1e4-122">Включает в себя элемент **набора правил** для каждого правила проверки, задайте в документе.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dd1e4-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dd1e4-123">Child elements</span></span>

|<span data-ttu-id="dd1e4-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-124">**Element**</span></span>|<span data-ttu-id="dd1e4-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-125">**Type**</span></span>|<span data-ttu-id="dd1e4-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dd1e4-127">Rule</span><span class="sxs-lookup"><span data-stu-id="dd1e4-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dd1e4-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="dd1e4-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dd1e4-129">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="dd1e4-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="dd1e4-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dd1e4-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="dd1e4-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dd1e4-132">Задает свойства набора правил.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dd1e4-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dd1e4-133">Attributes</span></span>

|<span data-ttu-id="dd1e4-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-134">**Attribute**</span></span>|<span data-ttu-id="dd1e4-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-135">**Type**</span></span>|<span data-ttu-id="dd1e4-136">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-136">**Required**</span></span>|<span data-ttu-id="dd1e4-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-137">**Description**</span></span>|<span data-ttu-id="dd1e4-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="dd1e4-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dd1e4-139">Описание</span><span class="sxs-lookup"><span data-stu-id="dd1e4-139">Description</span></span>  <br/> |<span data-ttu-id="dd1e4-140">XSD:String</span><span class="sxs-lookup"><span data-stu-id="dd1e4-140">xsd:string</span></span>  <br/> |<span data-ttu-id="dd1e4-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="dd1e4-141">optional</span></span>  <br/> |<span data-ttu-id="dd1e4-142">Указывает описание, которое отображается в пользовательском интерфейсе для набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="dd1e4-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="dd1e4-144">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dd1e4-145">Включена</span><span class="sxs-lookup"><span data-stu-id="dd1e4-145">Enabled</span></span>  <br/> |<span data-ttu-id="dd1e4-146">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="dd1e4-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dd1e4-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="dd1e4-147">optional</span></span>  <br/> |<span data-ttu-id="dd1e4-148">Указывает, проверяются ли правила в наборе правил указанного проверки при проверке запускается для текущего документа.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="dd1e4-149">Значение по умолчанию — True.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-149">Default is True.</span></span>  <br/> |<span data-ttu-id="dd1e4-150">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dd1e4-151">ID</span><span class="sxs-lookup"><span data-stu-id="dd1e4-151">ID</span></span>  <br/> |<span data-ttu-id="dd1e4-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dd1e4-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dd1e4-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dd1e4-153">required</span></span>  <br/> |<span data-ttu-id="dd1e4-154">Задает уникальный идентификатор набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="dd1e4-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dd1e4-156">Имя</span><span class="sxs-lookup"><span data-stu-id="dd1e4-156">Name</span></span>  <br/> |<span data-ttu-id="dd1e4-157">XSD:String</span><span class="sxs-lookup"><span data-stu-id="dd1e4-157">xsd:string</span></span>  <br/> |<span data-ttu-id="dd1e4-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="dd1e4-158">optional</span></span>  <br/> |<span data-ttu-id="dd1e4-159">Указывает локальное имя набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="dd1e4-160">По умолчанию используется значение атрибута NameU.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="dd1e4-161">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dd1e4-162">NameU</span><span class="sxs-lookup"><span data-stu-id="dd1e4-162">NameU</span></span>  <br/> |<span data-ttu-id="dd1e4-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="dd1e4-163">xsd:string</span></span>  <br/> |<span data-ttu-id="dd1e4-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dd1e4-164">required</span></span>  <br/> |<span data-ttu-id="dd1e4-165">Задает имя универсального набора правил проверки.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="dd1e4-166">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dd1e4-166">Values of the xsd:string type.</span></span>  <br/> |
   

