---
title: Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Задает свойства, используемые для идентификации комментария в документ.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813420"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="88b42-103">Элемент CommentEntry (CommentList_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="88b42-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="88b42-104">Задает свойства, используемые для идентификации комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="88b42-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88b42-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="88b42-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88b42-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="88b42-106">**Element type**</span></span> <br/> |[<span data-ttu-id="88b42-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="88b42-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="88b42-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="88b42-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="88b42-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="88b42-109">**Schema file**</span></span> <br/> |<span data-ttu-id="88b42-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="88b42-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="88b42-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="88b42-111">**Document parts**</span></span> <br/> |<span data-ttu-id="88b42-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="88b42-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88b42-113">Определение</span><span class="sxs-lookup"><span data-stu-id="88b42-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88b42-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="88b42-114">Elements and attributes</span></span>

<span data-ttu-id="88b42-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="88b42-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="88b42-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="88b42-116">Parent elements</span></span>

|<span data-ttu-id="88b42-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="88b42-117">**Element**</span></span>|<span data-ttu-id="88b42-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="88b42-118">**Type**</span></span>|<span data-ttu-id="88b42-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88b42-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88b42-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="88b42-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88b42-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="88b42-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88b42-122">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="88b42-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88b42-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="88b42-123">Child elements</span></span>

<span data-ttu-id="88b42-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="88b42-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88b42-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="88b42-125">Attributes</span></span>

|<span data-ttu-id="88b42-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="88b42-126">**Attribute**</span></span>|<span data-ttu-id="88b42-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="88b42-127">**Type**</span></span>|<span data-ttu-id="88b42-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="88b42-128">**Required**</span></span>|<span data-ttu-id="88b42-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88b42-129">**Description**</span></span>|<span data-ttu-id="88b42-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="88b42-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88b42-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="88b42-131">AuthorID</span></span>  <br/> |<span data-ttu-id="88b42-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b42-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b42-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-133">required</span></span>  <br/> |<span data-ttu-id="88b42-134">На основе одно значение, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="88b42-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="88b42-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b42-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88b42-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="88b42-136">CommentID</span></span>  <br/> |<span data-ttu-id="88b42-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b42-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b42-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-138">required</span></span>  <br/> |<span data-ttu-id="88b42-139">Уникальное значение, определяющее комментария в страницу документа.</span><span class="sxs-lookup"><span data-stu-id="88b42-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="88b42-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b42-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88b42-141">Date</span><span class="sxs-lookup"><span data-stu-id="88b42-141">Date</span></span>  <br/> |<span data-ttu-id="88b42-142">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="88b42-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="88b42-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-143">required</span></span>  <br/> |<span data-ttu-id="88b42-144">Указывает время создания комментария.</span><span class="sxs-lookup"><span data-stu-id="88b42-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="88b42-145">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="88b42-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="88b42-146">done</span><span class="sxs-lookup"><span data-stu-id="88b42-146">Done</span></span>  <br/> |<span data-ttu-id="88b42-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="88b42-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="88b42-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-148">optional</span></span>  <br/> |<span data-ttu-id="88b42-149">Указывает текущее состояние комментария.</span><span class="sxs-lookup"><span data-stu-id="88b42-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="88b42-150">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="88b42-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="88b42-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="88b42-151">EditDate</span></span>  <br/> |<span data-ttu-id="88b42-152">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="88b42-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="88b42-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-153">optional</span></span>  <br/> |<span data-ttu-id="88b42-154">Указывает время последнего изменения комментария.</span><span class="sxs-lookup"><span data-stu-id="88b42-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="88b42-155">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="88b42-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="88b42-156">PageID</span><span class="sxs-lookup"><span data-stu-id="88b42-156">PageID</span></span>  <br/> |<span data-ttu-id="88b42-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b42-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b42-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-158">required</span></span>  <br/> |<span data-ttu-id="88b42-159">Значение, указывающее странице документа комментарий — на.</span><span class="sxs-lookup"><span data-stu-id="88b42-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="88b42-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b42-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88b42-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="88b42-161">ShapeID</span></span>  <br/> |<span data-ttu-id="88b42-162">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88b42-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88b42-163">необязательный</span><span class="sxs-lookup"><span data-stu-id="88b42-163">optional</span></span>  <br/> |<span data-ttu-id="88b42-164">Значение, указывающее фигуры комментария включен.</span><span class="sxs-lookup"><span data-stu-id="88b42-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="88b42-165">Если не ShapeID не указан, то comment указывает на странице документа.</span><span class="sxs-lookup"><span data-stu-id="88b42-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="88b42-166">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88b42-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

