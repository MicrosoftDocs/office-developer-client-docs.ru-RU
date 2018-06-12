---
title: StyleSheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814975"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="0e6fd-102">StyleSheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0e6fd-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0e6fd-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0e6fd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e6fd-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e6fd-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e6fd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0e6fd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e6fd-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e6fd-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0e6fd-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e6fd-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0e6fd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0e6fd-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0e6fd-110">Elements and attributes</span></span>

<span data-ttu-id="0e6fd-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e6fd-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0e6fd-112">Child elements</span></span>

<span data-ttu-id="0e6fd-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e6fd-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0e6fd-114">Attributes</span></span>

|<span data-ttu-id="0e6fd-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-115">**Attribute**</span></span>|<span data-ttu-id="0e6fd-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-116">**Type**</span></span>|<span data-ttu-id="0e6fd-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-117">**Required**</span></span>|<span data-ttu-id="0e6fd-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-118">**Description**</span></span>|<span data-ttu-id="0e6fd-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0e6fd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e6fd-120">ID</span><span class="sxs-lookup"><span data-stu-id="0e6fd-120">ID</span></span>  <br/> |<span data-ttu-id="0e6fd-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0e6fd-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e6fd-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0e6fd-122">required</span></span>  <br/> ||<span data-ttu-id="0e6fd-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e6fd-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0e6fd-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="0e6fd-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0e6fd-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e6fd-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="0e6fd-126">optional</span></span>  <br/> ||<span data-ttu-id="0e6fd-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e6fd-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0e6fd-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0e6fd-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0e6fd-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e6fd-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="0e6fd-130">optional</span></span>  <br/> ||<span data-ttu-id="0e6fd-131">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e6fd-132">Имя</span><span class="sxs-lookup"><span data-stu-id="0e6fd-132">Name</span></span>  <br/> |<span data-ttu-id="0e6fd-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0e6fd-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0e6fd-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="0e6fd-134">optional</span></span>  <br/> ||<span data-ttu-id="0e6fd-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e6fd-136">NameU</span><span class="sxs-lookup"><span data-stu-id="0e6fd-136">NameU</span></span>  <br/> |<span data-ttu-id="0e6fd-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0e6fd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0e6fd-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0e6fd-138">optional</span></span>  <br/> ||<span data-ttu-id="0e6fd-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0e6fd-139">Values of the xsd:string type.</span></span>  <br/> |
   

