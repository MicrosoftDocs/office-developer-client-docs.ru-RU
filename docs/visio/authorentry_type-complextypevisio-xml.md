---
title: AuthorEntry_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 41279e9f4ffa0bba17d4f74eb2f40d724589c17d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537880"
---
# <a name="authorentry_type-complextype-visio-xml"></a><span data-ttu-id="7aa63-102">AuthorEntry_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="7aa63-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7aa63-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7aa63-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7aa63-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7aa63-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7aa63-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7aa63-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7aa63-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7aa63-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7aa63-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7aa63-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7aa63-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7aa63-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7aa63-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7aa63-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7aa63-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7aa63-110">Elements and attributes</span></span>

<span data-ttu-id="7aa63-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7aa63-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7aa63-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7aa63-112">Child elements</span></span>

<span data-ttu-id="7aa63-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="7aa63-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7aa63-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7aa63-114">Attributes</span></span>

|<span data-ttu-id="7aa63-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7aa63-115">**Attribute**</span></span>|<span data-ttu-id="7aa63-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7aa63-116">**Type**</span></span>|<span data-ttu-id="7aa63-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7aa63-117">**Required**</span></span>|<span data-ttu-id="7aa63-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7aa63-118">**Description**</span></span>|<span data-ttu-id="7aa63-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7aa63-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7aa63-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7aa63-120">ID</span></span>  <br/> |<span data-ttu-id="7aa63-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="7aa63-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7aa63-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7aa63-122">required</span></span>  <br/> ||<span data-ttu-id="7aa63-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="7aa63-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7aa63-124">Инициалы</span><span class="sxs-lookup"><span data-stu-id="7aa63-124">Initials</span></span>  <br/> |<span data-ttu-id="7aa63-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7aa63-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7aa63-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="7aa63-126">optional</span></span>  <br/> ||<span data-ttu-id="7aa63-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7aa63-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7aa63-128">Имя</span><span class="sxs-lookup"><span data-stu-id="7aa63-128">Name</span></span>  <br/> |<span data-ttu-id="7aa63-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7aa63-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7aa63-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="7aa63-130">optional</span></span>  <br/> ||<span data-ttu-id="7aa63-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7aa63-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7aa63-132">ресолутионид</span><span class="sxs-lookup"><span data-stu-id="7aa63-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="7aa63-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7aa63-133">xsd:string</span></span>  <br/> |<span data-ttu-id="7aa63-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="7aa63-134">optional</span></span>  <br/> ||<span data-ttu-id="7aa63-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7aa63-135">Values of the xsd:string type.</span></span>  <br/> |
   

