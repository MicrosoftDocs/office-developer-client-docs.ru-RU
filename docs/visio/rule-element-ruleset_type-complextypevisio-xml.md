---
title: Элемент Rule (RuleSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет правило одного проверки в набор правил проверки схемы.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814688"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="8f678-103">Элемент Rule (RuleSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="8f678-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8f678-104">Представляет правило одного проверки в набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="8f678-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f678-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8f678-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f678-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8f678-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8f678-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="8f678-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8f678-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8f678-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8f678-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8f678-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8f678-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8f678-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8f678-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="8f678-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8f678-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="8f678-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f678-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8f678-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8f678-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f678-114">Elements and attributes</span></span>

<span data-ttu-id="8f678-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="8f678-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8f678-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8f678-116">Parent elements</span></span>

|<span data-ttu-id="8f678-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f678-117">**Element**</span></span>|<span data-ttu-id="8f678-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f678-118">**Type**</span></span>|<span data-ttu-id="8f678-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f678-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f678-120">Набор правил</span><span class="sxs-lookup"><span data-stu-id="8f678-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f678-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="8f678-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f678-122">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="8f678-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f678-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8f678-123">Child elements</span></span>

|<span data-ttu-id="8f678-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8f678-124">**Element**</span></span>|<span data-ttu-id="8f678-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f678-125">**Type**</span></span>|<span data-ttu-id="8f678-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f678-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f678-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="8f678-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f678-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="8f678-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f678-129">Задает логическое выражение, которое определяет, применяется ли правило проверки на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="8f678-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="8f678-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="8f678-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f678-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="8f678-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f678-132">Задает логическое выражение, которое определяет, удовлетворяет ли целевой объект правила проверки.</span><span class="sxs-lookup"><span data-stu-id="8f678-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8f678-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8f678-133">Attributes</span></span>

|<span data-ttu-id="8f678-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8f678-134">**Attribute**</span></span>|<span data-ttu-id="8f678-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8f678-135">**Type**</span></span>|<span data-ttu-id="8f678-136">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="8f678-136">**Required**</span></span>|<span data-ttu-id="8f678-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f678-137">**Description**</span></span>|<span data-ttu-id="8f678-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8f678-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8f678-139">Категория</span><span class="sxs-lookup"><span data-stu-id="8f678-139">Category</span></span>  <br/> |<span data-ttu-id="8f678-140">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8f678-140">xsd:string</span></span>  <br/> |<span data-ttu-id="8f678-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-141">optional</span></span>  <br/> |<span data-ttu-id="8f678-142">Задает текст, отображаемый в столбце **категории** окно вопросов.</span><span class="sxs-lookup"><span data-stu-id="8f678-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="8f678-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="8f678-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="8f678-144">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f678-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f678-145">Описание</span><span class="sxs-lookup"><span data-stu-id="8f678-145">Description</span></span>  <br/> |<span data-ttu-id="8f678-146">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8f678-146">xsd:string</span></span>  <br/> |<span data-ttu-id="8f678-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-147">optional</span></span>  <br/> |<span data-ttu-id="8f678-148">Задает описание правила проверки, который отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8f678-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="8f678-149">Значение по умолчанию — «Неизвестно».</span><span class="sxs-lookup"><span data-stu-id="8f678-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="8f678-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f678-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f678-151">ID</span><span class="sxs-lookup"><span data-stu-id="8f678-151">ID</span></span>  <br/> |<span data-ttu-id="8f678-152">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8f678-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8f678-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-153">required</span></span>  <br/> |<span data-ttu-id="8f678-154">Задает уникальный идентификатор для правила проверки.</span><span class="sxs-lookup"><span data-stu-id="8f678-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="8f678-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8f678-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8f678-156">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="8f678-156">Ignored</span></span>  <br/> |<span data-ttu-id="8f678-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="8f678-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8f678-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-158">optional</span></span>  <br/> |<span data-ttu-id="8f678-159">Указывает, учитывается ли правило проверки.</span><span class="sxs-lookup"><span data-stu-id="8f678-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="8f678-160">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="8f678-160">Default is False.</span></span>  <br/> |<span data-ttu-id="8f678-161">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8f678-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8f678-162">NameU</span><span class="sxs-lookup"><span data-stu-id="8f678-162">NameU</span></span>  <br/> |<span data-ttu-id="8f678-163">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8f678-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8f678-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-164">required</span></span>  <br/> |<span data-ttu-id="8f678-165">Задает имя универсальные правила проверки.</span><span class="sxs-lookup"><span data-stu-id="8f678-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="8f678-166">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8f678-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8f678-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="8f678-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="8f678-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8f678-168">xsd:int</span></span>  <br/> |<span data-ttu-id="8f678-169">необязательный</span><span class="sxs-lookup"><span data-stu-id="8f678-169">optional</span></span>  <br/> |<span data-ttu-id="8f678-170">Указывает тип объекта, к которому применяется правило проверки.</span><span class="sxs-lookup"><span data-stu-id="8f678-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="8f678-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8f678-171">Values of the xsd:int type.</span></span>  <br/> |
   

