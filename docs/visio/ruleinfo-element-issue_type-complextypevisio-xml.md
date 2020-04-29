---
title: Элемент Рулеинфо (Issue_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541689"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="283de-103">Элемент Рулеинфо (Issue_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="283de-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="283de-104">Задает сведения о правиле проверки, к которым относится ошибка родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="283de-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="283de-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="283de-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="283de-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="283de-106">**Element type**</span></span> <br/> |[<span data-ttu-id="283de-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="283de-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="283de-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="283de-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="283de-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="283de-109">**Schema file**</span></span> <br/> |<span data-ttu-id="283de-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="283de-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="283de-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="283de-111">**Document parts**</span></span> <br/> |<span data-ttu-id="283de-112">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="283de-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="283de-113">Определение</span><span class="sxs-lookup"><span data-stu-id="283de-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="283de-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="283de-114">Elements and attributes</span></span>

<span data-ttu-id="283de-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="283de-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="283de-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="283de-116">Parent elements</span></span>

|<span data-ttu-id="283de-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="283de-117">**Element**</span></span>|<span data-ttu-id="283de-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="283de-118">**Type**</span></span>|<span data-ttu-id="283de-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="283de-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="283de-120">Проблема</span><span class="sxs-lookup"><span data-stu-id="283de-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="283de-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="283de-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="283de-122">Представляет одну ошибку проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="283de-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="283de-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="283de-123">Child elements</span></span>

<span data-ttu-id="283de-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="283de-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="283de-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="283de-125">Attributes</span></span>

|<span data-ttu-id="283de-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="283de-126">**Attribute**</span></span>|<span data-ttu-id="283de-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="283de-127">**Type**</span></span>|<span data-ttu-id="283de-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="283de-128">**Required**</span></span>|<span data-ttu-id="283de-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="283de-129">**Description**</span></span>|<span data-ttu-id="283de-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="283de-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="283de-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="283de-131">RuleID</span></span>  <br/> |<span data-ttu-id="283de-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="283de-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="283de-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="283de-133">required</span></span>  <br/> |<span data-ttu-id="283de-134">Задает уникальный идентификатор правила проверки, к которому относится родительская ошибка.</span><span class="sxs-lookup"><span data-stu-id="283de-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="283de-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="283de-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="283de-136">рулесетид</span><span class="sxs-lookup"><span data-stu-id="283de-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="283de-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="283de-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="283de-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="283de-138">required</span></span>  <br/> |<span data-ttu-id="283de-139">Задает уникальный идентификатор набора правил проверки, к которому относится родительская ошибка.</span><span class="sxs-lookup"><span data-stu-id="283de-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="283de-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="283de-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

