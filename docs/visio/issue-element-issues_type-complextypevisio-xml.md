---
title: Элемент issue (Issues_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет одну проблему проверки в документе.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541129"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="5112b-103">Элемент issue (Issues_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5112b-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5112b-104">Представляет одну проблему проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="5112b-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5112b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5112b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5112b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5112b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5112b-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="5112b-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5112b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5112b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5112b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5112b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5112b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5112b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5112b-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="5112b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5112b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="5112b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5112b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5112b-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5112b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5112b-114">Elements and attributes</span></span>

<span data-ttu-id="5112b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5112b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5112b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5112b-116">Parent elements</span></span>

|<span data-ttu-id="5112b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5112b-117">**Element**</span></span>|<span data-ttu-id="5112b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5112b-118">**Type**</span></span>|<span data-ttu-id="5112b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5112b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5112b-120">Issues</span><span class="sxs-lookup"><span data-stu-id="5112b-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5112b-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5112b-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5112b-122">Содержит все **элементы Issue** для документа.</span><span class="sxs-lookup"><span data-stu-id="5112b-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5112b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5112b-123">Child elements</span></span>

|<span data-ttu-id="5112b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5112b-124">**Element**</span></span>|<span data-ttu-id="5112b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5112b-125">**Type**</span></span>|<span data-ttu-id="5112b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5112b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5112b-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="5112b-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5112b-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="5112b-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5112b-129">В зависимости от цели родительской проблемы проверки указывается страница или страница и форма, связанные с родительской проблемой проверки.</span><span class="sxs-lookup"><span data-stu-id="5112b-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="5112b-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="5112b-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5112b-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="5112b-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5112b-132">Указывает сведения о правиле проверки, к который относится родительская проблема проверки.</span><span class="sxs-lookup"><span data-stu-id="5112b-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5112b-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5112b-133">Attributes</span></span>

|<span data-ttu-id="5112b-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5112b-134">**Attribute**</span></span>|<span data-ttu-id="5112b-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5112b-135">**Type**</span></span>|<span data-ttu-id="5112b-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5112b-136">**Required**</span></span>|<span data-ttu-id="5112b-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5112b-137">**Description**</span></span>|<span data-ttu-id="5112b-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5112b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5112b-139">ID</span><span class="sxs-lookup"><span data-stu-id="5112b-139">ID</span></span>  <br/> |<span data-ttu-id="5112b-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5112b-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5112b-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5112b-141">required</span></span>  <br/> |<span data-ttu-id="5112b-142">Указывает уникальный идентификатор проблемы проверки.</span><span class="sxs-lookup"><span data-stu-id="5112b-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="5112b-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5112b-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5112b-144">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="5112b-144">Ignored</span></span>  <br/> |<span data-ttu-id="5112b-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5112b-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5112b-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="5112b-146">optional</span></span>  <br/> |<span data-ttu-id="5112b-147">Указывает сведения о правиле проверки, к который относится родительская проблема проверки.</span><span class="sxs-lookup"><span data-stu-id="5112b-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="5112b-148">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5112b-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

