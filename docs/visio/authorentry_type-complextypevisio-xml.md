---
title: AuthorEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386840"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="4a989-102">AuthorEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4a989-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4a989-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4a989-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a989-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4a989-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4a989-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4a989-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4a989-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4a989-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4a989-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4a989-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4a989-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4a989-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4a989-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4a989-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4a989-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4a989-110">Elements and attributes</span></span>

<span data-ttu-id="4a989-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4a989-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4a989-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4a989-112">Child elements</span></span>

<span data-ttu-id="4a989-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="4a989-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a989-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4a989-114">Attributes</span></span>

|<span data-ttu-id="4a989-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4a989-115">**Attribute**</span></span>|<span data-ttu-id="4a989-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4a989-116">**Type**</span></span>|<span data-ttu-id="4a989-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4a989-117">**Required**</span></span>|<span data-ttu-id="4a989-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a989-118">**Description**</span></span>|<span data-ttu-id="4a989-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4a989-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4a989-120">ID</span><span class="sxs-lookup"><span data-stu-id="4a989-120">ID</span></span>  <br/> |<span data-ttu-id="4a989-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4a989-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4a989-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4a989-122">required</span></span>  <br/> ||<span data-ttu-id="4a989-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4a989-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4a989-124">Initials</span><span class="sxs-lookup"><span data-stu-id="4a989-124">Initials</span></span>  <br/> |<span data-ttu-id="4a989-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="4a989-125">xsd:string</span></span>  <br/> |<span data-ttu-id="4a989-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="4a989-126">optional</span></span>  <br/> ||<span data-ttu-id="4a989-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4a989-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4a989-128">Имя</span><span class="sxs-lookup"><span data-stu-id="4a989-128">Name</span></span>  <br/> |<span data-ttu-id="4a989-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="4a989-129">xsd:string</span></span>  <br/> |<span data-ttu-id="4a989-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="4a989-130">optional</span></span>  <br/> ||<span data-ttu-id="4a989-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4a989-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4a989-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="4a989-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="4a989-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="4a989-133">xsd:string</span></span>  <br/> |<span data-ttu-id="4a989-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="4a989-134">optional</span></span>  <br/> ||<span data-ttu-id="4a989-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4a989-135">Values of the xsd:string type.</span></span>  <br/> |
   

