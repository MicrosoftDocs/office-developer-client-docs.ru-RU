---
title: StyleSheet_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541983"
---
# <a name="stylesheet_type-complextype-visio-xml"></a><span data-ttu-id="4f5ea-102">StyleSheet_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4f5ea-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4f5ea-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4f5ea-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f5ea-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4f5ea-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4f5ea-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4f5ea-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4f5ea-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4f5ea-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="4f5ea-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f5ea-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4f5ea-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f5ea-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f5ea-110">Elements and attributes</span></span>

<span data-ttu-id="4f5ea-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4f5ea-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4f5ea-112">Child elements</span></span>

<span data-ttu-id="4f5ea-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f5ea-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f5ea-114">Attributes</span></span>

|<span data-ttu-id="4f5ea-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-115">**Attribute**</span></span>|<span data-ttu-id="4f5ea-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-116">**Type**</span></span>|<span data-ttu-id="4f5ea-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-117">**Required**</span></span>|<span data-ttu-id="4f5ea-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-118">**Description**</span></span>|<span data-ttu-id="4f5ea-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4f5ea-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4f5ea-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="4f5ea-120">ID</span></span>  <br/> |<span data-ttu-id="4f5ea-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4f5ea-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4f5ea-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4f5ea-122">required</span></span>  <br/> ||<span data-ttu-id="4f5ea-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4f5ea-124">искустомнаме</span><span class="sxs-lookup"><span data-stu-id="4f5ea-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="4f5ea-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4f5ea-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f5ea-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f5ea-126">optional</span></span>  <br/> ||<span data-ttu-id="4f5ea-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4f5ea-128">искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="4f5ea-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="4f5ea-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4f5ea-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4f5ea-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f5ea-130">optional</span></span>  <br/> ||<span data-ttu-id="4f5ea-131">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4f5ea-132">Имя</span><span class="sxs-lookup"><span data-stu-id="4f5ea-132">Name</span></span>  <br/> |<span data-ttu-id="4f5ea-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4f5ea-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4f5ea-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f5ea-134">optional</span></span>  <br/> ||<span data-ttu-id="4f5ea-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4f5ea-136">NameU</span><span class="sxs-lookup"><span data-stu-id="4f5ea-136">NameU</span></span>  <br/> |<span data-ttu-id="4f5ea-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4f5ea-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4f5ea-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4f5ea-138">optional</span></span>  <br/> ||<span data-ttu-id="4f5ea-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4f5ea-139">Values of the xsd:string type.</span></span>  <br/> |
   

