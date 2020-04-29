---
title: Элемент Комментентри (CommentList_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документе.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540114"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="01b69-103">Элемент Комментентри (CommentList_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="01b69-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="01b69-104">Задает свойства, используемые для идентификации комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="01b69-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01b69-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="01b69-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01b69-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="01b69-106">**Element type**</span></span> <br/> |[<span data-ttu-id="01b69-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="01b69-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="01b69-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="01b69-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="01b69-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="01b69-109">**Schema file**</span></span> <br/> |<span data-ttu-id="01b69-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="01b69-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="01b69-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="01b69-111">**Document parts**</span></span> <br/> |<span data-ttu-id="01b69-112">Comments. XML</span><span class="sxs-lookup"><span data-stu-id="01b69-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01b69-113">Определение</span><span class="sxs-lookup"><span data-stu-id="01b69-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="01b69-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="01b69-114">Elements and attributes</span></span>

<span data-ttu-id="01b69-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="01b69-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="01b69-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="01b69-116">Parent elements</span></span>

|<span data-ttu-id="01b69-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="01b69-117">**Element**</span></span>|<span data-ttu-id="01b69-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01b69-118">**Type**</span></span>|<span data-ttu-id="01b69-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01b69-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01b69-120">комментлист</span><span class="sxs-lookup"><span data-stu-id="01b69-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01b69-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="01b69-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01b69-122">Задает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="01b69-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01b69-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="01b69-123">Child elements</span></span>

<span data-ttu-id="01b69-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="01b69-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01b69-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="01b69-125">Attributes</span></span>

|<span data-ttu-id="01b69-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="01b69-126">**Attribute**</span></span>|<span data-ttu-id="01b69-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01b69-127">**Type**</span></span>|<span data-ttu-id="01b69-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="01b69-128">**Required**</span></span>|<span data-ttu-id="01b69-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01b69-129">**Description**</span></span>|<span data-ttu-id="01b69-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="01b69-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01b69-131">аусорид</span><span class="sxs-lookup"><span data-stu-id="01b69-131">AuthorID</span></span>  <br/> |<span data-ttu-id="01b69-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01b69-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b69-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-133">required</span></span>  <br/> |<span data-ttu-id="01b69-134">Значение с отзначением от единицы, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="01b69-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="01b69-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01b69-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01b69-136">комментид</span><span class="sxs-lookup"><span data-stu-id="01b69-136">CommentID</span></span>  <br/> |<span data-ttu-id="01b69-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01b69-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b69-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-138">required</span></span>  <br/> |<span data-ttu-id="01b69-139">Уникальное значение, идентифицирующее комментарий на странице документа.</span><span class="sxs-lookup"><span data-stu-id="01b69-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="01b69-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01b69-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01b69-141">Дата</span><span class="sxs-lookup"><span data-stu-id="01b69-141">Date</span></span>  <br/> |<span data-ttu-id="01b69-142">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="01b69-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="01b69-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-143">required</span></span>  <br/> |<span data-ttu-id="01b69-144">Указывает, когда был создан комментарий.</span><span class="sxs-lookup"><span data-stu-id="01b69-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="01b69-145">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="01b69-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="01b69-146">Готово</span><span class="sxs-lookup"><span data-stu-id="01b69-146">Done</span></span>  <br/> |<span data-ttu-id="01b69-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="01b69-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="01b69-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-148">optional</span></span>  <br/> |<span data-ttu-id="01b69-149">Задает текущее состояние комментария.</span><span class="sxs-lookup"><span data-stu-id="01b69-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="01b69-150">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="01b69-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="01b69-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="01b69-151">EditDate</span></span>  <br/> |<span data-ttu-id="01b69-152">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="01b69-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="01b69-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-153">optional</span></span>  <br/> |<span data-ttu-id="01b69-154">Указывает время последнего изменения комментария.</span><span class="sxs-lookup"><span data-stu-id="01b69-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="01b69-155">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="01b69-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="01b69-156">PageID</span><span class="sxs-lookup"><span data-stu-id="01b69-156">PageID</span></span>  <br/> |<span data-ttu-id="01b69-157">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01b69-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b69-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-158">required</span></span>  <br/> |<span data-ttu-id="01b69-159">Значение, идентифицирующее страницу документа, к которой относится комментарий.</span><span class="sxs-lookup"><span data-stu-id="01b69-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="01b69-160">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01b69-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01b69-161">шапеид</span><span class="sxs-lookup"><span data-stu-id="01b69-161">ShapeID</span></span>  <br/> |<span data-ttu-id="01b69-162">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01b69-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01b69-163">необязательный</span><span class="sxs-lookup"><span data-stu-id="01b69-163">optional</span></span>  <br/> |<span data-ttu-id="01b69-164">Значение, определяющее фигуру, в которой находится комментарий.</span><span class="sxs-lookup"><span data-stu-id="01b69-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="01b69-165">Если Шапеид не указан, комментарий ссылается на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="01b69-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="01b69-166">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01b69-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

