---
title: EventItem_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395730"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="b06fd-102">EventItem_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b06fd-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b06fd-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b06fd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b06fd-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b06fd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b06fd-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b06fd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b06fd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b06fd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b06fd-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b06fd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b06fd-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b06fd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b06fd-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b06fd-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b06fd-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b06fd-110">Elements and attributes</span></span>

<span data-ttu-id="b06fd-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b06fd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b06fd-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b06fd-112">Child elements</span></span>

<span data-ttu-id="b06fd-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="b06fd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b06fd-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b06fd-114">Attributes</span></span>

|<span data-ttu-id="b06fd-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b06fd-115">**Attribute**</span></span>|<span data-ttu-id="b06fd-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b06fd-116">**Type**</span></span>|<span data-ttu-id="b06fd-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b06fd-117">**Required**</span></span>|<span data-ttu-id="b06fd-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b06fd-118">**Description**</span></span>|<span data-ttu-id="b06fd-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b06fd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b06fd-120">Действие</span><span class="sxs-lookup"><span data-stu-id="b06fd-120">Action</span></span>  <br/> |<span data-ttu-id="b06fd-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b06fd-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b06fd-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-122">required</span></span>  <br/> ||<span data-ttu-id="b06fd-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b06fd-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b06fd-124">Включена</span><span class="sxs-lookup"><span data-stu-id="b06fd-124">Enabled</span></span>  <br/> |<span data-ttu-id="b06fd-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="b06fd-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b06fd-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-126">optional</span></span>  <br/> ||<span data-ttu-id="b06fd-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b06fd-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b06fd-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="b06fd-128">EventCode</span></span>  <br/> |<span data-ttu-id="b06fd-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b06fd-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b06fd-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-130">required</span></span>  <br/> ||<span data-ttu-id="b06fd-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b06fd-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b06fd-132">ID</span><span class="sxs-lookup"><span data-stu-id="b06fd-132">ID</span></span>  <br/> |<span data-ttu-id="b06fd-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b06fd-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b06fd-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-134">required</span></span>  <br/> ||<span data-ttu-id="b06fd-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b06fd-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b06fd-136">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="b06fd-136">Target</span></span>  <br/> |<span data-ttu-id="b06fd-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="b06fd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="b06fd-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-138">required</span></span>  <br/> ||<span data-ttu-id="b06fd-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b06fd-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b06fd-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="b06fd-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="b06fd-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="b06fd-141">xsd:string</span></span>  <br/> |<span data-ttu-id="b06fd-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b06fd-142">required</span></span>  <br/> ||<span data-ttu-id="b06fd-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b06fd-143">Values of the xsd:string type.</span></span>  <br/> |
   

