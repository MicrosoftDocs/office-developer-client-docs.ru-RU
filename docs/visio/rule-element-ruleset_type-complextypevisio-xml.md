---
title: Элемент Rule (RuleSet_Type complexType) (XML для Visio)
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
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="1c2f9-103">Элемент Rule (RuleSet_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1c2f9-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1c2f9-104">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c2f9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1c2f9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c2f9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1c2f9-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="1c2f9-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1c2f9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1c2f9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1c2f9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="1c2f9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1c2f9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1c2f9-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="1c2f9-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c2f9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="1c2f9-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1c2f9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1c2f9-114">Elements and attributes</span></span>

<span data-ttu-id="1c2f9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1c2f9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1c2f9-116">Parent elements</span></span>

|<span data-ttu-id="1c2f9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-117">**Element**</span></span>|<span data-ttu-id="1c2f9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-118">**Type**</span></span>|<span data-ttu-id="1c2f9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c2f9-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="1c2f9-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c2f9-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="1c2f9-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c2f9-122">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1c2f9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1c2f9-123">Child elements</span></span>

|<span data-ttu-id="1c2f9-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-124">**Element**</span></span>|<span data-ttu-id="1c2f9-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-125">**Type**</span></span>|<span data-ttu-id="1c2f9-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1c2f9-127">рулефилтер</span><span class="sxs-lookup"><span data-stu-id="1c2f9-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c2f9-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="1c2f9-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c2f9-129">Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="1c2f9-130">Правила</span><span class="sxs-lookup"><span data-stu-id="1c2f9-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1c2f9-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="1c2f9-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1c2f9-132">Задает логическое выражение, которое определяет, соответствует ли целевой объект правилу проверки.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1c2f9-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1c2f9-133">Attributes</span></span>

|<span data-ttu-id="1c2f9-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-134">**Attribute**</span></span>|<span data-ttu-id="1c2f9-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-135">**Type**</span></span>|<span data-ttu-id="1c2f9-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-136">**Required**</span></span>|<span data-ttu-id="1c2f9-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-137">**Description**</span></span>|<span data-ttu-id="1c2f9-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1c2f9-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c2f9-139">Категория</span><span class="sxs-lookup"><span data-stu-id="1c2f9-139">Category</span></span>  <br/> |<span data-ttu-id="1c2f9-140">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1c2f9-140">xsd:string</span></span>  <br/> |<span data-ttu-id="1c2f9-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-141">optional</span></span>  <br/> |<span data-ttu-id="1c2f9-142">Задает текст, отображаемый в столбце **категорий** окна "проблемы".</span><span class="sxs-lookup"><span data-stu-id="1c2f9-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="1c2f9-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="1c2f9-144">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c2f9-145">Описание</span><span class="sxs-lookup"><span data-stu-id="1c2f9-145">Description</span></span>  <br/> |<span data-ttu-id="1c2f9-146">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1c2f9-146">xsd:string</span></span>  <br/> |<span data-ttu-id="1c2f9-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-147">optional</span></span>  <br/> |<span data-ttu-id="1c2f9-148">Задает описание правила проверки, которое отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="1c2f9-149">Значение по умолчанию — "Unknown".</span><span class="sxs-lookup"><span data-stu-id="1c2f9-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="1c2f9-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c2f9-151">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="1c2f9-151">ID</span></span>  <br/> |<span data-ttu-id="1c2f9-152">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="1c2f9-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1c2f9-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-153">required</span></span>  <br/> |<span data-ttu-id="1c2f9-154">Задает уникальный идентификатор для правила проверки.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="1c2f9-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1c2f9-156">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="1c2f9-156">Ignored</span></span>  <br/> |<span data-ttu-id="1c2f9-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="1c2f9-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c2f9-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-158">optional</span></span>  <br/> |<span data-ttu-id="1c2f9-159">Указывает, игнорируется ли правило проверки.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="1c2f9-160">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-160">Default is False.</span></span>  <br/> |<span data-ttu-id="1c2f9-161">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c2f9-162">NameU</span><span class="sxs-lookup"><span data-stu-id="1c2f9-162">NameU</span></span>  <br/> |<span data-ttu-id="1c2f9-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1c2f9-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1c2f9-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-164">required</span></span>  <br/> |<span data-ttu-id="1c2f9-165">Задает универсальное имя правила проверки.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="1c2f9-166">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c2f9-167">рулетаржет</span><span class="sxs-lookup"><span data-stu-id="1c2f9-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="1c2f9-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1c2f9-168">xsd:int</span></span>  <br/> |<span data-ttu-id="1c2f9-169">необязательный</span><span class="sxs-lookup"><span data-stu-id="1c2f9-169">optional</span></span>  <br/> |<span data-ttu-id="1c2f9-170">Указывает тип объекта, к которому применяется правило проверки.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="1c2f9-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1c2f9-171">Values of the xsd:int type.</span></span>  <br/> |
   

