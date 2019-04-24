---
title: Элемент Rule (Рулесет_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Представляет одно правило проверки в наборе правил проверки схемы.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358802"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="93147-103">Элемент Rule (Рулесет_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="93147-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="93147-104">Представляет одно правило проверки в наборе правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="93147-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93147-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="93147-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93147-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="93147-106">**Element type**</span></span> <br/> |[<span data-ttu-id="93147-107">Руле_типе</span><span class="sxs-lookup"><span data-stu-id="93147-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="93147-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="93147-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="93147-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="93147-109">**Schema file**</span></span> <br/> |<span data-ttu-id="93147-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="93147-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="93147-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="93147-111">**Document parts**</span></span> <br/> |<span data-ttu-id="93147-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="93147-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="93147-113">Определение</span><span class="sxs-lookup"><span data-stu-id="93147-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="93147-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="93147-114">Elements and attributes</span></span>

<span data-ttu-id="93147-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="93147-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="93147-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="93147-116">Parent elements</span></span>

|<span data-ttu-id="93147-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="93147-117">**Element**</span></span>|<span data-ttu-id="93147-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93147-118">**Type**</span></span>|<span data-ttu-id="93147-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93147-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93147-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="93147-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93147-121">Рулесет_типе</span><span class="sxs-lookup"><span data-stu-id="93147-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93147-122">Представляет один набор правил проверки схемы.</span><span class="sxs-lookup"><span data-stu-id="93147-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="93147-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="93147-123">Child elements</span></span>

|<span data-ttu-id="93147-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="93147-124">**Element**</span></span>|<span data-ttu-id="93147-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93147-125">**Type**</span></span>|<span data-ttu-id="93147-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93147-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="93147-127">Рулефилтер</span><span class="sxs-lookup"><span data-stu-id="93147-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93147-128">Рулефилтер_типе</span><span class="sxs-lookup"><span data-stu-id="93147-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93147-129">Задает логическое выражение, определяющее, следует ли применять правило проверки к целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="93147-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="93147-130">Правила</span><span class="sxs-lookup"><span data-stu-id="93147-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="93147-131">Рулетест_типе</span><span class="sxs-lookup"><span data-stu-id="93147-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="93147-132">Задает логическое выражение, которое определяет, соответствует ли целевой объект правилу проверки.</span><span class="sxs-lookup"><span data-stu-id="93147-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="93147-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="93147-133">Attributes</span></span>

|<span data-ttu-id="93147-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="93147-134">**Attribute**</span></span>|<span data-ttu-id="93147-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93147-135">**Type**</span></span>|<span data-ttu-id="93147-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="93147-136">**Required**</span></span>|<span data-ttu-id="93147-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93147-137">**Description**</span></span>|<span data-ttu-id="93147-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="93147-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="93147-139">Категория</span><span class="sxs-lookup"><span data-stu-id="93147-139">Category</span></span>  <br/> |<span data-ttu-id="93147-140">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="93147-140">xsd:string</span></span>  <br/> |<span data-ttu-id="93147-141">необязательный</span><span class="sxs-lookup"><span data-stu-id="93147-141">optional</span></span>  <br/> |<span data-ttu-id="93147-142">Задает текст, отображаемый в столбце **категорий** окна "проблемы".</span><span class="sxs-lookup"><span data-stu-id="93147-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="93147-143">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="93147-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="93147-144">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="93147-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="93147-145">Описание</span><span class="sxs-lookup"><span data-stu-id="93147-145">Description</span></span>  <br/> |<span data-ttu-id="93147-146">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="93147-146">xsd:string</span></span>  <br/> |<span data-ttu-id="93147-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="93147-147">optional</span></span>  <br/> |<span data-ttu-id="93147-148">Задает описание правила проверки, которое отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93147-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="93147-149">Значение по умолчанию — "Unknown".</span><span class="sxs-lookup"><span data-stu-id="93147-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="93147-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="93147-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="93147-151">ИД</span><span class="sxs-lookup"><span data-stu-id="93147-151">ID</span></span>  <br/> |<span data-ttu-id="93147-152">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="93147-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="93147-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="93147-153">required</span></span>  <br/> |<span data-ttu-id="93147-154">Задает уникальный идентификатор для правила проверки.</span><span class="sxs-lookup"><span data-stu-id="93147-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="93147-155">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="93147-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="93147-156">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="93147-156">Ignored</span></span>  <br/> |<span data-ttu-id="93147-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="93147-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="93147-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="93147-158">optional</span></span>  <br/> |<span data-ttu-id="93147-159">Указывает, игнорируется ли правило проверки.</span><span class="sxs-lookup"><span data-stu-id="93147-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="93147-160">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="93147-160">Default is False.</span></span>  <br/> |<span data-ttu-id="93147-161">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="93147-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="93147-162">NameU</span><span class="sxs-lookup"><span data-stu-id="93147-162">NameU</span></span>  <br/> |<span data-ttu-id="93147-163">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="93147-163">xsd:string</span></span>  <br/> |<span data-ttu-id="93147-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="93147-164">required</span></span>  <br/> |<span data-ttu-id="93147-165">Задает универсальное имя правила проверки.</span><span class="sxs-lookup"><span data-stu-id="93147-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="93147-166">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="93147-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="93147-167">Рулетаржет</span><span class="sxs-lookup"><span data-stu-id="93147-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="93147-168">XSD: int</span><span class="sxs-lookup"><span data-stu-id="93147-168">xsd:int</span></span>  <br/> |<span data-ttu-id="93147-169">необязательный</span><span class="sxs-lookup"><span data-stu-id="93147-169">optional</span></span>  <br/> |<span data-ttu-id="93147-170">Указывает тип объекта, к которому применяется правило проверки.</span><span class="sxs-lookup"><span data-stu-id="93147-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="93147-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="93147-171">Values of the xsd:int type.</span></span>  <br/> |
   

