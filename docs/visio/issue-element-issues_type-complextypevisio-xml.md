---
title: Элемент проблему (Issues_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет ошибки проверки одного документа.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389843"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="5cafd-103">Элемент проблему (Issues_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5cafd-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5cafd-104">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="5cafd-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cafd-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5cafd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cafd-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5cafd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5cafd-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="5cafd-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5cafd-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5cafd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5cafd-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5cafd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5cafd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5cafd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5cafd-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5cafd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5cafd-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="5cafd-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5cafd-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5cafd-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5cafd-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5cafd-114">Elements and attributes</span></span>

<span data-ttu-id="5cafd-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5cafd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5cafd-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5cafd-116">Parent elements</span></span>

|<span data-ttu-id="5cafd-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5cafd-117">**Element**</span></span>|<span data-ttu-id="5cafd-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5cafd-118">**Type**</span></span>|<span data-ttu-id="5cafd-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cafd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cafd-120">Проблемы</span><span class="sxs-lookup"><span data-stu-id="5cafd-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cafd-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5cafd-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cafd-122">Содержит все элементы **проблему** для документа.</span><span class="sxs-lookup"><span data-stu-id="5cafd-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5cafd-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5cafd-123">Child elements</span></span>

|<span data-ttu-id="5cafd-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5cafd-124">**Element**</span></span>|<span data-ttu-id="5cafd-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5cafd-125">**Type**</span></span>|<span data-ttu-id="5cafd-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cafd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cafd-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="5cafd-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cafd-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="5cafd-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cafd-129">В зависимости от целевого родительский ошибки проверки указывает либо страницы или страницы и фигуры, связанного с родительской ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="5cafd-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="5cafd-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="5cafd-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cafd-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="5cafd-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cafd-132">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="5cafd-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5cafd-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5cafd-133">Attributes</span></span>

|<span data-ttu-id="5cafd-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5cafd-134">**Attribute**</span></span>|<span data-ttu-id="5cafd-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5cafd-135">**Type**</span></span>|<span data-ttu-id="5cafd-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5cafd-136">**Required**</span></span>|<span data-ttu-id="5cafd-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cafd-137">**Description**</span></span>|<span data-ttu-id="5cafd-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5cafd-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5cafd-139">ID</span><span class="sxs-lookup"><span data-stu-id="5cafd-139">ID</span></span>  <br/> |<span data-ttu-id="5cafd-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5cafd-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5cafd-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5cafd-141">required</span></span>  <br/> |<span data-ttu-id="5cafd-142">Задает уникальный идентификатор ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="5cafd-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="5cafd-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5cafd-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5cafd-144">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="5cafd-144">Ignored</span></span>  <br/> |<span data-ttu-id="5cafd-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="5cafd-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5cafd-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="5cafd-146">optional</span></span>  <br/> |<span data-ttu-id="5cafd-147">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="5cafd-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="5cafd-148">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5cafd-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

