---
title: Документшит_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540009"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="24db9-102">Документшит_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="24db9-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="24db9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="24db9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24db9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="24db9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="24db9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="24db9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="24db9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="24db9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="24db9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="24db9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="24db9-108">Шит_типе</span><span class="sxs-lookup"><span data-stu-id="24db9-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24db9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="24db9-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="24db9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="24db9-110">Elements and attributes</span></span>

<span data-ttu-id="24db9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="24db9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="24db9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="24db9-112">Child elements</span></span>

<span data-ttu-id="24db9-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="24db9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24db9-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="24db9-114">Attributes</span></span>

|<span data-ttu-id="24db9-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="24db9-115">**Attribute**</span></span>|<span data-ttu-id="24db9-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="24db9-116">**Type**</span></span>|<span data-ttu-id="24db9-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="24db9-117">**Required**</span></span>|<span data-ttu-id="24db9-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24db9-118">**Description**</span></span>|<span data-ttu-id="24db9-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="24db9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24db9-120">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="24db9-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="24db9-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="24db9-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="24db9-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="24db9-122">optional</span></span>  <br/> ||<span data-ttu-id="24db9-123">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="24db9-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="24db9-124">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="24db9-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="24db9-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="24db9-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="24db9-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="24db9-126">optional</span></span>  <br/> ||<span data-ttu-id="24db9-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="24db9-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="24db9-128">Имя</span><span class="sxs-lookup"><span data-stu-id="24db9-128">Name</span></span>  <br/> |<span data-ttu-id="24db9-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="24db9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="24db9-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="24db9-130">optional</span></span>  <br/> ||<span data-ttu-id="24db9-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="24db9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="24db9-132">NameU</span><span class="sxs-lookup"><span data-stu-id="24db9-132">NameU</span></span>  <br/> |<span data-ttu-id="24db9-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="24db9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="24db9-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="24db9-134">optional</span></span>  <br/> ||<span data-ttu-id="24db9-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="24db9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="24db9-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="24db9-136">UniqueID</span></span>  <br/> |<span data-ttu-id="24db9-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="24db9-137">xsd:string</span></span>  <br/> |<span data-ttu-id="24db9-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="24db9-138">optional</span></span>  <br/> ||<span data-ttu-id="24db9-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="24db9-139">Values of the xsd:string type.</span></span>  <br/> |
   

