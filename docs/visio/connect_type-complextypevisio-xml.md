---
title: Коннект_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327085"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="3c190-102">Коннект_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3c190-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3c190-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3c190-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c190-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3c190-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3c190-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3c190-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3c190-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3c190-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3c190-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="3c190-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3c190-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="3c190-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c190-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3c190-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3c190-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c190-110">Elements and attributes</span></span>

<span data-ttu-id="3c190-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3c190-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3c190-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3c190-112">Child elements</span></span>

<span data-ttu-id="3c190-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="3c190-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c190-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c190-114">Attributes</span></span>

|<span data-ttu-id="3c190-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3c190-115">**Attribute**</span></span>|<span data-ttu-id="3c190-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c190-116">**Type**</span></span>|<span data-ttu-id="3c190-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3c190-117">**Required**</span></span>|<span data-ttu-id="3c190-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c190-118">**Description**</span></span>|<span data-ttu-id="3c190-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3c190-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c190-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="3c190-120">FromCell</span></span>  <br/> |<span data-ttu-id="3c190-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3c190-121">xsd:string</span></span>  <br/> |<span data-ttu-id="3c190-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-122">optional</span></span>  <br/> ||<span data-ttu-id="3c190-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3c190-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c190-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="3c190-124">FromPart</span></span>  <br/> |<span data-ttu-id="3c190-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="3c190-125">xsd:int</span></span>  <br/> |<span data-ttu-id="3c190-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-126">optional</span></span>  <br/> ||<span data-ttu-id="3c190-127">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="3c190-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3c190-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="3c190-128">FromSheet</span></span>  <br/> |<span data-ttu-id="3c190-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3c190-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c190-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-130">required</span></span>  <br/> ||<span data-ttu-id="3c190-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3c190-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c190-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="3c190-132">ToCell</span></span>  <br/> |<span data-ttu-id="3c190-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3c190-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3c190-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-134">optional</span></span>  <br/> ||<span data-ttu-id="3c190-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3c190-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c190-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="3c190-136">ToPart</span></span>  <br/> |<span data-ttu-id="3c190-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="3c190-137">xsd:int</span></span>  <br/> |<span data-ttu-id="3c190-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-138">optional</span></span>  <br/> ||<span data-ttu-id="3c190-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="3c190-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="3c190-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="3c190-140">ToSheet</span></span>  <br/> |<span data-ttu-id="3c190-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3c190-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c190-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c190-142">required</span></span>  <br/> ||<span data-ttu-id="3c190-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3c190-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

