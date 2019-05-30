---
title: Коннект_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538741"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="0fc19-102">Коннект_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0fc19-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0fc19-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0fc19-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fc19-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0fc19-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0fc19-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0fc19-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0fc19-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0fc19-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0fc19-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0fc19-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0fc19-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0fc19-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0fc19-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0fc19-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0fc19-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0fc19-110">Elements and attributes</span></span>

<span data-ttu-id="0fc19-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0fc19-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0fc19-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0fc19-112">Child elements</span></span>

<span data-ttu-id="0fc19-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0fc19-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fc19-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0fc19-114">Attributes</span></span>

|<span data-ttu-id="0fc19-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0fc19-115">**Attribute**</span></span>|<span data-ttu-id="0fc19-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0fc19-116">**Type**</span></span>|<span data-ttu-id="0fc19-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0fc19-117">**Required**</span></span>|<span data-ttu-id="0fc19-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0fc19-118">**Description**</span></span>|<span data-ttu-id="0fc19-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0fc19-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0fc19-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="0fc19-120">FromCell</span></span>  <br/> |<span data-ttu-id="0fc19-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0fc19-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0fc19-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-122">optional</span></span>  <br/> ||<span data-ttu-id="0fc19-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0fc19-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0fc19-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="0fc19-124">FromPart</span></span>  <br/> |<span data-ttu-id="0fc19-125">XSD: int</span><span class="sxs-lookup"><span data-stu-id="0fc19-125">xsd:int</span></span>  <br/> |<span data-ttu-id="0fc19-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-126">optional</span></span>  <br/> ||<span data-ttu-id="0fc19-127">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="0fc19-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="0fc19-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="0fc19-128">FromSheet</span></span>  <br/> |<span data-ttu-id="0fc19-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0fc19-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0fc19-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-130">required</span></span>  <br/> ||<span data-ttu-id="0fc19-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0fc19-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0fc19-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="0fc19-132">ToCell</span></span>  <br/> |<span data-ttu-id="0fc19-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0fc19-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0fc19-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-134">optional</span></span>  <br/> ||<span data-ttu-id="0fc19-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0fc19-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0fc19-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="0fc19-136">ToPart</span></span>  <br/> |<span data-ttu-id="0fc19-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="0fc19-137">xsd:int</span></span>  <br/> |<span data-ttu-id="0fc19-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-138">optional</span></span>  <br/> ||<span data-ttu-id="0fc19-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="0fc19-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="0fc19-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="0fc19-140">ToSheet</span></span>  <br/> |<span data-ttu-id="0fc19-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0fc19-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0fc19-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0fc19-142">required</span></span>  <br/> ||<span data-ttu-id="0fc19-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0fc19-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

