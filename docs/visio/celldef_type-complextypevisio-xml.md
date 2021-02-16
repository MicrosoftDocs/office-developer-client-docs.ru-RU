---
title: CellDef_Type complexType (Visio XML)
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
# <a name="celldef_type-complextype-visio-xml"></a><span data-ttu-id="6b936-102">CellDef_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6b936-102">CellDef_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6b936-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6b936-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b936-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b936-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6b936-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b936-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6b936-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6b936-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6b936-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6b936-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6b936-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="6b936-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b936-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6b936-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6b936-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b936-110">Elements and attributes</span></span>

<span data-ttu-id="6b936-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b936-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6b936-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b936-112">Child elements</span></span>

<span data-ttu-id="6b936-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b936-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b936-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b936-114">Attributes</span></span>

|<span data-ttu-id="6b936-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6b936-115">**Attribute**</span></span>|<span data-ttu-id="6b936-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b936-116">**Type**</span></span>|<span data-ttu-id="6b936-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6b936-117">**Required**</span></span>|<span data-ttu-id="6b936-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b936-118">**Description**</span></span>|<span data-ttu-id="6b936-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6b936-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b936-120">F</span><span class="sxs-lookup"><span data-stu-id="6b936-120">F</span></span>  <br/> |<span data-ttu-id="6b936-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b936-121">xsd:string</span></span>  <br/> |<span data-ttu-id="6b936-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b936-122">optional</span></span>  <br/> ||<span data-ttu-id="6b936-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6b936-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b936-124">IX</span><span class="sxs-lookup"><span data-stu-id="6b936-124">IX</span></span>  <br/> |<span data-ttu-id="6b936-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6b936-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="6b936-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b936-126">optional</span></span>  <br/> ||<span data-ttu-id="6b936-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="6b936-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="6b936-128">N</span><span class="sxs-lookup"><span data-stu-id="6b936-128">N</span></span>  <br/> |<span data-ttu-id="6b936-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b936-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6b936-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b936-130">required</span></span>  <br/> ||<span data-ttu-id="6b936-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6b936-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b936-132">S</span><span class="sxs-lookup"><span data-stu-id="6b936-132">S</span></span>  <br/> |<span data-ttu-id="6b936-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6b936-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="6b936-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b936-134">optional</span></span>  <br/> ||<span data-ttu-id="6b936-135">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="6b936-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="6b936-136">T</span><span class="sxs-lookup"><span data-stu-id="6b936-136">T</span></span>  <br/> |<span data-ttu-id="6b936-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6b936-137">xsd:token</span></span>  <br/> |<span data-ttu-id="6b936-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b936-138">required</span></span>  <br/> ||<span data-ttu-id="6b936-139">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="6b936-139">Values of the xsd:token type.</span></span>  <br/> |
   

