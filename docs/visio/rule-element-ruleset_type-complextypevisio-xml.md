---
title: Элемент Rule (RuleSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет правило одного проверки в набор правил проверки схемы.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395912"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="65c52-103">Элемент Rule (RuleSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="65c52-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="65c52-104">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="65c52-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65c52-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="65c52-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65c52-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="65c52-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65c52-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65c52-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="65c52-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65c52-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="65c52-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65c52-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="65c52-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65c52-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="65c52-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65c52-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="65c52-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65c52-113">Определение</span><span class="sxs-lookup"><span data-stu-id="65c52-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65c52-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="65c52-114">Elements and attributes</span></span>

<span data-ttu-id="65c52-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="65c52-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65c52-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="65c52-116">Parent elements</span></span>

|<span data-ttu-id="65c52-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="65c52-117">**Element**</span></span>|<span data-ttu-id="65c52-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="65c52-118">**Type**</span></span>|<span data-ttu-id="65c52-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65c52-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65c52-120">Набор правил</span><span class="sxs-lookup"><span data-stu-id="65c52-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65c52-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65c52-122">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="65c52-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65c52-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65c52-123">Child elements</span></span>

|<span data-ttu-id="65c52-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="65c52-124">**Element**</span></span>|<span data-ttu-id="65c52-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="65c52-125">**Type**</span></span>|<span data-ttu-id="65c52-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65c52-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65c52-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="65c52-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65c52-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65c52-129">Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="65c52-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="65c52-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="65c52-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65c52-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="65c52-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65c52-132">Задает логическое выражение, которое определяет, удовлетворяет ли целевой объект правила проверки.</span><span class="sxs-lookup"><span data-stu-id="65c52-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="65c52-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="65c52-133">Attributes</span></span>

|<span data-ttu-id="65c52-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="65c52-134">**Attribute**</span></span>|<span data-ttu-id="65c52-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="65c52-135">**Type**</span></span>|<span data-ttu-id="65c52-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="65c52-136">**Required**</span></span>|<span data-ttu-id="65c52-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65c52-137">**Description**</span></span>|<span data-ttu-id="65c52-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="65c52-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65c52-139">Категория</span><span class="sxs-lookup"><span data-stu-id="65c52-139">Category</span></span>  <br/> |<span data-ttu-id="65c52-140">XSD:String</span><span class="sxs-lookup"><span data-stu-id="65c52-140">xsd:string</span></span>  <br/> |<span data-ttu-id="65c52-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-141">optional</span></span>  <br/> |<span data-ttu-id="65c52-142">Задает текст, отображаемый в столбце **категории** окно вопросов.</span><span class="sxs-lookup"><span data-stu-id="65c52-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="65c52-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="65c52-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="65c52-144">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65c52-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65c52-145">Описание</span><span class="sxs-lookup"><span data-stu-id="65c52-145">Description</span></span>  <br/> |<span data-ttu-id="65c52-146">XSD:String</span><span class="sxs-lookup"><span data-stu-id="65c52-146">xsd:string</span></span>  <br/> |<span data-ttu-id="65c52-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-147">optional</span></span>  <br/> |<span data-ttu-id="65c52-148">Задает описание правила проверки, который отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="65c52-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="65c52-149">Значение по умолчанию — «Неизвестно».</span><span class="sxs-lookup"><span data-stu-id="65c52-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="65c52-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65c52-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65c52-151">ID</span><span class="sxs-lookup"><span data-stu-id="65c52-151">ID</span></span>  <br/> |<span data-ttu-id="65c52-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65c52-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65c52-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-153">required</span></span>  <br/> |<span data-ttu-id="65c52-154">Задает уникальный идентификатор для правила проверки.</span><span class="sxs-lookup"><span data-stu-id="65c52-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="65c52-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65c52-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65c52-156">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="65c52-156">Ignored</span></span>  <br/> |<span data-ttu-id="65c52-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="65c52-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65c52-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-158">optional</span></span>  <br/> |<span data-ttu-id="65c52-159">Указывает, учитывается ли правило проверки.</span><span class="sxs-lookup"><span data-stu-id="65c52-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="65c52-160">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="65c52-160">Default is False.</span></span>  <br/> |<span data-ttu-id="65c52-161">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="65c52-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="65c52-162">NameU</span><span class="sxs-lookup"><span data-stu-id="65c52-162">NameU</span></span>  <br/> |<span data-ttu-id="65c52-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="65c52-163">xsd:string</span></span>  <br/> |<span data-ttu-id="65c52-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-164">required</span></span>  <br/> |<span data-ttu-id="65c52-165">Задает имя универсальные правила проверки.</span><span class="sxs-lookup"><span data-stu-id="65c52-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="65c52-166">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="65c52-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="65c52-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="65c52-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="65c52-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="65c52-168">xsd:int</span></span>  <br/> |<span data-ttu-id="65c52-169">необязательный</span><span class="sxs-lookup"><span data-stu-id="65c52-169">optional</span></span>  <br/> |<span data-ttu-id="65c52-170">Указывает тип объекта, к которому применяется правило проверки.</span><span class="sxs-lookup"><span data-stu-id="65c52-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="65c52-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="65c52-171">Values of the xsd:int type.</span></span>  <br/> |
   

