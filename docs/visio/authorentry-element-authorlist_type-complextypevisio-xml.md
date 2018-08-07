---
title: Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документ.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813166"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="8e90f-103">Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="8e90f-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8e90f-104">Задает свойства, используемые для идентификации автора комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="8e90f-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e90f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8e90f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e90f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8e90f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8e90f-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="8e90f-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8e90f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8e90f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8e90f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8e90f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8e90f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8e90f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8e90f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="8e90f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8e90f-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="8e90f-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8e90f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8e90f-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8e90f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8e90f-114">Elements and attributes</span></span>

<span data-ttu-id="8e90f-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="8e90f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8e90f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8e90f-116">Parent elements</span></span>

|<span data-ttu-id="8e90f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8e90f-117">**Element**</span></span>|<span data-ttu-id="8e90f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8e90f-118">**Type**</span></span>|<span data-ttu-id="8e90f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e90f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8e90f-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="8e90f-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8e90f-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="8e90f-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8e90f-122">Задает авторы документа.</span><span class="sxs-lookup"><span data-stu-id="8e90f-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8e90f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8e90f-123">Child elements</span></span>

<span data-ttu-id="8e90f-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="8e90f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e90f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8e90f-125">Attributes</span></span>

|<span data-ttu-id="8e90f-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8e90f-126">**Attribute**</span></span>|<span data-ttu-id="8e90f-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8e90f-127">**Type**</span></span>|<span data-ttu-id="8e90f-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="8e90f-128">**Required**</span></span>|<span data-ttu-id="8e90f-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e90f-129">**Description**</span></span>|<span data-ttu-id="8e90f-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8e90f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8e90f-131">ID</span><span class="sxs-lookup"><span data-stu-id="8e90f-131">ID</span></span>  <br/> |<span data-ttu-id="8e90f-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8e90f-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8e90f-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8e90f-133">required</span></span>  <br/> |<span data-ttu-id="8e90f-134">На основе одно значение, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="8e90f-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="8e90f-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8e90f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8e90f-136">Initials</span><span class="sxs-lookup"><span data-stu-id="8e90f-136">Initials</span></span>  <br/> |<span data-ttu-id="8e90f-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8e90f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8e90f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="8e90f-138">optional</span></span>  <br/> |<span data-ttu-id="8e90f-139">Инициалы автора.</span><span class="sxs-lookup"><span data-stu-id="8e90f-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="8e90f-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8e90f-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8e90f-141">Имя</span><span class="sxs-lookup"><span data-stu-id="8e90f-141">Name</span></span>  <br/> |<span data-ttu-id="8e90f-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8e90f-142">xsd:string</span></span>  <br/> |<span data-ttu-id="8e90f-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="8e90f-143">optional</span></span>  <br/> |<span data-ttu-id="8e90f-144">Имя автора.</span><span class="sxs-lookup"><span data-stu-id="8e90f-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="8e90f-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8e90f-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8e90f-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="8e90f-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="8e90f-147">XSD:String</span><span class="sxs-lookup"><span data-stu-id="8e90f-147">xsd:string</span></span>  <br/> |<span data-ttu-id="8e90f-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="8e90f-148">optional</span></span>  <br/> |<span data-ttu-id="8e90f-149">Уникальный идентификатор автора.</span><span class="sxs-lookup"><span data-stu-id="8e90f-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="8e90f-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8e90f-150">Values of the xsd:string type.</span></span>  <br/> |
   

