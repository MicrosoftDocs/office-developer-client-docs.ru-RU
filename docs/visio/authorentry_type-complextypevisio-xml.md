---
title: AuthorEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813150"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="bbd7a-102">AuthorEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bbd7a-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bbd7a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bbd7a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbd7a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bbd7a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bbd7a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bbd7a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bbd7a-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bbd7a-108">Нет</span><span class="sxs-lookup"><span data-stu-id="bbd7a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bbd7a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bbd7a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bbd7a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bbd7a-110">Elements and attributes</span></span>

<span data-ttu-id="bbd7a-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bbd7a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bbd7a-112">Child elements</span></span>

<span data-ttu-id="bbd7a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bbd7a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bbd7a-114">Attributes</span></span>

|<span data-ttu-id="bbd7a-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-115">**Attribute**</span></span>|<span data-ttu-id="bbd7a-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-116">**Type**</span></span>|<span data-ttu-id="bbd7a-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-117">**Required**</span></span>|<span data-ttu-id="bbd7a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-118">**Description**</span></span>|<span data-ttu-id="bbd7a-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bbd7a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bbd7a-120">ID</span><span class="sxs-lookup"><span data-stu-id="bbd7a-120">ID</span></span>  <br/> |<span data-ttu-id="bbd7a-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bbd7a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bbd7a-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bbd7a-122">required</span></span>  <br/> ||<span data-ttu-id="bbd7a-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bbd7a-124">Initials</span><span class="sxs-lookup"><span data-stu-id="bbd7a-124">Initials</span></span>  <br/> |<span data-ttu-id="bbd7a-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bbd7a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bbd7a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="bbd7a-126">optional</span></span>  <br/> ||<span data-ttu-id="bbd7a-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bbd7a-128">Имя</span><span class="sxs-lookup"><span data-stu-id="bbd7a-128">Name</span></span>  <br/> |<span data-ttu-id="bbd7a-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bbd7a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="bbd7a-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="bbd7a-130">optional</span></span>  <br/> ||<span data-ttu-id="bbd7a-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bbd7a-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="bbd7a-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="bbd7a-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bbd7a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="bbd7a-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="bbd7a-134">optional</span></span>  <br/> ||<span data-ttu-id="bbd7a-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bbd7a-135">Values of the xsd:string type.</span></span>  <br/> |
   

