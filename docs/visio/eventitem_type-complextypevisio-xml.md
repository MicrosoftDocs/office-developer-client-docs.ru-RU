---
title: EventItem_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 7fc23d9e2a9e4567693a4979b796804b16f148e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813713"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="ecdbe-102">EventItem_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ecdbe-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ecdbe-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ecdbe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ecdbe-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ecdbe-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ecdbe-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ecdbe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ecdbe-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ecdbe-108">Нет</span><span class="sxs-lookup"><span data-stu-id="ecdbe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ecdbe-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ecdbe-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ecdbe-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ecdbe-110">Elements and attributes</span></span>

<span data-ttu-id="ecdbe-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ecdbe-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ecdbe-112">Child elements</span></span>

<span data-ttu-id="ecdbe-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ecdbe-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ecdbe-114">Attributes</span></span>

|<span data-ttu-id="ecdbe-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-115">**Attribute**</span></span>|<span data-ttu-id="ecdbe-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-116">**Type**</span></span>|<span data-ttu-id="ecdbe-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-117">**Required**</span></span>|<span data-ttu-id="ecdbe-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-118">**Description**</span></span>|<span data-ttu-id="ecdbe-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ecdbe-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ecdbe-120">Действие</span><span class="sxs-lookup"><span data-stu-id="ecdbe-120">Action</span></span>  <br/> |<span data-ttu-id="ecdbe-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ecdbe-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ecdbe-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-122">required</span></span>  <br/> ||<span data-ttu-id="ecdbe-123">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ecdbe-124">Включена</span><span class="sxs-lookup"><span data-stu-id="ecdbe-124">Enabled</span></span>  <br/> |<span data-ttu-id="ecdbe-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="ecdbe-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ecdbe-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-126">optional</span></span>  <br/> ||<span data-ttu-id="ecdbe-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ecdbe-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="ecdbe-128">EventCode</span></span>  <br/> |<span data-ttu-id="ecdbe-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ecdbe-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ecdbe-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-130">required</span></span>  <br/> ||<span data-ttu-id="ecdbe-131">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ecdbe-132">ID</span><span class="sxs-lookup"><span data-stu-id="ecdbe-132">ID</span></span>  <br/> |<span data-ttu-id="ecdbe-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ecdbe-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ecdbe-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-134">required</span></span>  <br/> ||<span data-ttu-id="ecdbe-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ecdbe-136">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="ecdbe-136">Target</span></span>  <br/> |<span data-ttu-id="ecdbe-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ecdbe-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ecdbe-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-138">required</span></span>  <br/> ||<span data-ttu-id="ecdbe-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ecdbe-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="ecdbe-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="ecdbe-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ecdbe-141">xsd:string</span></span>  <br/> |<span data-ttu-id="ecdbe-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ecdbe-142">required</span></span>  <br/> ||<span data-ttu-id="ecdbe-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ecdbe-143">Values of the xsd:string type.</span></span>  <br/> |
   

