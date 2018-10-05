---
title: Элемент RuleInfo (Issue_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Задает сведения о правиле проверки, относящимися ошибки проверки родительского.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394750"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="cd1cb-103">Элемент RuleInfo (Issue_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="cd1cb-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cd1cb-104">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd1cb-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cd1cb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd1cb-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cd1cb-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="cd1cb-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cd1cb-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cd1cb-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cd1cb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cd1cb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cd1cb-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cd1cb-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="cd1cb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cd1cb-113">Определение</span><span class="sxs-lookup"><span data-stu-id="cd1cb-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cd1cb-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cd1cb-114">Elements and attributes</span></span>

<span data-ttu-id="cd1cb-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cd1cb-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cd1cb-116">Parent elements</span></span>

|<span data-ttu-id="cd1cb-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-117">**Element**</span></span>|<span data-ttu-id="cd1cb-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-118">**Type**</span></span>|<span data-ttu-id="cd1cb-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cd1cb-120">Проблема</span><span class="sxs-lookup"><span data-stu-id="cd1cb-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cd1cb-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="cd1cb-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cd1cb-122">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd1cb-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cd1cb-123">Child elements</span></span>

<span data-ttu-id="cd1cb-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd1cb-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cd1cb-125">Attributes</span></span>

|<span data-ttu-id="cd1cb-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-126">**Attribute**</span></span>|<span data-ttu-id="cd1cb-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-127">**Type**</span></span>|<span data-ttu-id="cd1cb-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-128">**Required**</span></span>|<span data-ttu-id="cd1cb-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-129">**Description**</span></span>|<span data-ttu-id="cd1cb-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="cd1cb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cd1cb-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="cd1cb-131">RuleID</span></span>  <br/> |<span data-ttu-id="cd1cb-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cd1cb-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cd1cb-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cd1cb-133">required</span></span>  <br/> |<span data-ttu-id="cd1cb-134">Задает уникальный идентификатор правила проверки, проблема родительского относится к.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="cd1cb-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cd1cb-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="cd1cb-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="cd1cb-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cd1cb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cd1cb-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cd1cb-138">required</span></span>  <br/> |<span data-ttu-id="cd1cb-139">Указывает уникальный идентификатор набора правил проверки, относящимися родительского проблему.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="cd1cb-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cd1cb-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

