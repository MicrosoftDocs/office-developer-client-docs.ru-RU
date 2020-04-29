---
title: EventItem_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541794"
---
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="ec091-102">EventItem_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="ec091-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ec091-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ec091-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec091-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ec091-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec091-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ec091-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec091-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec091-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec091-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ec091-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec091-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ec091-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec091-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ec091-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec091-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec091-110">Elements and attributes</span></span>

<span data-ttu-id="ec091-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ec091-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec091-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec091-112">Child elements</span></span>

<span data-ttu-id="ec091-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="ec091-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec091-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec091-114">Attributes</span></span>

|<span data-ttu-id="ec091-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ec091-115">**Attribute**</span></span>|<span data-ttu-id="ec091-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec091-116">**Type**</span></span>|<span data-ttu-id="ec091-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ec091-117">**Required**</span></span>|<span data-ttu-id="ec091-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec091-118">**Description**</span></span>|<span data-ttu-id="ec091-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ec091-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec091-120">Action</span><span class="sxs-lookup"><span data-stu-id="ec091-120">Action</span></span>  <br/> |<span data-ttu-id="ec091-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ec091-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ec091-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-122">required</span></span>  <br/> ||<span data-ttu-id="ec091-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ec091-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ec091-124">Включен</span><span class="sxs-lookup"><span data-stu-id="ec091-124">Enabled</span></span>  <br/> |<span data-ttu-id="ec091-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec091-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec091-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-126">optional</span></span>  <br/> ||<span data-ttu-id="ec091-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec091-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec091-128">евенткоде</span><span class="sxs-lookup"><span data-stu-id="ec091-128">EventCode</span></span>  <br/> |<span data-ttu-id="ec091-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ec091-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ec091-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-130">required</span></span>  <br/> ||<span data-ttu-id="ec091-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ec091-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ec091-132">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ec091-132">ID</span></span>  <br/> |<span data-ttu-id="ec091-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec091-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec091-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-134">required</span></span>  <br/> ||<span data-ttu-id="ec091-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec091-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec091-136">Target</span><span class="sxs-lookup"><span data-stu-id="ec091-136">Target</span></span>  <br/> |<span data-ttu-id="ec091-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec091-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ec091-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-138">required</span></span>  <br/> ||<span data-ttu-id="ec091-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec091-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec091-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="ec091-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="ec091-141">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec091-141">xsd:string</span></span>  <br/> |<span data-ttu-id="ec091-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec091-142">required</span></span>  <br/> ||<span data-ttu-id="ec091-143">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec091-143">Values of the xsd:string type.</span></span>  <br/> |
   

