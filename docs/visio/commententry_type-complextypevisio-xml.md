---
title: CommentEntry_Type ComplexType (Visio XML)
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
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="667c5-102">CommentEntry_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="667c5-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="667c5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="667c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="667c5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="667c5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="667c5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="667c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="667c5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="667c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="667c5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="667c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="667c5-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="667c5-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="667c5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="667c5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="667c5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="667c5-110">Elements and attributes</span></span>

<span data-ttu-id="667c5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="667c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="667c5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="667c5-112">Child elements</span></span>

<span data-ttu-id="667c5-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="667c5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="667c5-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="667c5-114">Attributes</span></span>

|<span data-ttu-id="667c5-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="667c5-115">**Attribute**</span></span>|<span data-ttu-id="667c5-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="667c5-116">**Type**</span></span>|<span data-ttu-id="667c5-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="667c5-117">**Required**</span></span>|<span data-ttu-id="667c5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="667c5-118">**Description**</span></span>|<span data-ttu-id="667c5-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="667c5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="667c5-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="667c5-120">AuthorID</span></span>  <br/> |<span data-ttu-id="667c5-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="667c5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="667c5-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-122">required</span></span>  <br/> ||<span data-ttu-id="667c5-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="667c5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="667c5-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="667c5-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="667c5-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="667c5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="667c5-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-126">optional</span></span>  <br/> ||<span data-ttu-id="667c5-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="667c5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="667c5-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="667c5-128">CommentID</span></span>  <br/> |<span data-ttu-id="667c5-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="667c5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="667c5-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-130">required</span></span>  <br/> ||<span data-ttu-id="667c5-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="667c5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="667c5-132">Date</span><span class="sxs-lookup"><span data-stu-id="667c5-132">Date</span></span>  <br/> |<span data-ttu-id="667c5-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="667c5-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="667c5-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-134">required</span></span>  <br/> ||<span data-ttu-id="667c5-135">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="667c5-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="667c5-136">Готово</span><span class="sxs-lookup"><span data-stu-id="667c5-136">Done</span></span>  <br/> |<span data-ttu-id="667c5-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="667c5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="667c5-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-138">optional</span></span>  <br/> ||<span data-ttu-id="667c5-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="667c5-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="667c5-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="667c5-140">EditDate</span></span>  <br/> |<span data-ttu-id="667c5-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="667c5-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="667c5-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-142">optional</span></span>  <br/> ||<span data-ttu-id="667c5-143">Значения типа xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="667c5-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="667c5-144">PageID</span><span class="sxs-lookup"><span data-stu-id="667c5-144">PageID</span></span>  <br/> |<span data-ttu-id="667c5-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="667c5-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="667c5-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-146">required</span></span>  <br/> ||<span data-ttu-id="667c5-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="667c5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="667c5-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="667c5-148">ShapeID</span></span>  <br/> |<span data-ttu-id="667c5-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="667c5-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="667c5-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="667c5-150">optional</span></span>  <br/> ||<span data-ttu-id="667c5-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="667c5-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

