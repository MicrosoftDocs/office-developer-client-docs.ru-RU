---
title: Элемент Комментентри (Комментлист_типе complexType) (XML для Visio)
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
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="05c41-103">Элемент Комментентри (Комментлист_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="05c41-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="05c41-104">Задает свойства, используемые для идентификации комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="05c41-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05c41-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="05c41-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05c41-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="05c41-106">**Element type**</span></span> <br/> |[<span data-ttu-id="05c41-107">Комментентри_типе</span><span class="sxs-lookup"><span data-stu-id="05c41-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="05c41-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="05c41-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="05c41-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="05c41-109">**Schema file**</span></span> <br/> |<span data-ttu-id="05c41-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="05c41-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="05c41-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="05c41-111">**Document parts**</span></span> <br/> |<span data-ttu-id="05c41-112">Comments. XML</span><span class="sxs-lookup"><span data-stu-id="05c41-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05c41-113">Определение</span><span class="sxs-lookup"><span data-stu-id="05c41-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="05c41-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="05c41-114">Elements and attributes</span></span>

<span data-ttu-id="05c41-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="05c41-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="05c41-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="05c41-116">Parent elements</span></span>

|<span data-ttu-id="05c41-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="05c41-117">**Element**</span></span>|<span data-ttu-id="05c41-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="05c41-118">**Type**</span></span>|<span data-ttu-id="05c41-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05c41-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="05c41-120">Комментлист</span><span class="sxs-lookup"><span data-stu-id="05c41-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="05c41-121">Комментлист_типе</span><span class="sxs-lookup"><span data-stu-id="05c41-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="05c41-122">Задает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="05c41-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05c41-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="05c41-123">Child elements</span></span>

<span data-ttu-id="05c41-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="05c41-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05c41-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="05c41-125">Attributes</span></span>

|<span data-ttu-id="05c41-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="05c41-126">**Attribute**</span></span>|<span data-ttu-id="05c41-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="05c41-127">**Type**</span></span>|<span data-ttu-id="05c41-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="05c41-128">**Required**</span></span>|<span data-ttu-id="05c41-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05c41-129">**Description**</span></span>|<span data-ttu-id="05c41-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="05c41-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="05c41-131">Аусорид</span><span class="sxs-lookup"><span data-stu-id="05c41-131">AuthorID</span></span>  <br/> |<span data-ttu-id="05c41-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="05c41-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05c41-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-133">required</span></span>  <br/> |<span data-ttu-id="05c41-134">Значение с отзначением от единицы, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="05c41-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="05c41-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="05c41-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="05c41-136">Комментид</span><span class="sxs-lookup"><span data-stu-id="05c41-136">CommentID</span></span>  <br/> |<span data-ttu-id="05c41-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="05c41-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05c41-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-138">required</span></span>  <br/> |<span data-ttu-id="05c41-139">Уникальное значение, идентифицирующее комментарий на странице документа.</span><span class="sxs-lookup"><span data-stu-id="05c41-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="05c41-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="05c41-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="05c41-141">Дата</span><span class="sxs-lookup"><span data-stu-id="05c41-141">Date</span></span>  <br/> |<span data-ttu-id="05c41-142">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="05c41-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="05c41-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-143">required</span></span>  <br/> |<span data-ttu-id="05c41-144">Указывает, когда был создан комментарий.</span><span class="sxs-lookup"><span data-stu-id="05c41-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="05c41-145">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="05c41-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="05c41-146">Готово</span><span class="sxs-lookup"><span data-stu-id="05c41-146">Done</span></span>  <br/> |<span data-ttu-id="05c41-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="05c41-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="05c41-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-148">optional</span></span>  <br/> |<span data-ttu-id="05c41-149">Задает текущее состояние комментария.</span><span class="sxs-lookup"><span data-stu-id="05c41-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="05c41-150">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="05c41-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="05c41-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="05c41-151">EditDate</span></span>  <br/> |<span data-ttu-id="05c41-152">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="05c41-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="05c41-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-153">optional</span></span>  <br/> |<span data-ttu-id="05c41-154">Указывает время последнего изменения комментария.</span><span class="sxs-lookup"><span data-stu-id="05c41-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="05c41-155">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="05c41-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="05c41-156">PageID</span><span class="sxs-lookup"><span data-stu-id="05c41-156">PageID</span></span>  <br/> |<span data-ttu-id="05c41-157">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="05c41-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05c41-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-158">required</span></span>  <br/> |<span data-ttu-id="05c41-159">Значение, идентифицирующее страницу документа, к которой относится комментарий.</span><span class="sxs-lookup"><span data-stu-id="05c41-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="05c41-160">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="05c41-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="05c41-161">Шапеид</span><span class="sxs-lookup"><span data-stu-id="05c41-161">ShapeID</span></span>  <br/> |<span data-ttu-id="05c41-162">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="05c41-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05c41-163">необязательный</span><span class="sxs-lookup"><span data-stu-id="05c41-163">optional</span></span>  <br/> |<span data-ttu-id="05c41-164">Значение, определяющее фигуру, в которой находится комментарий.</span><span class="sxs-lookup"><span data-stu-id="05c41-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="05c41-165">Если Шапеид не указан, комментарий ссылается на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="05c41-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="05c41-166">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="05c41-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

