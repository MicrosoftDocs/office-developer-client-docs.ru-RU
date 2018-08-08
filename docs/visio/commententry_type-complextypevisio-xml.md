---
title: CommentEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813413"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="76dc0-102">CommentEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="76dc0-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="76dc0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="76dc0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76dc0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="76dc0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="76dc0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="76dc0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="76dc0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="76dc0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="76dc0-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="76dc0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="76dc0-108">XSD:String</span><span class="sxs-lookup"><span data-stu-id="76dc0-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76dc0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="76dc0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="76dc0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="76dc0-110">Elements and attributes</span></span>

<span data-ttu-id="76dc0-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="76dc0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="76dc0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76dc0-112">Child elements</span></span>

<span data-ttu-id="76dc0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="76dc0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76dc0-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76dc0-114">Attributes</span></span>

|<span data-ttu-id="76dc0-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="76dc0-115">**Attribute**</span></span>|<span data-ttu-id="76dc0-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76dc0-116">**Type**</span></span>|<span data-ttu-id="76dc0-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="76dc0-117">**Required**</span></span>|<span data-ttu-id="76dc0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76dc0-118">**Description**</span></span>|<span data-ttu-id="76dc0-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="76dc0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="76dc0-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="76dc0-120">AuthorID</span></span>  <br/> |<span data-ttu-id="76dc0-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76dc0-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76dc0-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-122">required</span></span>  <br/> ||<span data-ttu-id="76dc0-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76dc0-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="76dc0-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="76dc0-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76dc0-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76dc0-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-126">optional</span></span>  <br/> ||<span data-ttu-id="76dc0-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76dc0-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="76dc0-128">CommentID</span></span>  <br/> |<span data-ttu-id="76dc0-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76dc0-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76dc0-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-130">required</span></span>  <br/> ||<span data-ttu-id="76dc0-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76dc0-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-132">Date</span><span class="sxs-lookup"><span data-stu-id="76dc0-132">Date</span></span>  <br/> |<span data-ttu-id="76dc0-133">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="76dc0-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="76dc0-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-134">required</span></span>  <br/> ||<span data-ttu-id="76dc0-135">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="76dc0-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-136">done</span><span class="sxs-lookup"><span data-stu-id="76dc0-136">Done</span></span>  <br/> |<span data-ttu-id="76dc0-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="76dc0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="76dc0-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-138">optional</span></span>  <br/> ||<span data-ttu-id="76dc0-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="76dc0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="76dc0-140">EditDate</span></span>  <br/> |<span data-ttu-id="76dc0-141">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="76dc0-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="76dc0-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-142">optional</span></span>  <br/> ||<span data-ttu-id="76dc0-143">Значения типа XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="76dc0-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-144">PageID</span><span class="sxs-lookup"><span data-stu-id="76dc0-144">PageID</span></span>  <br/> |<span data-ttu-id="76dc0-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76dc0-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76dc0-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-146">required</span></span>  <br/> ||<span data-ttu-id="76dc0-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76dc0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76dc0-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="76dc0-148">ShapeID</span></span>  <br/> |<span data-ttu-id="76dc0-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76dc0-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76dc0-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="76dc0-150">optional</span></span>  <br/> ||<span data-ttu-id="76dc0-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76dc0-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

