---
title: CellDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 6471158df8c89e8d7b0202f9bdbce196e24b93b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813354"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="9469a-102">CellDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9469a-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9469a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9469a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9469a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9469a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9469a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9469a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9469a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9469a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9469a-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="9469a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9469a-108">Нет</span><span class="sxs-lookup"><span data-stu-id="9469a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9469a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9469a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9469a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9469a-110">Elements and attributes</span></span>

<span data-ttu-id="9469a-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="9469a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9469a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9469a-112">Child elements</span></span>

<span data-ttu-id="9469a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9469a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9469a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9469a-114">Attributes</span></span>

|<span data-ttu-id="9469a-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9469a-115">**Attribute**</span></span>|<span data-ttu-id="9469a-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9469a-116">**Type**</span></span>|<span data-ttu-id="9469a-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="9469a-117">**Required**</span></span>|<span data-ttu-id="9469a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9469a-118">**Description**</span></span>|<span data-ttu-id="9469a-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9469a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9469a-120">F</span><span class="sxs-lookup"><span data-stu-id="9469a-120">F</span></span>  <br/> |<span data-ttu-id="9469a-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="9469a-121">xsd:string</span></span>  <br/> |<span data-ttu-id="9469a-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="9469a-122">optional</span></span>  <br/> ||<span data-ttu-id="9469a-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9469a-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9469a-124">IX</span><span class="sxs-lookup"><span data-stu-id="9469a-124">IX</span></span>  <br/> |<span data-ttu-id="9469a-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="9469a-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="9469a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="9469a-126">optional</span></span>  <br/> ||<span data-ttu-id="9469a-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="9469a-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="9469a-128">N</span><span class="sxs-lookup"><span data-stu-id="9469a-128">N</span></span>  <br/> |<span data-ttu-id="9469a-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="9469a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9469a-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9469a-130">required</span></span>  <br/> ||<span data-ttu-id="9469a-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9469a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9469a-132">s</span><span class="sxs-lookup"><span data-stu-id="9469a-132">S</span></span>  <br/> |<span data-ttu-id="9469a-133">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="9469a-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="9469a-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="9469a-134">optional</span></span>  <br/> ||<span data-ttu-id="9469a-135">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="9469a-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="9469a-136">T</span><span class="sxs-lookup"><span data-stu-id="9469a-136">T</span></span>  <br/> |<span data-ttu-id="9469a-137">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="9469a-137">xsd:token</span></span>  <br/> |<span data-ttu-id="9469a-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9469a-138">required</span></span>  <br/> ||<span data-ttu-id="9469a-139">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="9469a-139">Values of the xsd:token type.</span></span>  <br/> |
   

