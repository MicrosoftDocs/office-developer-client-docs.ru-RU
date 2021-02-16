---
title: Элемент CommentEntry (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Указывает свойства, используемые для идентификации комментария в документе.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540114"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="efc70-103">Элемент CommentEntry (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="efc70-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="efc70-104">Указывает свойства, используемые для идентификации комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="efc70-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efc70-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="efc70-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efc70-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="efc70-106">**Element type**</span></span> <br/> |[<span data-ttu-id="efc70-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="efc70-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="efc70-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="efc70-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="efc70-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="efc70-109">**Schema file**</span></span> <br/> |<span data-ttu-id="efc70-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="efc70-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="efc70-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="efc70-111">**Document parts**</span></span> <br/> |<span data-ttu-id="efc70-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="efc70-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efc70-113">Определение</span><span class="sxs-lookup"><span data-stu-id="efc70-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="efc70-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="efc70-114">Elements and attributes</span></span>

<span data-ttu-id="efc70-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="efc70-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="efc70-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="efc70-116">Parent elements</span></span>

|<span data-ttu-id="efc70-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="efc70-117">**Element**</span></span>|<span data-ttu-id="efc70-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="efc70-118">**Type**</span></span>|<span data-ttu-id="efc70-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="efc70-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efc70-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="efc70-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efc70-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="efc70-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="efc70-122">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="efc70-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="efc70-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="efc70-123">Child elements</span></span>

<span data-ttu-id="efc70-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="efc70-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efc70-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="efc70-125">Attributes</span></span>

|<span data-ttu-id="efc70-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="efc70-126">**Attribute**</span></span>|<span data-ttu-id="efc70-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="efc70-127">**Type**</span></span>|<span data-ttu-id="efc70-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="efc70-128">**Required**</span></span>|<span data-ttu-id="efc70-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="efc70-129">**Description**</span></span>|<span data-ttu-id="efc70-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="efc70-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efc70-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="efc70-131">AuthorID</span></span>  <br/> |<span data-ttu-id="efc70-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efc70-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efc70-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-133">required</span></span>  <br/> |<span data-ttu-id="efc70-134">Одно основанное на значении, идентифицирует автора.</span><span class="sxs-lookup"><span data-stu-id="efc70-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="efc70-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efc70-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efc70-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="efc70-136">CommentID</span></span>  <br/> |<span data-ttu-id="efc70-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efc70-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efc70-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-138">required</span></span>  <br/> |<span data-ttu-id="efc70-139">Уникальное значение, идентифицирует комментарий на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="efc70-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="efc70-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efc70-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efc70-141">Дата</span><span class="sxs-lookup"><span data-stu-id="efc70-141">Date</span></span>  <br/> |<span data-ttu-id="efc70-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="efc70-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="efc70-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-143">required</span></span>  <br/> |<span data-ttu-id="efc70-144">Указывает, когда был создан комментарий.</span><span class="sxs-lookup"><span data-stu-id="efc70-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="efc70-145">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="efc70-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="efc70-146">Готово</span><span class="sxs-lookup"><span data-stu-id="efc70-146">Done</span></span>  <br/> |<span data-ttu-id="efc70-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="efc70-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="efc70-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-148">optional</span></span>  <br/> |<span data-ttu-id="efc70-149">Указывает текущее состояние комментария.</span><span class="sxs-lookup"><span data-stu-id="efc70-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="efc70-150">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="efc70-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="efc70-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="efc70-151">EditDate</span></span>  <br/> |<span data-ttu-id="efc70-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="efc70-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="efc70-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-153">optional</span></span>  <br/> |<span data-ttu-id="efc70-154">Указывает время последнего изменения комментария.</span><span class="sxs-lookup"><span data-stu-id="efc70-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="efc70-155">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="efc70-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="efc70-156">PageID</span><span class="sxs-lookup"><span data-stu-id="efc70-156">PageID</span></span>  <br/> |<span data-ttu-id="efc70-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efc70-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efc70-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-158">required</span></span>  <br/> |<span data-ttu-id="efc70-159">Значение, определяя страницу рисования, на которую указывает комментарий.</span><span class="sxs-lookup"><span data-stu-id="efc70-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="efc70-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efc70-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="efc70-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="efc70-161">ShapeID</span></span>  <br/> |<span data-ttu-id="efc70-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="efc70-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="efc70-163">необязательный</span><span class="sxs-lookup"><span data-stu-id="efc70-163">optional</span></span>  <br/> |<span data-ttu-id="efc70-164">Значение, определяя фигуру, в которую добавлен комментарий.</span><span class="sxs-lookup"><span data-stu-id="efc70-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="efc70-165">Если shapeID не указан, комментарий ссылается на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="efc70-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="efc70-166">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="efc70-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

