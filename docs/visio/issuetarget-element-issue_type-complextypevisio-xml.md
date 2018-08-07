---
title: Элемент IssueTarget (Issue_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: В зависимости от целевого родительский ошибки проверки указывает либо страницы или страницы и фигуры, связанного с родительской ошибки проверки. Если целевой ошибки проверки родительского документа, указывающий IssueTarget страница ни в форму.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814027"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="1ca70-104">Элемент IssueTarget (Issue_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1ca70-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1ca70-105">В зависимости от целевого родительский ошибки проверки указывает либо страницы или страницы и фигуры, связанного с родительской ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="1ca70-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="1ca70-106">Если целевой ошибки проверки родительского документа, указывающий **IssueTarget** страница ни в форму.</span><span class="sxs-lookup"><span data-stu-id="1ca70-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1ca70-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1ca70-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ca70-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1ca70-108">**Element type**</span></span> <br/> |[<span data-ttu-id="1ca70-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="1ca70-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ca70-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1ca70-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ca70-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1ca70-111">**Schema file**</span></span> <br/> |<span data-ttu-id="1ca70-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1ca70-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ca70-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="1ca70-113">**Document parts**</span></span> <br/> |<span data-ttu-id="1ca70-114">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="1ca70-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ca70-115">Определение</span><span class="sxs-lookup"><span data-stu-id="1ca70-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ca70-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ca70-116">Elements and attributes</span></span>

<span data-ttu-id="1ca70-117">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="1ca70-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ca70-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1ca70-118">Parent elements</span></span>

|<span data-ttu-id="1ca70-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1ca70-119">**Element**</span></span>|<span data-ttu-id="1ca70-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1ca70-120">**Type**</span></span>|<span data-ttu-id="1ca70-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ca70-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ca70-122">Проблема</span><span class="sxs-lookup"><span data-stu-id="1ca70-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ca70-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="1ca70-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ca70-124">Представляет ошибки проверки одного документа.</span><span class="sxs-lookup"><span data-stu-id="1ca70-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ca70-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1ca70-125">Child elements</span></span>

<span data-ttu-id="1ca70-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="1ca70-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ca70-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ca70-127">Attributes</span></span>

|<span data-ttu-id="1ca70-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1ca70-128">**Attribute**</span></span>|<span data-ttu-id="1ca70-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1ca70-129">**Type**</span></span>|<span data-ttu-id="1ca70-130">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="1ca70-130">**Required**</span></span>|<span data-ttu-id="1ca70-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ca70-131">**Description**</span></span>|<span data-ttu-id="1ca70-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1ca70-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ca70-133">PageID</span><span class="sxs-lookup"><span data-stu-id="1ca70-133">PageID</span></span>  <br/> |<span data-ttu-id="1ca70-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ca70-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ca70-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ca70-135">required</span></span>  <br/> |<span data-ttu-id="1ca70-136">Задает уникальный идентификатор страницы, который связан с родительской ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="1ca70-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="1ca70-137">Если целевой документ, PageID значение может быть 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1ca70-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="1ca70-138">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ca70-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ca70-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1ca70-139">ShapeID</span></span>  <br/> |<span data-ttu-id="1ca70-140">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ca70-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ca70-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ca70-141">required</span></span>  <br/> |<span data-ttu-id="1ca70-142">Задает уникальный идентификатор фигуры, связанного с родительской ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="1ca70-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="1ca70-143">Если целевая база данных документа или страницы, ShapeID значение может быть 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1ca70-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="1ca70-144">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ca70-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

