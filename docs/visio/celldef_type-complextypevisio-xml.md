---
title: CellDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399986"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="1ad99-102">CellDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1ad99-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ad99-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1ad99-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad99-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1ad99-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ad99-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1ad99-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ad99-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ad99-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ad99-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1ad99-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ad99-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1ad99-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ad99-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1ad99-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ad99-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ad99-110">Elements and attributes</span></span>

<span data-ttu-id="1ad99-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1ad99-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ad99-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1ad99-112">Child elements</span></span>

<span data-ttu-id="1ad99-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="1ad99-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ad99-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ad99-114">Attributes</span></span>

|<span data-ttu-id="1ad99-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1ad99-115">**Attribute**</span></span>|<span data-ttu-id="1ad99-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1ad99-116">**Type**</span></span>|<span data-ttu-id="1ad99-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1ad99-117">**Required**</span></span>|<span data-ttu-id="1ad99-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ad99-118">**Description**</span></span>|<span data-ttu-id="1ad99-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1ad99-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ad99-120">F</span><span class="sxs-lookup"><span data-stu-id="1ad99-120">F</span></span>  <br/> |<span data-ttu-id="1ad99-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ad99-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1ad99-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ad99-122">optional</span></span>  <br/> ||<span data-ttu-id="1ad99-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ad99-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ad99-124">IX</span><span class="sxs-lookup"><span data-stu-id="1ad99-124">IX</span></span>  <br/> |<span data-ttu-id="1ad99-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1ad99-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1ad99-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ad99-126">optional</span></span>  <br/> ||<span data-ttu-id="1ad99-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="1ad99-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1ad99-128">N</span><span class="sxs-lookup"><span data-stu-id="1ad99-128">N</span></span>  <br/> |<span data-ttu-id="1ad99-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ad99-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1ad99-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ad99-130">required</span></span>  <br/> ||<span data-ttu-id="1ad99-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ad99-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ad99-132">s</span><span class="sxs-lookup"><span data-stu-id="1ad99-132">S</span></span>  <br/> |<span data-ttu-id="1ad99-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="1ad99-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1ad99-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ad99-134">optional</span></span>  <br/> ||<span data-ttu-id="1ad99-135">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="1ad99-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1ad99-136">T</span><span class="sxs-lookup"><span data-stu-id="1ad99-136">T</span></span>  <br/> |<span data-ttu-id="1ad99-137">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="1ad99-137">xsd:token</span></span>  <br/> |<span data-ttu-id="1ad99-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ad99-138">required</span></span>  <br/> ||<span data-ttu-id="1ad99-139">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="1ad99-139">Values of the xsd:token type.</span></span>  <br/> |
   

