---
title: StyleSheet_Type Type (Visio XML)
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
# <a name="stylesheet_type-complextype-visio-xml"></a><span data-ttu-id="0c90a-102">StyleSheet_Type Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0c90a-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0c90a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0c90a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c90a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0c90a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c90a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0c90a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c90a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c90a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c90a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0c90a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c90a-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0c90a-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c90a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0c90a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c90a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c90a-110">Elements and attributes</span></span>

<span data-ttu-id="0c90a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0c90a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c90a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0c90a-112">Child elements</span></span>

<span data-ttu-id="0c90a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0c90a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c90a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c90a-114">Attributes</span></span>

|<span data-ttu-id="0c90a-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0c90a-115">**Attribute**</span></span>|<span data-ttu-id="0c90a-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0c90a-116">**Type**</span></span>|<span data-ttu-id="0c90a-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0c90a-117">**Required**</span></span>|<span data-ttu-id="0c90a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c90a-118">**Description**</span></span>|<span data-ttu-id="0c90a-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0c90a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c90a-120">ID</span><span class="sxs-lookup"><span data-stu-id="0c90a-120">ID</span></span>  <br/> |<span data-ttu-id="0c90a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c90a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c90a-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c90a-122">required</span></span>  <br/> ||<span data-ttu-id="0c90a-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0c90a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c90a-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0c90a-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="0c90a-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0c90a-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c90a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="0c90a-126">optional</span></span>  <br/> ||<span data-ttu-id="0c90a-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0c90a-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c90a-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0c90a-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0c90a-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0c90a-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c90a-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="0c90a-130">optional</span></span>  <br/> ||<span data-ttu-id="0c90a-131">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0c90a-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c90a-132">Имя</span><span class="sxs-lookup"><span data-stu-id="0c90a-132">Name</span></span>  <br/> |<span data-ttu-id="0c90a-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0c90a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0c90a-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="0c90a-134">optional</span></span>  <br/> ||<span data-ttu-id="0c90a-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0c90a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c90a-136">NameU</span><span class="sxs-lookup"><span data-stu-id="0c90a-136">NameU</span></span>  <br/> |<span data-ttu-id="0c90a-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0c90a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0c90a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0c90a-138">optional</span></span>  <br/> ||<span data-ttu-id="0c90a-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0c90a-139">Values of the xsd:string type.</span></span>  <br/> |
   

