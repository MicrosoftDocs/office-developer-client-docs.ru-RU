---
title: FaceName_Type complexType (Visio XML)
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
# <a name="facename_type-complextype-visio-xml"></a><span data-ttu-id="73782-102">FaceName_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="73782-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="73782-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="73782-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73782-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="73782-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="73782-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="73782-105">**Schema file**</span></span> <br/> |<span data-ttu-id="73782-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="73782-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="73782-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="73782-107">**Extension base**</span></span> <br/> |<span data-ttu-id="73782-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="73782-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73782-109">Определение</span><span class="sxs-lookup"><span data-stu-id="73782-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="73782-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="73782-110">Elements and attributes</span></span>

<span data-ttu-id="73782-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="73782-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="73782-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="73782-112">Child elements</span></span>

<span data-ttu-id="73782-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="73782-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73782-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="73782-114">Attributes</span></span>

|<span data-ttu-id="73782-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="73782-115">**Attribute**</span></span>|<span data-ttu-id="73782-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="73782-116">**Type**</span></span>|<span data-ttu-id="73782-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="73782-117">**Required**</span></span>|<span data-ttu-id="73782-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73782-118">**Description**</span></span>|<span data-ttu-id="73782-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="73782-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73782-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="73782-120">CharSets</span></span>  <br/> |<span data-ttu-id="73782-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="73782-121">xsd:string</span></span>  <br/> |<span data-ttu-id="73782-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="73782-122">optional</span></span>  <br/> ||<span data-ttu-id="73782-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="73782-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="73782-124">Flags</span><span class="sxs-lookup"><span data-stu-id="73782-124">Flags</span></span>  <br/> |<span data-ttu-id="73782-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="73782-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="73782-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="73782-126">optional</span></span>  <br/> ||<span data-ttu-id="73782-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="73782-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="73782-128">NameU</span><span class="sxs-lookup"><span data-stu-id="73782-128">NameU</span></span>  <br/> |<span data-ttu-id="73782-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="73782-129">xsd:string</span></span>  <br/> |<span data-ttu-id="73782-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="73782-130">required</span></span>  <br/> ||<span data-ttu-id="73782-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="73782-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="73782-132">Panos</span><span class="sxs-lookup"><span data-stu-id="73782-132">Panos</span></span>  <br/> |<span data-ttu-id="73782-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="73782-133">xsd:string</span></span>  <br/> |<span data-ttu-id="73782-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="73782-134">optional</span></span>  <br/> ||<span data-ttu-id="73782-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="73782-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="73782-136">Panose</span><span class="sxs-lookup"><span data-stu-id="73782-136">Panose</span></span>  <br/> |<span data-ttu-id="73782-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="73782-137">xsd:string</span></span>  <br/> |<span data-ttu-id="73782-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="73782-138">optional</span></span>  <br/> ||<span data-ttu-id="73782-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="73782-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="73782-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="73782-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="73782-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="73782-141">xsd:string</span></span>  <br/> |<span data-ttu-id="73782-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="73782-142">optional</span></span>  <br/> ||<span data-ttu-id="73782-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="73782-143">Values of the xsd:string type.</span></span>  <br/> |
   

