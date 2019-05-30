---
title: Стилешит_типе complexType (XML для Visio)
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
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="35019-102">Стилешит_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="35019-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="35019-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="35019-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35019-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="35019-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="35019-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="35019-105">**Schema file**</span></span> <br/> |<span data-ttu-id="35019-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="35019-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="35019-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="35019-107">**Extension base**</span></span> <br/> |<span data-ttu-id="35019-108">Шит_типе</span><span class="sxs-lookup"><span data-stu-id="35019-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35019-109">Определение</span><span class="sxs-lookup"><span data-stu-id="35019-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="35019-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="35019-110">Elements and attributes</span></span>

<span data-ttu-id="35019-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="35019-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="35019-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="35019-112">Child elements</span></span>

<span data-ttu-id="35019-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="35019-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35019-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="35019-114">Attributes</span></span>

|<span data-ttu-id="35019-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="35019-115">**Attribute**</span></span>|<span data-ttu-id="35019-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35019-116">**Type**</span></span>|<span data-ttu-id="35019-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="35019-117">**Required**</span></span>|<span data-ttu-id="35019-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35019-118">**Description**</span></span>|<span data-ttu-id="35019-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="35019-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35019-120">ID</span><span class="sxs-lookup"><span data-stu-id="35019-120">ID</span></span>  <br/> |<span data-ttu-id="35019-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="35019-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="35019-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35019-122">required</span></span>  <br/> ||<span data-ttu-id="35019-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="35019-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="35019-124">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="35019-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="35019-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="35019-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="35019-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="35019-126">optional</span></span>  <br/> ||<span data-ttu-id="35019-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="35019-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="35019-128">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="35019-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="35019-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="35019-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="35019-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="35019-130">optional</span></span>  <br/> ||<span data-ttu-id="35019-131">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="35019-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="35019-132">Имя</span><span class="sxs-lookup"><span data-stu-id="35019-132">Name</span></span>  <br/> |<span data-ttu-id="35019-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="35019-133">xsd:string</span></span>  <br/> |<span data-ttu-id="35019-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="35019-134">optional</span></span>  <br/> ||<span data-ttu-id="35019-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="35019-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35019-136">NameU</span><span class="sxs-lookup"><span data-stu-id="35019-136">NameU</span></span>  <br/> |<span data-ttu-id="35019-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="35019-137">xsd:string</span></span>  <br/> |<span data-ttu-id="35019-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="35019-138">optional</span></span>  <br/> ||<span data-ttu-id="35019-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="35019-139">Values of the xsd:string type.</span></span>  <br/> |
   

