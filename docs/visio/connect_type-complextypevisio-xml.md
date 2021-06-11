---
title: Connect_Type ComplexType (Visio XML)
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
# <a name="connect_type-complextype-visio-xml"></a><span data-ttu-id="784c7-102">Connect_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="784c7-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="784c7-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="784c7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="784c7-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="784c7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="784c7-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="784c7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="784c7-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="784c7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="784c7-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="784c7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="784c7-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="784c7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="784c7-109">Определение</span><span class="sxs-lookup"><span data-stu-id="784c7-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="784c7-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="784c7-110">Elements and attributes</span></span>

<span data-ttu-id="784c7-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="784c7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="784c7-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="784c7-112">Child elements</span></span>

<span data-ttu-id="784c7-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="784c7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="784c7-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="784c7-114">Attributes</span></span>

|<span data-ttu-id="784c7-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="784c7-115">**Attribute**</span></span>|<span data-ttu-id="784c7-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="784c7-116">**Type**</span></span>|<span data-ttu-id="784c7-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="784c7-117">**Required**</span></span>|<span data-ttu-id="784c7-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="784c7-118">**Description**</span></span>|<span data-ttu-id="784c7-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="784c7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="784c7-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="784c7-120">FromCell</span></span>  <br/> |<span data-ttu-id="784c7-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="784c7-121">xsd:string</span></span>  <br/> |<span data-ttu-id="784c7-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-122">optional</span></span>  <br/> ||<span data-ttu-id="784c7-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="784c7-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c7-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="784c7-124">FromPart</span></span>  <br/> |<span data-ttu-id="784c7-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="784c7-125">xsd:int</span></span>  <br/> |<span data-ttu-id="784c7-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-126">optional</span></span>  <br/> ||<span data-ttu-id="784c7-127">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="784c7-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="784c7-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="784c7-128">FromSheet</span></span>  <br/> |<span data-ttu-id="784c7-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="784c7-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="784c7-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-130">required</span></span>  <br/> ||<span data-ttu-id="784c7-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="784c7-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="784c7-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="784c7-132">ToCell</span></span>  <br/> |<span data-ttu-id="784c7-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="784c7-133">xsd:string</span></span>  <br/> |<span data-ttu-id="784c7-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-134">optional</span></span>  <br/> ||<span data-ttu-id="784c7-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="784c7-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c7-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="784c7-136">ToPart</span></span>  <br/> |<span data-ttu-id="784c7-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="784c7-137">xsd:int</span></span>  <br/> |<span data-ttu-id="784c7-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-138">optional</span></span>  <br/> ||<span data-ttu-id="784c7-139">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="784c7-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="784c7-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="784c7-140">ToSheet</span></span>  <br/> |<span data-ttu-id="784c7-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="784c7-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="784c7-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="784c7-142">required</span></span>  <br/> ||<span data-ttu-id="784c7-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="784c7-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

