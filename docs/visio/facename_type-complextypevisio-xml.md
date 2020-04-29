---
title: FaceName_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542900"
---
# <a name="facename_type-complextype-visio-xml"></a><span data-ttu-id="4c0a4-102">FaceName_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4c0a4-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4c0a4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4c0a4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c0a4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4c0a4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4c0a4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4c0a4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4c0a4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4c0a4-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4c0a4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c0a4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4c0a4-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c0a4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c0a4-110">Elements and attributes</span></span>

<span data-ttu-id="4c0a4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4c0a4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4c0a4-112">Child elements</span></span>

<span data-ttu-id="4c0a4-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c0a4-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c0a4-114">Attributes</span></span>

|<span data-ttu-id="4c0a4-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-115">**Attribute**</span></span>|<span data-ttu-id="4c0a4-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-116">**Type**</span></span>|<span data-ttu-id="4c0a4-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-117">**Required**</span></span>|<span data-ttu-id="4c0a4-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-118">**Description**</span></span>|<span data-ttu-id="4c0a4-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4c0a4-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4c0a4-120">чарсетс</span><span class="sxs-lookup"><span data-stu-id="4c0a4-120">CharSets</span></span>  <br/> |<span data-ttu-id="4c0a4-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4c0a4-121">xsd:string</span></span>  <br/> |<span data-ttu-id="4c0a4-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-122">optional</span></span>  <br/> ||<span data-ttu-id="4c0a4-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4c0a4-124">Flags</span><span class="sxs-lookup"><span data-stu-id="4c0a4-124">Flags</span></span>  <br/> |<span data-ttu-id="4c0a4-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4c0a4-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4c0a4-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-126">optional</span></span>  <br/> ||<span data-ttu-id="4c0a4-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4c0a4-128">NameU</span><span class="sxs-lookup"><span data-stu-id="4c0a4-128">NameU</span></span>  <br/> |<span data-ttu-id="4c0a4-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4c0a4-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4c0a4-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-130">required</span></span>  <br/> ||<span data-ttu-id="4c0a4-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4c0a4-132">панос</span><span class="sxs-lookup"><span data-stu-id="4c0a4-132">Panos</span></span>  <br/> |<span data-ttu-id="4c0a4-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4c0a4-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4c0a4-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-134">optional</span></span>  <br/> ||<span data-ttu-id="4c0a4-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4c0a4-136">паносе</span><span class="sxs-lookup"><span data-stu-id="4c0a4-136">Panose</span></span>  <br/> |<span data-ttu-id="4c0a4-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4c0a4-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4c0a4-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-138">optional</span></span>  <br/> ||<span data-ttu-id="4c0a4-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4c0a4-140">уникодеранжес</span><span class="sxs-lookup"><span data-stu-id="4c0a4-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="4c0a4-141">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4c0a4-141">xsd:string</span></span>  <br/> |<span data-ttu-id="4c0a4-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="4c0a4-142">optional</span></span>  <br/> ||<span data-ttu-id="4c0a4-143">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4c0a4-143">Values of the xsd:string type.</span></span>  <br/> |
   

