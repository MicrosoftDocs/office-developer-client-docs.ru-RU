---
title: CommentEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384796"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="4b78f-102">CommentEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4b78f-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4b78f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4b78f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b78f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4b78f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4b78f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4b78f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4b78f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4b78f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4b78f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4b78f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4b78f-108">XSD:String</span><span class="sxs-lookup"><span data-stu-id="4b78f-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b78f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4b78f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4b78f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b78f-110">Elements and attributes</span></span>

<span data-ttu-id="4b78f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4b78f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4b78f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4b78f-112">Child elements</span></span>

<span data-ttu-id="4b78f-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="4b78f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b78f-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b78f-114">Attributes</span></span>

|<span data-ttu-id="4b78f-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4b78f-115">**Attribute**</span></span>|<span data-ttu-id="4b78f-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4b78f-116">**Type**</span></span>|<span data-ttu-id="4b78f-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4b78f-117">**Required**</span></span>|<span data-ttu-id="4b78f-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b78f-118">**Description**</span></span>|<span data-ttu-id="4b78f-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4b78f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b78f-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="4b78f-120">AuthorID</span></span>  <br/> |<span data-ttu-id="4b78f-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b78f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b78f-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-122">required</span></span>  <br/> ||<span data-ttu-id="4b78f-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b78f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="4b78f-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="4b78f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b78f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b78f-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-126">optional</span></span>  <br/> ||<span data-ttu-id="4b78f-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b78f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="4b78f-128">CommentID</span></span>  <br/> |<span data-ttu-id="4b78f-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b78f-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b78f-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-130">required</span></span>  <br/> ||<span data-ttu-id="4b78f-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b78f-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-132">Date</span><span class="sxs-lookup"><span data-stu-id="4b78f-132">Date</span></span>  <br/> |<span data-ttu-id="4b78f-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4b78f-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4b78f-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-134">required</span></span>  <br/> ||<span data-ttu-id="4b78f-135">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4b78f-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-136">done</span><span class="sxs-lookup"><span data-stu-id="4b78f-136">Done</span></span>  <br/> |<span data-ttu-id="4b78f-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="4b78f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4b78f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-138">optional</span></span>  <br/> ||<span data-ttu-id="4b78f-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4b78f-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="4b78f-140">EditDate</span></span>  <br/> |<span data-ttu-id="4b78f-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="4b78f-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="4b78f-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-142">optional</span></span>  <br/> ||<span data-ttu-id="4b78f-143">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="4b78f-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-144">PageID</span><span class="sxs-lookup"><span data-stu-id="4b78f-144">PageID</span></span>  <br/> |<span data-ttu-id="4b78f-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b78f-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b78f-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-146">required</span></span>  <br/> ||<span data-ttu-id="4b78f-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b78f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b78f-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="4b78f-148">ShapeID</span></span>  <br/> |<span data-ttu-id="4b78f-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b78f-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b78f-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b78f-150">optional</span></span>  <br/> ||<span data-ttu-id="4b78f-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b78f-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

