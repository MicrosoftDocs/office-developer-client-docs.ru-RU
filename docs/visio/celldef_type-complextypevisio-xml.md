---
title: Целлдеф_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327127"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="57704-102">Целлдеф_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="57704-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="57704-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="57704-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57704-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="57704-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57704-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="57704-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57704-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="57704-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57704-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="57704-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57704-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="57704-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57704-109">Определение</span><span class="sxs-lookup"><span data-stu-id="57704-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="57704-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="57704-110">Elements and attributes</span></span>

<span data-ttu-id="57704-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="57704-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57704-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="57704-112">Child elements</span></span>

<span data-ttu-id="57704-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="57704-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57704-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="57704-114">Attributes</span></span>

|<span data-ttu-id="57704-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="57704-115">**Attribute**</span></span>|<span data-ttu-id="57704-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="57704-116">**Type**</span></span>|<span data-ttu-id="57704-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="57704-117">**Required**</span></span>|<span data-ttu-id="57704-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="57704-118">**Description**</span></span>|<span data-ttu-id="57704-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="57704-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="57704-120">F</span><span class="sxs-lookup"><span data-stu-id="57704-120">F</span></span>  <br/> |<span data-ttu-id="57704-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="57704-121">xsd:string</span></span>  <br/> |<span data-ttu-id="57704-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="57704-122">optional</span></span>  <br/> ||<span data-ttu-id="57704-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="57704-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="57704-124">IX</span><span class="sxs-lookup"><span data-stu-id="57704-124">IX</span></span>  <br/> |<span data-ttu-id="57704-125">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="57704-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="57704-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="57704-126">optional</span></span>  <br/> ||<span data-ttu-id="57704-127">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="57704-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="57704-128">N</span><span class="sxs-lookup"><span data-stu-id="57704-128">N</span></span>  <br/> |<span data-ttu-id="57704-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="57704-129">xsd:string</span></span>  <br/> |<span data-ttu-id="57704-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="57704-130">required</span></span>  <br/> ||<span data-ttu-id="57704-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="57704-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="57704-132">S</span><span class="sxs-lookup"><span data-stu-id="57704-132">S</span></span>  <br/> |<span data-ttu-id="57704-133">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="57704-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="57704-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="57704-134">optional</span></span>  <br/> ||<span data-ttu-id="57704-135">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="57704-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="57704-136">Д</span><span class="sxs-lookup"><span data-stu-id="57704-136">T</span></span>  <br/> |<span data-ttu-id="57704-137">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="57704-137">xsd:token</span></span>  <br/> |<span data-ttu-id="57704-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="57704-138">required</span></span>  <br/> ||<span data-ttu-id="57704-139">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="57704-139">Values of the xsd:token type.</span></span>  <br/> |
   

