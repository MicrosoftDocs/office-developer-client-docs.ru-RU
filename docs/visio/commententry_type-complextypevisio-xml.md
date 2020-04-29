---
title: CommentEntry_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540128"
---
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="0de03-102">CommentEntry_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0de03-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0de03-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0de03-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0de03-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0de03-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0de03-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0de03-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0de03-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0de03-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0de03-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0de03-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0de03-108">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0de03-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0de03-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0de03-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0de03-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0de03-110">Elements and attributes</span></span>

<span data-ttu-id="0de03-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0de03-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0de03-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0de03-112">Child elements</span></span>

<span data-ttu-id="0de03-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0de03-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0de03-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0de03-114">Attributes</span></span>

|<span data-ttu-id="0de03-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0de03-115">**Attribute**</span></span>|<span data-ttu-id="0de03-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0de03-116">**Type**</span></span>|<span data-ttu-id="0de03-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0de03-117">**Required**</span></span>|<span data-ttu-id="0de03-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0de03-118">**Description**</span></span>|<span data-ttu-id="0de03-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0de03-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0de03-120">аусорид</span><span class="sxs-lookup"><span data-stu-id="0de03-120">AuthorID</span></span>  <br/> |<span data-ttu-id="0de03-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0de03-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0de03-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-122">required</span></span>  <br/> ||<span data-ttu-id="0de03-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0de03-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0de03-124">аутокомменттипе</span><span class="sxs-lookup"><span data-stu-id="0de03-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="0de03-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0de03-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0de03-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-126">optional</span></span>  <br/> ||<span data-ttu-id="0de03-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0de03-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0de03-128">комментид</span><span class="sxs-lookup"><span data-stu-id="0de03-128">CommentID</span></span>  <br/> |<span data-ttu-id="0de03-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0de03-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0de03-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-130">required</span></span>  <br/> ||<span data-ttu-id="0de03-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0de03-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0de03-132">Дата</span><span class="sxs-lookup"><span data-stu-id="0de03-132">Date</span></span>  <br/> |<span data-ttu-id="0de03-133">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="0de03-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0de03-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-134">required</span></span>  <br/> ||<span data-ttu-id="0de03-135">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="0de03-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="0de03-136">Готово</span><span class="sxs-lookup"><span data-stu-id="0de03-136">Done</span></span>  <br/> |<span data-ttu-id="0de03-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0de03-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0de03-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-138">optional</span></span>  <br/> ||<span data-ttu-id="0de03-139">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0de03-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0de03-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="0de03-140">EditDate</span></span>  <br/> |<span data-ttu-id="0de03-141">XSD: dateTime</span><span class="sxs-lookup"><span data-stu-id="0de03-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0de03-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-142">optional</span></span>  <br/> ||<span data-ttu-id="0de03-143">Значения типа XSD: dateTime.</span><span class="sxs-lookup"><span data-stu-id="0de03-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="0de03-144">PageID</span><span class="sxs-lookup"><span data-stu-id="0de03-144">PageID</span></span>  <br/> |<span data-ttu-id="0de03-145">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0de03-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0de03-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-146">required</span></span>  <br/> ||<span data-ttu-id="0de03-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0de03-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0de03-148">шапеид</span><span class="sxs-lookup"><span data-stu-id="0de03-148">ShapeID</span></span>  <br/> |<span data-ttu-id="0de03-149">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0de03-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0de03-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="0de03-150">optional</span></span>  <br/> ||<span data-ttu-id="0de03-151">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0de03-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

