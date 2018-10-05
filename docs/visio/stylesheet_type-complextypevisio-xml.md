---
title: StyleSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396003"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="e5597-102">StyleSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e5597-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5597-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e5597-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5597-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e5597-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5597-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e5597-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5597-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e5597-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5597-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e5597-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5597-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="e5597-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5597-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e5597-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e5597-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5597-110">Elements and attributes</span></span>

<span data-ttu-id="e5597-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e5597-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5597-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e5597-112">Child elements</span></span>

<span data-ttu-id="e5597-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="e5597-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5597-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5597-114">Attributes</span></span>

|<span data-ttu-id="e5597-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e5597-115">**Attribute**</span></span>|<span data-ttu-id="e5597-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e5597-116">**Type**</span></span>|<span data-ttu-id="e5597-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e5597-117">**Required**</span></span>|<span data-ttu-id="e5597-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5597-118">**Description**</span></span>|<span data-ttu-id="e5597-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e5597-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e5597-120">ID</span><span class="sxs-lookup"><span data-stu-id="e5597-120">ID</span></span>  <br/> |<span data-ttu-id="e5597-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e5597-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e5597-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5597-122">required</span></span>  <br/> ||<span data-ttu-id="e5597-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e5597-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e5597-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="e5597-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="e5597-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="e5597-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e5597-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="e5597-126">optional</span></span>  <br/> ||<span data-ttu-id="e5597-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e5597-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e5597-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="e5597-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="e5597-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="e5597-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e5597-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="e5597-130">optional</span></span>  <br/> ||<span data-ttu-id="e5597-131">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e5597-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e5597-132">Имя</span><span class="sxs-lookup"><span data-stu-id="e5597-132">Name</span></span>  <br/> |<span data-ttu-id="e5597-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e5597-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e5597-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="e5597-134">optional</span></span>  <br/> ||<span data-ttu-id="e5597-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e5597-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5597-136">NameU</span><span class="sxs-lookup"><span data-stu-id="e5597-136">NameU</span></span>  <br/> |<span data-ttu-id="e5597-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e5597-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e5597-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e5597-138">optional</span></span>  <br/> ||<span data-ttu-id="e5597-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e5597-139">Values of the xsd:string type.</span></span>  <br/> |
   

