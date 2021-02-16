---
title: Элемент Rule (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет одно правило проверки в наборе правил проверки схемы.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541710"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="0a41b-103">Элемент Rule (RuleSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0a41b-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0a41b-104">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="0a41b-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a41b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0a41b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a41b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0a41b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0a41b-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="0a41b-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0a41b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0a41b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0a41b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0a41b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0a41b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0a41b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0a41b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0a41b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0a41b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="0a41b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a41b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0a41b-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0a41b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a41b-114">Elements and attributes</span></span>

<span data-ttu-id="0a41b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0a41b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0a41b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0a41b-116">Parent elements</span></span>

|<span data-ttu-id="0a41b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0a41b-117">**Element**</span></span>|<span data-ttu-id="0a41b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a41b-118">**Type**</span></span>|<span data-ttu-id="0a41b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a41b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a41b-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="0a41b-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0a41b-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="0a41b-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0a41b-122">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="0a41b-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0a41b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0a41b-123">Child elements</span></span>

|<span data-ttu-id="0a41b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0a41b-124">**Element**</span></span>|<span data-ttu-id="0a41b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a41b-125">**Type**</span></span>|<span data-ttu-id="0a41b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a41b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a41b-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="0a41b-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0a41b-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="0a41b-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0a41b-129">Указывает логическое выражение, которое определяет, следует ли применять правило проверки к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="0a41b-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="0a41b-130">RuleTest (тест правил)</span><span class="sxs-lookup"><span data-stu-id="0a41b-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0a41b-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="0a41b-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0a41b-132">Указывает логическое выражение, которое определяет, удовлетворяет ли целевой объект правилу проверки.</span><span class="sxs-lookup"><span data-stu-id="0a41b-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0a41b-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a41b-133">Attributes</span></span>

|<span data-ttu-id="0a41b-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0a41b-134">**Attribute**</span></span>|<span data-ttu-id="0a41b-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a41b-135">**Type**</span></span>|<span data-ttu-id="0a41b-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0a41b-136">**Required**</span></span>|<span data-ttu-id="0a41b-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a41b-137">**Description**</span></span>|<span data-ttu-id="0a41b-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0a41b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a41b-139">Category</span><span class="sxs-lookup"><span data-stu-id="0a41b-139">Category</span></span>  <br/> |<span data-ttu-id="0a41b-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0a41b-140">xsd:string</span></span>  <br/> |<span data-ttu-id="0a41b-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-141">optional</span></span>  <br/> |<span data-ttu-id="0a41b-142">Указывает текст, отображаемого в **столбце "Категория"** окна "Проблемы".</span><span class="sxs-lookup"><span data-stu-id="0a41b-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="0a41b-143">По умолчанию это пустая строка.</span><span class="sxs-lookup"><span data-stu-id="0a41b-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="0a41b-144">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a41b-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a41b-145">Описание</span><span class="sxs-lookup"><span data-stu-id="0a41b-145">Description</span></span>  <br/> |<span data-ttu-id="0a41b-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0a41b-146">xsd:string</span></span>  <br/> |<span data-ttu-id="0a41b-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-147">optional</span></span>  <br/> |<span data-ttu-id="0a41b-148">Указывает описание правила проверки, которое отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="0a41b-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="0a41b-149">Значение по умолчанию — Unknown (Неизвестно).</span><span class="sxs-lookup"><span data-stu-id="0a41b-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="0a41b-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a41b-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a41b-151">ID</span><span class="sxs-lookup"><span data-stu-id="0a41b-151">ID</span></span>  <br/> |<span data-ttu-id="0a41b-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a41b-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a41b-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-153">required</span></span>  <br/> |<span data-ttu-id="0a41b-154">Указывает уникальный идентификатор правила проверки.</span><span class="sxs-lookup"><span data-stu-id="0a41b-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="0a41b-155">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a41b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a41b-156">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="0a41b-156">Ignored</span></span>  <br/> |<span data-ttu-id="0a41b-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0a41b-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0a41b-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-158">optional</span></span>  <br/> |<span data-ttu-id="0a41b-159">Указывает, игнорируется ли правило проверки.</span><span class="sxs-lookup"><span data-stu-id="0a41b-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="0a41b-160">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="0a41b-160">Default is False.</span></span>  <br/> |<span data-ttu-id="0a41b-161">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0a41b-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0a41b-162">NameU</span><span class="sxs-lookup"><span data-stu-id="0a41b-162">NameU</span></span>  <br/> |<span data-ttu-id="0a41b-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0a41b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0a41b-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-164">required</span></span>  <br/> |<span data-ttu-id="0a41b-165">Указывает универсальное имя правила проверки.</span><span class="sxs-lookup"><span data-stu-id="0a41b-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="0a41b-166">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a41b-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a41b-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="0a41b-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="0a41b-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="0a41b-168">xsd:int</span></span>  <br/> |<span data-ttu-id="0a41b-169">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a41b-169">optional</span></span>  <br/> |<span data-ttu-id="0a41b-170">Указывает тип объекта, к которому применяется правило проверки.</span><span class="sxs-lookup"><span data-stu-id="0a41b-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="0a41b-171">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="0a41b-171">Values of the xsd:int type.</span></span>  <br/> |
   

