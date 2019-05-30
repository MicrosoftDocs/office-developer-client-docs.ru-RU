---
title: Элемент Иссуетаржет (Иссуе_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки. Если целью родительской ошибки проверки является документ, Иссуетаржет спеЦифес ни страницу, ни фигуру.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542956"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="40dc8-104">Элемент Иссуетаржет (Иссуе_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="40dc8-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="40dc8-105">В зависимости от цели родительской ошибки проверки указывает либо страницу, либо и фигуру, и страницу, связанную с ошибкой родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="40dc8-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="40dc8-106">Если целью родительской ошибки проверки является документ, **иссуетаржет** спеЦифес ни страницу, ни фигуру.</span><span class="sxs-lookup"><span data-stu-id="40dc8-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="40dc8-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="40dc8-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40dc8-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="40dc8-108">**Element type**</span></span> <br/> |[<span data-ttu-id="40dc8-109">Иссуетаржет_типе</span><span class="sxs-lookup"><span data-stu-id="40dc8-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="40dc8-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="40dc8-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="40dc8-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="40dc8-111">**Schema file**</span></span> <br/> |<span data-ttu-id="40dc8-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="40dc8-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="40dc8-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="40dc8-113">**Document parts**</span></span> <br/> |<span data-ttu-id="40dc8-114">Проверка. XML</span><span class="sxs-lookup"><span data-stu-id="40dc8-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40dc8-115">Определение</span><span class="sxs-lookup"><span data-stu-id="40dc8-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="40dc8-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="40dc8-116">Elements and attributes</span></span>

<span data-ttu-id="40dc8-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="40dc8-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="40dc8-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="40dc8-118">Parent elements</span></span>

|<span data-ttu-id="40dc8-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="40dc8-119">**Element**</span></span>|<span data-ttu-id="40dc8-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="40dc8-120">**Type**</span></span>|<span data-ttu-id="40dc8-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40dc8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40dc8-122">Проблема</span><span class="sxs-lookup"><span data-stu-id="40dc8-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40dc8-123">Иссуе_типе</span><span class="sxs-lookup"><span data-stu-id="40dc8-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40dc8-124">Представляет одну ошибку проверки в документе.</span><span class="sxs-lookup"><span data-stu-id="40dc8-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40dc8-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="40dc8-125">Child elements</span></span>

<span data-ttu-id="40dc8-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="40dc8-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40dc8-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="40dc8-127">Attributes</span></span>

|<span data-ttu-id="40dc8-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="40dc8-128">**Attribute**</span></span>|<span data-ttu-id="40dc8-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="40dc8-129">**Type**</span></span>|<span data-ttu-id="40dc8-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="40dc8-130">**Required**</span></span>|<span data-ttu-id="40dc8-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40dc8-131">**Description**</span></span>|<span data-ttu-id="40dc8-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="40dc8-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40dc8-133">PageID</span><span class="sxs-lookup"><span data-stu-id="40dc8-133">PageID</span></span>  <br/> |<span data-ttu-id="40dc8-134">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="40dc8-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40dc8-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="40dc8-135">required</span></span>  <br/> |<span data-ttu-id="40dc8-136">Задает уникальный идентификатор страницы, связанной с ошибкой родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="40dc8-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="40dc8-137">Если целевым объектом является документ, значение Пажеид может быть 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="40dc8-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="40dc8-138">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="40dc8-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="40dc8-139">Шапеид</span><span class="sxs-lookup"><span data-stu-id="40dc8-139">ShapeID</span></span>  <br/> |<span data-ttu-id="40dc8-140">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="40dc8-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="40dc8-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="40dc8-141">required</span></span>  <br/> |<span data-ttu-id="40dc8-142">Задает уникальный идентификатор фигуры, связанной с ошибкой родительской проверки.</span><span class="sxs-lookup"><span data-stu-id="40dc8-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="40dc8-143">Если целевым объектом является документ или страница, значение Шапеид может быть 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="40dc8-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="40dc8-144">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="40dc8-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

