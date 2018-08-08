---
title: Connect_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9a321a3ff910afb183e1a697eaad9dfb51125524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813457"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="9a59a-102">Connect_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9a59a-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9a59a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9a59a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a59a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9a59a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a59a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9a59a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a59a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a59a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a59a-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="9a59a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a59a-108">Нет</span><span class="sxs-lookup"><span data-stu-id="9a59a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a59a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9a59a-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a59a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a59a-110">Elements and attributes</span></span>

<span data-ttu-id="9a59a-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="9a59a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a59a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a59a-112">Child elements</span></span>

<span data-ttu-id="9a59a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9a59a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a59a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a59a-114">Attributes</span></span>

|<span data-ttu-id="9a59a-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9a59a-115">**Attribute**</span></span>|<span data-ttu-id="9a59a-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9a59a-116">**Type**</span></span>|<span data-ttu-id="9a59a-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="9a59a-117">**Required**</span></span>|<span data-ttu-id="9a59a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9a59a-118">**Description**</span></span>|<span data-ttu-id="9a59a-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9a59a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a59a-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="9a59a-120">FromCell</span></span>  <br/> |<span data-ttu-id="9a59a-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="9a59a-121">xsd:string</span></span>  <br/> |<span data-ttu-id="9a59a-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-122">optional</span></span>  <br/> ||<span data-ttu-id="9a59a-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a59a-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a59a-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="9a59a-124">FromPart</span></span>  <br/> |<span data-ttu-id="9a59a-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="9a59a-125">xsd:int</span></span>  <br/> |<span data-ttu-id="9a59a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-126">optional</span></span>  <br/> ||<span data-ttu-id="9a59a-127">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="9a59a-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="9a59a-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="9a59a-128">FromSheet</span></span>  <br/> |<span data-ttu-id="9a59a-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a59a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a59a-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-130">required</span></span>  <br/> ||<span data-ttu-id="9a59a-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a59a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a59a-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="9a59a-132">ToCell</span></span>  <br/> |<span data-ttu-id="9a59a-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="9a59a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9a59a-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-134">optional</span></span>  <br/> ||<span data-ttu-id="9a59a-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a59a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a59a-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="9a59a-136">ToPart</span></span>  <br/> |<span data-ttu-id="9a59a-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="9a59a-137">xsd:int</span></span>  <br/> |<span data-ttu-id="9a59a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-138">optional</span></span>  <br/> ||<span data-ttu-id="9a59a-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="9a59a-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="9a59a-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="9a59a-140">ToSheet</span></span>  <br/> |<span data-ttu-id="9a59a-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a59a-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a59a-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a59a-142">required</span></span>  <br/> ||<span data-ttu-id="9a59a-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a59a-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

