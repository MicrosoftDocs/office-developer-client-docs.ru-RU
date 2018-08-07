---
title: Элемент проблему (Issues_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет ошибки проверки одного документа.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814010"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="6ebd0-103">Элемент проблему (Issues_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="6ebd0-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6ebd0-104">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ebd0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6ebd0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ebd0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6ebd0-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="6ebd0-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6ebd0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6ebd0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6ebd0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6ebd0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6ebd0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6ebd0-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="6ebd0-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ebd0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6ebd0-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ebd0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ebd0-114">Elements and attributes</span></span>

<span data-ttu-id="6ebd0-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6ebd0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6ebd0-116">Parent elements</span></span>

|<span data-ttu-id="6ebd0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-117">**Element**</span></span>|<span data-ttu-id="6ebd0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-118">**Type**</span></span>|<span data-ttu-id="6ebd0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ebd0-120">Проблемы</span><span class="sxs-lookup"><span data-stu-id="6ebd0-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ebd0-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="6ebd0-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ebd0-122">Содержит все элементы **проблему** для документа.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ebd0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6ebd0-123">Child elements</span></span>

|<span data-ttu-id="6ebd0-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-124">**Element**</span></span>|<span data-ttu-id="6ebd0-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-125">**Type**</span></span>|<span data-ttu-id="6ebd0-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ebd0-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="6ebd0-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ebd0-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="6ebd0-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ebd0-129">В зависимости от целевого родительский ошибки проверки указывает либо страницы или страницы и фигуры, связанного с родительской ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="6ebd0-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="6ebd0-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ebd0-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="6ebd0-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ebd0-132">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6ebd0-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ebd0-133">Attributes</span></span>

|<span data-ttu-id="6ebd0-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-134">**Attribute**</span></span>|<span data-ttu-id="6ebd0-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-135">**Type**</span></span>|<span data-ttu-id="6ebd0-136">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-136">**Required**</span></span>|<span data-ttu-id="6ebd0-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-137">**Description**</span></span>|<span data-ttu-id="6ebd0-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6ebd0-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6ebd0-139">ID</span><span class="sxs-lookup"><span data-stu-id="6ebd0-139">ID</span></span>  <br/> |<span data-ttu-id="6ebd0-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ebd0-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6ebd0-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6ebd0-141">required</span></span>  <br/> |<span data-ttu-id="6ebd0-142">Задает уникальный идентификатор ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="6ebd0-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6ebd0-144">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="6ebd0-144">Ignored</span></span>  <br/> |<span data-ttu-id="6ebd0-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="6ebd0-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6ebd0-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="6ebd0-146">optional</span></span>  <br/> |<span data-ttu-id="6ebd0-147">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="6ebd0-148">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6ebd0-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

