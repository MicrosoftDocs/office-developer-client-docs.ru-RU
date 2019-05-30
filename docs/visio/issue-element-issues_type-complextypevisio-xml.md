---
title: Элемент Issue (Иссуес_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет одну ошибку проверки в документе.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541129"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="4519d-103">Элемент Issue (Иссуес_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4519d-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4519d-104">Представляет одну ошибку проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="4519d-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4519d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4519d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4519d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4519d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4519d-107">Иссуе_типе</span><span class="sxs-lookup"><span data-stu-id="4519d-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4519d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4519d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4519d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4519d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4519d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4519d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4519d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4519d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4519d-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="4519d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4519d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4519d-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4519d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4519d-114">Elements and attributes</span></span>

<span data-ttu-id="4519d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4519d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4519d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4519d-116">Parent elements</span></span>

|<span data-ttu-id="4519d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4519d-117">**Element**</span></span>|<span data-ttu-id="4519d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4519d-118">**Type**</span></span>|<span data-ttu-id="4519d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4519d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4519d-120">Issues</span><span class="sxs-lookup"><span data-stu-id="4519d-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4519d-121">Иссуес_типе</span><span class="sxs-lookup"><span data-stu-id="4519d-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4519d-122">Содержит все элементы **issue** для документа.</span><span class="sxs-lookup"><span data-stu-id="4519d-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4519d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4519d-123">Child elements</span></span>

|<span data-ttu-id="4519d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4519d-124">**Element**</span></span>|<span data-ttu-id="4519d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4519d-125">**Type**</span></span>|<span data-ttu-id="4519d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4519d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4519d-127">Иссуетаржет</span><span class="sxs-lookup"><span data-stu-id="4519d-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4519d-128">Иссуетаржет_типе</span><span class="sxs-lookup"><span data-stu-id="4519d-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4519d-129">В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="4519d-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="4519d-130">Рулеинфо</span><span class="sxs-lookup"><span data-stu-id="4519d-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4519d-131">Рулеинфо_типе</span><span class="sxs-lookup"><span data-stu-id="4519d-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4519d-132">Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="4519d-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4519d-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4519d-133">Attributes</span></span>

|<span data-ttu-id="4519d-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4519d-134">**Attribute**</span></span>|<span data-ttu-id="4519d-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4519d-135">**Type**</span></span>|<span data-ttu-id="4519d-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4519d-136">**Required**</span></span>|<span data-ttu-id="4519d-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4519d-137">**Description**</span></span>|<span data-ttu-id="4519d-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4519d-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4519d-139">ID</span><span class="sxs-lookup"><span data-stu-id="4519d-139">ID</span></span>  <br/> |<span data-ttu-id="4519d-140">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4519d-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4519d-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4519d-141">required</span></span>  <br/> |<span data-ttu-id="4519d-142">Указывает уникальный идентификатор для ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="4519d-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="4519d-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4519d-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4519d-144">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="4519d-144">Ignored</span></span>  <br/> |<span data-ttu-id="4519d-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4519d-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4519d-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="4519d-146">optional</span></span>  <br/> |<span data-ttu-id="4519d-147">Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="4519d-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="4519d-148">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4519d-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

