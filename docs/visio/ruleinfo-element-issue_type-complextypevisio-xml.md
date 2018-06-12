---
title: Элемент RuleInfo (Issue_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Задает сведения о правиле проверки, относящимися ошибки проверки родительского.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814691"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="73521-103">Элемент RuleInfo (Issue_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="73521-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="73521-104">Задает сведения о правиле проверки, относящимися ошибки проверки родительского.</span><span class="sxs-lookup"><span data-stu-id="73521-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73521-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="73521-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73521-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="73521-106">**Element type**</span></span> <br/> |[<span data-ttu-id="73521-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="73521-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="73521-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="73521-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="73521-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="73521-109">**Schema file**</span></span> <br/> |<span data-ttu-id="73521-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="73521-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="73521-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="73521-111">**Document parts**</span></span> <br/> |<span data-ttu-id="73521-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="73521-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73521-113">Определение</span><span class="sxs-lookup"><span data-stu-id="73521-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="73521-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="73521-114">Elements and attributes</span></span>

<span data-ttu-id="73521-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="73521-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="73521-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="73521-116">Parent elements</span></span>

|<span data-ttu-id="73521-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="73521-117">**Element**</span></span>|<span data-ttu-id="73521-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="73521-118">**Type**</span></span>|<span data-ttu-id="73521-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73521-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73521-120">Проблема</span><span class="sxs-lookup"><span data-stu-id="73521-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="73521-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="73521-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="73521-122">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="73521-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73521-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="73521-123">Child elements</span></span>

<span data-ttu-id="73521-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="73521-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73521-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="73521-125">Attributes</span></span>

|<span data-ttu-id="73521-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="73521-126">**Attribute**</span></span>|<span data-ttu-id="73521-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="73521-127">**Type**</span></span>|<span data-ttu-id="73521-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="73521-128">**Required**</span></span>|<span data-ttu-id="73521-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73521-129">**Description**</span></span>|<span data-ttu-id="73521-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="73521-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73521-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="73521-131">RuleID</span></span>  <br/> |<span data-ttu-id="73521-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="73521-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="73521-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="73521-133">required</span></span>  <br/> |<span data-ttu-id="73521-134">Задает уникальный идентификатор правила проверки, проблема родительского относится к.</span><span class="sxs-lookup"><span data-stu-id="73521-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="73521-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="73521-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="73521-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="73521-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="73521-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="73521-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="73521-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="73521-138">required</span></span>  <br/> |<span data-ttu-id="73521-139">Указывает уникальный идентификатор набора правил проверки, относящимися родительского проблему.</span><span class="sxs-lookup"><span data-stu-id="73521-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="73521-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="73521-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

