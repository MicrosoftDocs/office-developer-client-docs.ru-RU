---
title: Элемент Аусорентри (Аусорлист_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Задает свойства, используемые для идентификации автора комментария в документе.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338628"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="a8595-103">Элемент Аусорентри (Аусорлист_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a8595-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a8595-104">Задает свойства, используемые для идентификации автора комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="a8595-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8595-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a8595-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8595-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a8595-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8595-107">Аусорентри_типе</span><span class="sxs-lookup"><span data-stu-id="a8595-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8595-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a8595-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8595-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a8595-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8595-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a8595-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8595-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="a8595-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8595-112">Comments. XML</span><span class="sxs-lookup"><span data-stu-id="a8595-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8595-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a8595-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8595-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a8595-114">Elements and attributes</span></span>

<span data-ttu-id="a8595-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a8595-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8595-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a8595-116">Parent elements</span></span>

|<span data-ttu-id="a8595-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a8595-117">**Element**</span></span>|<span data-ttu-id="a8595-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a8595-118">**Type**</span></span>|<span data-ttu-id="a8595-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8595-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8595-120">Аусорлист</span><span class="sxs-lookup"><span data-stu-id="a8595-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8595-121">Аусорлист_типе</span><span class="sxs-lookup"><span data-stu-id="a8595-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8595-122">Указывает авторов в документе.</span><span class="sxs-lookup"><span data-stu-id="a8595-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a8595-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a8595-123">Child elements</span></span>

<span data-ttu-id="a8595-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="a8595-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8595-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a8595-125">Attributes</span></span>

|<span data-ttu-id="a8595-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a8595-126">**Attribute**</span></span>|<span data-ttu-id="a8595-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a8595-127">**Type**</span></span>|<span data-ttu-id="a8595-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a8595-128">**Required**</span></span>|<span data-ttu-id="a8595-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a8595-129">**Description**</span></span>|<span data-ttu-id="a8595-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a8595-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8595-131">ИД</span><span class="sxs-lookup"><span data-stu-id="a8595-131">ID</span></span>  <br/> |<span data-ttu-id="a8595-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a8595-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a8595-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a8595-133">required</span></span>  <br/> |<span data-ttu-id="a8595-134">Значение с отзначением от единицы, идентифицирующее автора.</span><span class="sxs-lookup"><span data-stu-id="a8595-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="a8595-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a8595-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a8595-136">Инициалы</span><span class="sxs-lookup"><span data-stu-id="a8595-136">Initials</span></span>  <br/> |<span data-ttu-id="a8595-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a8595-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a8595-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="a8595-138">optional</span></span>  <br/> |<span data-ttu-id="a8595-139">Инициалы автора.</span><span class="sxs-lookup"><span data-stu-id="a8595-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="a8595-140">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a8595-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8595-141">Имя</span><span class="sxs-lookup"><span data-stu-id="a8595-141">Name</span></span>  <br/> |<span data-ttu-id="a8595-142">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a8595-142">xsd:string</span></span>  <br/> |<span data-ttu-id="a8595-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="a8595-143">optional</span></span>  <br/> |<span data-ttu-id="a8595-144">Имя автора.</span><span class="sxs-lookup"><span data-stu-id="a8595-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="a8595-145">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a8595-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a8595-146">Ресолутионид</span><span class="sxs-lookup"><span data-stu-id="a8595-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="a8595-147">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a8595-147">xsd:string</span></span>  <br/> |<span data-ttu-id="a8595-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="a8595-148">optional</span></span>  <br/> |<span data-ttu-id="a8595-149">Уникальный идентификатор автора.</span><span class="sxs-lookup"><span data-stu-id="a8595-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="a8595-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a8595-150">Values of the xsd:string type.</span></span>  <br/> |
   

