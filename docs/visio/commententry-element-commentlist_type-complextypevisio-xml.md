---
title: Элемент CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Указывает свойства, используемые для идентификации комментария на рисунке.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540114"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="245c9-103">Элемент CommentEntry (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="245c9-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="245c9-104">Указывает свойства, используемые для идентификации комментария на рисунке.</span><span class="sxs-lookup"><span data-stu-id="245c9-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="245c9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="245c9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="245c9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="245c9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="245c9-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="245c9-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="245c9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="245c9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="245c9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="245c9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="245c9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="245c9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="245c9-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="245c9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="245c9-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="245c9-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="245c9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="245c9-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="245c9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="245c9-114">Elements and attributes</span></span>

<span data-ttu-id="245c9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="245c9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="245c9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="245c9-116">Parent elements</span></span>

|<span data-ttu-id="245c9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="245c9-117">**Element**</span></span>|<span data-ttu-id="245c9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="245c9-118">**Type**</span></span>|<span data-ttu-id="245c9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="245c9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="245c9-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="245c9-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="245c9-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="245c9-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="245c9-122">Указывает комментарии на рисунке.</span><span class="sxs-lookup"><span data-stu-id="245c9-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="245c9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="245c9-123">Child elements</span></span>

<span data-ttu-id="245c9-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="245c9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="245c9-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="245c9-125">Attributes</span></span>

|<span data-ttu-id="245c9-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="245c9-126">**Attribute**</span></span>|<span data-ttu-id="245c9-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="245c9-127">**Type**</span></span>|<span data-ttu-id="245c9-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="245c9-128">**Required**</span></span>|<span data-ttu-id="245c9-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="245c9-129">**Description**</span></span>|<span data-ttu-id="245c9-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="245c9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="245c9-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="245c9-131">AuthorID</span></span>  <br/> |<span data-ttu-id="245c9-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="245c9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="245c9-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-133">required</span></span>  <br/> |<span data-ttu-id="245c9-134">Одно основанное значение, которое идентифицирует автора.</span><span class="sxs-lookup"><span data-stu-id="245c9-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="245c9-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="245c9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="245c9-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="245c9-136">CommentID</span></span>  <br/> |<span data-ttu-id="245c9-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="245c9-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="245c9-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-138">required</span></span>  <br/> |<span data-ttu-id="245c9-139">Уникальное значение, идентифицирует комментарий на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="245c9-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="245c9-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="245c9-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="245c9-141">Date</span><span class="sxs-lookup"><span data-stu-id="245c9-141">Date</span></span>  <br/> |<span data-ttu-id="245c9-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="245c9-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="245c9-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-143">required</span></span>  <br/> |<span data-ttu-id="245c9-144">Указывает, когда был создан комментарий.</span><span class="sxs-lookup"><span data-stu-id="245c9-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="245c9-145">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="245c9-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="245c9-146">Готово</span><span class="sxs-lookup"><span data-stu-id="245c9-146">Done</span></span>  <br/> |<span data-ttu-id="245c9-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="245c9-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="245c9-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-148">optional</span></span>  <br/> |<span data-ttu-id="245c9-149">Указывает текущее состояние комментария.</span><span class="sxs-lookup"><span data-stu-id="245c9-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="245c9-150">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="245c9-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="245c9-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="245c9-151">EditDate</span></span>  <br/> |<span data-ttu-id="245c9-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="245c9-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="245c9-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-153">optional</span></span>  <br/> |<span data-ttu-id="245c9-154">Указывает, когда комментарий был изменен в последний раз.</span><span class="sxs-lookup"><span data-stu-id="245c9-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="245c9-155">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="245c9-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="245c9-156">PageID</span><span class="sxs-lookup"><span data-stu-id="245c9-156">PageID</span></span>  <br/> |<span data-ttu-id="245c9-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="245c9-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="245c9-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-158">required</span></span>  <br/> |<span data-ttu-id="245c9-159">Значение, которое определяет страницу рисования, на которую указан комментарий.</span><span class="sxs-lookup"><span data-stu-id="245c9-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="245c9-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="245c9-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="245c9-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="245c9-161">ShapeID</span></span>  <br/> |<span data-ttu-id="245c9-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="245c9-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="245c9-163">необязательный</span><span class="sxs-lookup"><span data-stu-id="245c9-163">optional</span></span>  <br/> |<span data-ttu-id="245c9-164">Значение, определяее форму, в которую указан комментарий.</span><span class="sxs-lookup"><span data-stu-id="245c9-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="245c9-165">Если не указан ShapeID, комментарий относится к странице рисования.</span><span class="sxs-lookup"><span data-stu-id="245c9-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="245c9-166">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="245c9-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

