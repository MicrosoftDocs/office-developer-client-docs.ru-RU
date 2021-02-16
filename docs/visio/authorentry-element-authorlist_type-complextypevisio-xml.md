---
title: Элемент AuthorEntry (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Указывает свойства, используемые для идентификации автора комментария в документе.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537908"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a><span data-ttu-id="6b25d-103">Элемент AuthorEntry (AuthorList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6b25d-103">AuthorEntry element (AuthorList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6b25d-104">Указывает свойства, используемые для идентификации автора комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="6b25d-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b25d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b25d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b25d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6b25d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b25d-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="6b25d-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b25d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b25d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b25d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b25d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b25d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6b25d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b25d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6b25d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b25d-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="6b25d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b25d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6b25d-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b25d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b25d-114">Elements and attributes</span></span>

<span data-ttu-id="6b25d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b25d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b25d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6b25d-116">Parent elements</span></span>

|<span data-ttu-id="6b25d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b25d-117">**Element**</span></span>|<span data-ttu-id="6b25d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b25d-118">**Type**</span></span>|<span data-ttu-id="6b25d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b25d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b25d-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="6b25d-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b25d-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="6b25d-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b25d-122">Указывает авторов в документе.</span><span class="sxs-lookup"><span data-stu-id="6b25d-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b25d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b25d-123">Child elements</span></span>

<span data-ttu-id="6b25d-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b25d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b25d-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b25d-125">Attributes</span></span>

|<span data-ttu-id="6b25d-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6b25d-126">**Attribute**</span></span>|<span data-ttu-id="6b25d-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b25d-127">**Type**</span></span>|<span data-ttu-id="6b25d-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6b25d-128">**Required**</span></span>|<span data-ttu-id="6b25d-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b25d-129">**Description**</span></span>|<span data-ttu-id="6b25d-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6b25d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b25d-131">ID</span><span class="sxs-lookup"><span data-stu-id="6b25d-131">ID</span></span>  <br/> |<span data-ttu-id="6b25d-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6b25d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b25d-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b25d-133">required</span></span>  <br/> |<span data-ttu-id="6b25d-134">Одно основанное на значении, идентифицирует автора.</span><span class="sxs-lookup"><span data-stu-id="6b25d-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="6b25d-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6b25d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b25d-136">Initials</span><span class="sxs-lookup"><span data-stu-id="6b25d-136">Initials</span></span>  <br/> |<span data-ttu-id="6b25d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b25d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6b25d-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b25d-138">optional</span></span>  <br/> |<span data-ttu-id="6b25d-139">Инициалы автора.</span><span class="sxs-lookup"><span data-stu-id="6b25d-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="6b25d-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6b25d-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b25d-141">Имя</span><span class="sxs-lookup"><span data-stu-id="6b25d-141">Name</span></span>  <br/> |<span data-ttu-id="6b25d-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b25d-142">xsd:string</span></span>  <br/> |<span data-ttu-id="6b25d-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b25d-143">optional</span></span>  <br/> |<span data-ttu-id="6b25d-144">Имя автора.</span><span class="sxs-lookup"><span data-stu-id="6b25d-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="6b25d-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6b25d-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b25d-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="6b25d-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="6b25d-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b25d-147">xsd:string</span></span>  <br/> |<span data-ttu-id="6b25d-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b25d-148">optional</span></span>  <br/> |<span data-ttu-id="6b25d-149">Уникальный идентификатор автора.</span><span class="sxs-lookup"><span data-stu-id="6b25d-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="6b25d-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6b25d-150">Values of the xsd:string type.</span></span>  <br/> |
   

