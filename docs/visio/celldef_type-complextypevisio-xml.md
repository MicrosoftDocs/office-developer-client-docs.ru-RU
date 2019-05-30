---
title: Целлдеф_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542298"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="8d3ac-102">Целлдеф_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8d3ac-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8d3ac-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8d3ac-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d3ac-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8d3ac-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8d3ac-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8d3ac-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8d3ac-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8d3ac-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8d3ac-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8d3ac-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8d3ac-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8d3ac-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8d3ac-110">Elements and attributes</span></span>

<span data-ttu-id="8d3ac-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8d3ac-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8d3ac-112">Child elements</span></span>

<span data-ttu-id="8d3ac-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d3ac-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8d3ac-114">Attributes</span></span>

|<span data-ttu-id="8d3ac-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-115">**Attribute**</span></span>|<span data-ttu-id="8d3ac-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-116">**Type**</span></span>|<span data-ttu-id="8d3ac-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-117">**Required**</span></span>|<span data-ttu-id="8d3ac-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-118">**Description**</span></span>|<span data-ttu-id="8d3ac-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8d3ac-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8d3ac-120">F</span><span class="sxs-lookup"><span data-stu-id="8d3ac-120">F</span></span>  <br/> |<span data-ttu-id="8d3ac-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8d3ac-121">xsd:string</span></span>  <br/> |<span data-ttu-id="8d3ac-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="8d3ac-122">optional</span></span>  <br/> ||<span data-ttu-id="8d3ac-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d3ac-124">IX</span><span class="sxs-lookup"><span data-stu-id="8d3ac-124">IX</span></span>  <br/> |<span data-ttu-id="8d3ac-125">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8d3ac-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8d3ac-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="8d3ac-126">optional</span></span>  <br/> ||<span data-ttu-id="8d3ac-127">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8d3ac-128">N</span><span class="sxs-lookup"><span data-stu-id="8d3ac-128">N</span></span>  <br/> |<span data-ttu-id="8d3ac-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8d3ac-129">xsd:string</span></span>  <br/> |<span data-ttu-id="8d3ac-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d3ac-130">required</span></span>  <br/> ||<span data-ttu-id="8d3ac-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8d3ac-132">S</span><span class="sxs-lookup"><span data-stu-id="8d3ac-132">S</span></span>  <br/> |<span data-ttu-id="8d3ac-133">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8d3ac-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8d3ac-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="8d3ac-134">optional</span></span>  <br/> ||<span data-ttu-id="8d3ac-135">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8d3ac-136">Д</span><span class="sxs-lookup"><span data-stu-id="8d3ac-136">T</span></span>  <br/> |<span data-ttu-id="8d3ac-137">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="8d3ac-137">xsd:token</span></span>  <br/> |<span data-ttu-id="8d3ac-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8d3ac-138">required</span></span>  <br/> ||<span data-ttu-id="8d3ac-139">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="8d3ac-139">Values of the xsd:token type.</span></span>  <br/> |
   

