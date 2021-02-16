---
title: CommentEntry_Type complexType (Visio XML)
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
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="61c20-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="61c20-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="61c20-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="61c20-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61c20-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="61c20-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="61c20-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="61c20-105">**Schema file**</span></span> <br/> |<span data-ttu-id="61c20-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="61c20-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="61c20-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="61c20-107">**Extension base**</span></span> <br/> |<span data-ttu-id="61c20-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="61c20-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61c20-109">Определение</span><span class="sxs-lookup"><span data-stu-id="61c20-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="61c20-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="61c20-110">Elements and attributes</span></span>

<span data-ttu-id="61c20-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="61c20-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="61c20-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="61c20-112">Child elements</span></span>

<span data-ttu-id="61c20-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="61c20-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61c20-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="61c20-114">Attributes</span></span>

|<span data-ttu-id="61c20-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="61c20-115">**Attribute**</span></span>|<span data-ttu-id="61c20-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="61c20-116">**Type**</span></span>|<span data-ttu-id="61c20-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="61c20-117">**Required**</span></span>|<span data-ttu-id="61c20-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="61c20-118">**Description**</span></span>|<span data-ttu-id="61c20-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="61c20-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="61c20-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="61c20-120">AuthorID</span></span>  <br/> |<span data-ttu-id="61c20-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61c20-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61c20-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-122">required</span></span>  <br/> ||<span data-ttu-id="61c20-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61c20-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61c20-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="61c20-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="61c20-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61c20-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61c20-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-126">optional</span></span>  <br/> ||<span data-ttu-id="61c20-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61c20-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61c20-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="61c20-128">CommentID</span></span>  <br/> |<span data-ttu-id="61c20-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61c20-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61c20-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-130">required</span></span>  <br/> ||<span data-ttu-id="61c20-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61c20-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61c20-132">Дата</span><span class="sxs-lookup"><span data-stu-id="61c20-132">Date</span></span>  <br/> |<span data-ttu-id="61c20-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="61c20-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="61c20-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-134">required</span></span>  <br/> ||<span data-ttu-id="61c20-135">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="61c20-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="61c20-136">Готово</span><span class="sxs-lookup"><span data-stu-id="61c20-136">Done</span></span>  <br/> |<span data-ttu-id="61c20-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="61c20-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="61c20-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-138">optional</span></span>  <br/> ||<span data-ttu-id="61c20-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="61c20-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="61c20-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="61c20-140">EditDate</span></span>  <br/> |<span data-ttu-id="61c20-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="61c20-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="61c20-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-142">optional</span></span>  <br/> ||<span data-ttu-id="61c20-143">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="61c20-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="61c20-144">PageID</span><span class="sxs-lookup"><span data-stu-id="61c20-144">PageID</span></span>  <br/> |<span data-ttu-id="61c20-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61c20-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61c20-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-146">required</span></span>  <br/> ||<span data-ttu-id="61c20-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61c20-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="61c20-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="61c20-148">ShapeID</span></span>  <br/> |<span data-ttu-id="61c20-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="61c20-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="61c20-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="61c20-150">optional</span></span>  <br/> ||<span data-ttu-id="61c20-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="61c20-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

