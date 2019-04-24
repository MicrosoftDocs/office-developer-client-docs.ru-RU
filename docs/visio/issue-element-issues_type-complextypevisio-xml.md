---
title: Элемент Issue (Иссуес_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Представляет одну ошибку проверки в документе.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317908"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="a054f-103">Элемент Issue (Иссуес_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="a054f-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a054f-104">Представляет одну ошибку проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="a054f-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a054f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a054f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a054f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a054f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a054f-107">Иссуе_типе</span><span class="sxs-lookup"><span data-stu-id="a054f-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a054f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a054f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a054f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a054f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a054f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a054f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a054f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="a054f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a054f-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="a054f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a054f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a054f-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a054f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a054f-114">Elements and attributes</span></span>

<span data-ttu-id="a054f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a054f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a054f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a054f-116">Parent elements</span></span>

|<span data-ttu-id="a054f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a054f-117">**Element**</span></span>|<span data-ttu-id="a054f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a054f-118">**Type**</span></span>|<span data-ttu-id="a054f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a054f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a054f-120">Issues</span><span class="sxs-lookup"><span data-stu-id="a054f-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a054f-121">Иссуес_типе</span><span class="sxs-lookup"><span data-stu-id="a054f-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a054f-122">Содержит все элементы **issue** для документа.</span><span class="sxs-lookup"><span data-stu-id="a054f-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a054f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a054f-123">Child elements</span></span>

|<span data-ttu-id="a054f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a054f-124">**Element**</span></span>|<span data-ttu-id="a054f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a054f-125">**Type**</span></span>|<span data-ttu-id="a054f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a054f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a054f-127">Иссуетаржет</span><span class="sxs-lookup"><span data-stu-id="a054f-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a054f-128">Иссуетаржет_типе</span><span class="sxs-lookup"><span data-stu-id="a054f-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a054f-129">В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="a054f-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="a054f-130">Рулеинфо</span><span class="sxs-lookup"><span data-stu-id="a054f-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a054f-131">Рулеинфо_типе</span><span class="sxs-lookup"><span data-stu-id="a054f-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a054f-132">Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="a054f-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a054f-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a054f-133">Attributes</span></span>

|<span data-ttu-id="a054f-134">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a054f-134">**Attribute**</span></span>|<span data-ttu-id="a054f-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a054f-135">**Type**</span></span>|<span data-ttu-id="a054f-136">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a054f-136">**Required**</span></span>|<span data-ttu-id="a054f-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a054f-137">**Description**</span></span>|<span data-ttu-id="a054f-138">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a054f-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a054f-139">ИД</span><span class="sxs-lookup"><span data-stu-id="a054f-139">ID</span></span>  <br/> |<span data-ttu-id="a054f-140">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a054f-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a054f-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a054f-141">required</span></span>  <br/> |<span data-ttu-id="a054f-142">Указывает уникальный идентификатор для ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="a054f-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="a054f-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a054f-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a054f-144">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="a054f-144">Ignored</span></span>  <br/> |<span data-ttu-id="a054f-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="a054f-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a054f-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="a054f-146">optional</span></span>  <br/> |<span data-ttu-id="a054f-147">Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="a054f-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="a054f-148">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a054f-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

