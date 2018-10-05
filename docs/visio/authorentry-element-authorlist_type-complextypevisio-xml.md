---
title: Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документ.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386335"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="3e35c-103">Элемент AuthorEntry (AuthorList_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3e35c-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3e35c-104">Задает свойства, используемые для идентификации автора комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="3e35c-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e35c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3e35c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e35c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3e35c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3e35c-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3e35c-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3e35c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3e35c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3e35c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3e35c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3e35c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3e35c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3e35c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3e35c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3e35c-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="3e35c-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e35c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3e35c-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3e35c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3e35c-114">Elements and attributes</span></span>

<span data-ttu-id="3e35c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3e35c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3e35c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3e35c-116">Parent elements</span></span>

|<span data-ttu-id="3e35c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3e35c-117">**Element**</span></span>|<span data-ttu-id="3e35c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3e35c-118">**Type**</span></span>|<span data-ttu-id="3e35c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e35c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e35c-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="3e35c-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3e35c-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="3e35c-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3e35c-122">Задает авторы документа.</span><span class="sxs-lookup"><span data-stu-id="3e35c-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3e35c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3e35c-123">Child elements</span></span>

<span data-ttu-id="3e35c-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="3e35c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e35c-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3e35c-125">Attributes</span></span>

|<span data-ttu-id="3e35c-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3e35c-126">**Attribute**</span></span>|<span data-ttu-id="3e35c-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3e35c-127">**Type**</span></span>|<span data-ttu-id="3e35c-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3e35c-128">**Required**</span></span>|<span data-ttu-id="3e35c-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e35c-129">**Description**</span></span>|<span data-ttu-id="3e35c-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3e35c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3e35c-131">ID</span><span class="sxs-lookup"><span data-stu-id="3e35c-131">ID</span></span>  <br/> |<span data-ttu-id="3e35c-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3e35c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3e35c-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3e35c-133">required</span></span>  <br/> |<span data-ttu-id="3e35c-134">На основе одно значение, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="3e35c-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="3e35c-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3e35c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3e35c-136">Initials</span><span class="sxs-lookup"><span data-stu-id="3e35c-136">Initials</span></span>  <br/> |<span data-ttu-id="3e35c-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3e35c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3e35c-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="3e35c-138">optional</span></span>  <br/> |<span data-ttu-id="3e35c-139">Инициалы автора.</span><span class="sxs-lookup"><span data-stu-id="3e35c-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="3e35c-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e35c-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e35c-141">Имя</span><span class="sxs-lookup"><span data-stu-id="3e35c-141">Name</span></span>  <br/> |<span data-ttu-id="3e35c-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3e35c-142">xsd:string</span></span>  <br/> |<span data-ttu-id="3e35c-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="3e35c-143">optional</span></span>  <br/> |<span data-ttu-id="3e35c-144">Имя автора.</span><span class="sxs-lookup"><span data-stu-id="3e35c-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="3e35c-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e35c-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e35c-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="3e35c-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="3e35c-147">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3e35c-147">xsd:string</span></span>  <br/> |<span data-ttu-id="3e35c-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="3e35c-148">optional</span></span>  <br/> |<span data-ttu-id="3e35c-149">Уникальный идентификатор автора.</span><span class="sxs-lookup"><span data-stu-id="3e35c-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="3e35c-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e35c-150">Values of the xsd:string type.</span></span>  <br/> |
   

