---
title: DocumentSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396346"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="0a8e5-102">DocumentSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0a8e5-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0a8e5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0a8e5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a8e5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a8e5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a8e5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0a8e5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a8e5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a8e5-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0a8e5-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a8e5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0a8e5-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0a8e5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a8e5-110">Elements and attributes</span></span>

<span data-ttu-id="0a8e5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a8e5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0a8e5-112">Child elements</span></span>

<span data-ttu-id="0a8e5-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a8e5-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a8e5-114">Attributes</span></span>

|<span data-ttu-id="0a8e5-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-115">**Attribute**</span></span>|<span data-ttu-id="0a8e5-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-116">**Type**</span></span>|<span data-ttu-id="0a8e5-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-117">**Required**</span></span>|<span data-ttu-id="0a8e5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-118">**Description**</span></span>|<span data-ttu-id="0a8e5-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0a8e5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a8e5-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0a8e5-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="0a8e5-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0a8e5-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0a8e5-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a8e5-122">optional</span></span>  <br/> ||<span data-ttu-id="0a8e5-123">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0a8e5-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0a8e5-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0a8e5-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0a8e5-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0a8e5-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a8e5-126">optional</span></span>  <br/> ||<span data-ttu-id="0a8e5-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0a8e5-128">Имя</span><span class="sxs-lookup"><span data-stu-id="0a8e5-128">Name</span></span>  <br/> |<span data-ttu-id="0a8e5-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0a8e5-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8e5-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a8e5-130">optional</span></span>  <br/> ||<span data-ttu-id="0a8e5-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8e5-132">NameU</span><span class="sxs-lookup"><span data-stu-id="0a8e5-132">NameU</span></span>  <br/> |<span data-ttu-id="0a8e5-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0a8e5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8e5-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a8e5-134">optional</span></span>  <br/> ||<span data-ttu-id="0a8e5-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0a8e5-136">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a8e5-136">UniqueID</span></span>  <br/> |<span data-ttu-id="0a8e5-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0a8e5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0a8e5-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0a8e5-138">optional</span></span>  <br/> ||<span data-ttu-id="0a8e5-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0a8e5-139">Values of the xsd:string type.</span></span>  <br/> |
   

