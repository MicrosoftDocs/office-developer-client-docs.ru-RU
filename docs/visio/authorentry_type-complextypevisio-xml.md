---
title: AuthorEntry_Type ComplexType (Visio XML)
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
# <a name="authorentry_type-complextype-visio-xml"></a><span data-ttu-id="b5555-102">AuthorEntry_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b5555-102">AuthorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b5555-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b5555-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5555-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b5555-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b5555-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b5555-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b5555-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b5555-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b5555-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b5555-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b5555-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b5555-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5555-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b5555-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b5555-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5555-110">Elements and attributes</span></span>

<span data-ttu-id="b5555-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b5555-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b5555-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b5555-112">Child elements</span></span>

<span data-ttu-id="b5555-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="b5555-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5555-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5555-114">Attributes</span></span>

|<span data-ttu-id="b5555-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b5555-115">**Attribute**</span></span>|<span data-ttu-id="b5555-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5555-116">**Type**</span></span>|<span data-ttu-id="b5555-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b5555-117">**Required**</span></span>|<span data-ttu-id="b5555-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5555-118">**Description**</span></span>|<span data-ttu-id="b5555-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b5555-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5555-120">ID</span><span class="sxs-lookup"><span data-stu-id="b5555-120">ID</span></span>  <br/> |<span data-ttu-id="b5555-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b5555-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5555-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5555-122">required</span></span>  <br/> ||<span data-ttu-id="b5555-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b5555-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b5555-124">Initials</span><span class="sxs-lookup"><span data-stu-id="b5555-124">Initials</span></span>  <br/> |<span data-ttu-id="b5555-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5555-125">xsd:string</span></span>  <br/> |<span data-ttu-id="b5555-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="b5555-126">optional</span></span>  <br/> ||<span data-ttu-id="b5555-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5555-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5555-128">Имя</span><span class="sxs-lookup"><span data-stu-id="b5555-128">Name</span></span>  <br/> |<span data-ttu-id="b5555-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5555-129">xsd:string</span></span>  <br/> |<span data-ttu-id="b5555-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="b5555-130">optional</span></span>  <br/> ||<span data-ttu-id="b5555-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5555-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b5555-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="b5555-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="b5555-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b5555-133">xsd:string</span></span>  <br/> |<span data-ttu-id="b5555-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="b5555-134">optional</span></span>  <br/> ||<span data-ttu-id="b5555-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b5555-135">Values of the xsd:string type.</span></span>  <br/> |
   

