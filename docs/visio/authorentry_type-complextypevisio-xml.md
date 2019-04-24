---
title: Аусорентри_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341386"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="3926d-102">Аусорентри_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3926d-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3926d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3926d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3926d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3926d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3926d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3926d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3926d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3926d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3926d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="3926d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3926d-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="3926d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3926d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3926d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3926d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3926d-110">Elements and attributes</span></span>

<span data-ttu-id="3926d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3926d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3926d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3926d-112">Child elements</span></span>

<span data-ttu-id="3926d-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="3926d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3926d-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3926d-114">Attributes</span></span>

|<span data-ttu-id="3926d-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3926d-115">**Attribute**</span></span>|<span data-ttu-id="3926d-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3926d-116">**Type**</span></span>|<span data-ttu-id="3926d-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3926d-117">**Required**</span></span>|<span data-ttu-id="3926d-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3926d-118">**Description**</span></span>|<span data-ttu-id="3926d-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3926d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3926d-120">ИД</span><span class="sxs-lookup"><span data-stu-id="3926d-120">ID</span></span>  <br/> |<span data-ttu-id="3926d-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3926d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3926d-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3926d-122">required</span></span>  <br/> ||<span data-ttu-id="3926d-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3926d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3926d-124">Инициалы</span><span class="sxs-lookup"><span data-stu-id="3926d-124">Initials</span></span>  <br/> |<span data-ttu-id="3926d-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3926d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="3926d-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="3926d-126">optional</span></span>  <br/> ||<span data-ttu-id="3926d-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3926d-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3926d-128">Имя</span><span class="sxs-lookup"><span data-stu-id="3926d-128">Name</span></span>  <br/> |<span data-ttu-id="3926d-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3926d-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3926d-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="3926d-130">optional</span></span>  <br/> ||<span data-ttu-id="3926d-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3926d-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3926d-132">Ресолутионид</span><span class="sxs-lookup"><span data-stu-id="3926d-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="3926d-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3926d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3926d-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="3926d-134">optional</span></span>  <br/> ||<span data-ttu-id="3926d-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3926d-135">Values of the xsd:string type.</span></span>  <br/> |
   

