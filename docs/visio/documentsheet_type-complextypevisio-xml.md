---
title: DocumentSheet_Type ComplexType (Visio XML)
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
# <a name="documentsheet_type-complextype-visio-xml"></a><span data-ttu-id="82c44-102">DocumentSheet_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="82c44-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="82c44-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="82c44-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82c44-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="82c44-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="82c44-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="82c44-105">**Schema file**</span></span> <br/> |<span data-ttu-id="82c44-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="82c44-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="82c44-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="82c44-107">**Extension base**</span></span> <br/> |<span data-ttu-id="82c44-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="82c44-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="82c44-109">Определение</span><span class="sxs-lookup"><span data-stu-id="82c44-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="82c44-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="82c44-110">Elements and attributes</span></span>

<span data-ttu-id="82c44-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="82c44-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="82c44-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82c44-112">Child elements</span></span>

<span data-ttu-id="82c44-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="82c44-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82c44-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="82c44-114">Attributes</span></span>

|<span data-ttu-id="82c44-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="82c44-115">**Attribute**</span></span>|<span data-ttu-id="82c44-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="82c44-116">**Type**</span></span>|<span data-ttu-id="82c44-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="82c44-117">**Required**</span></span>|<span data-ttu-id="82c44-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="82c44-118">**Description**</span></span>|<span data-ttu-id="82c44-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="82c44-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="82c44-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="82c44-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="82c44-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="82c44-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="82c44-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="82c44-122">optional</span></span>  <br/> ||<span data-ttu-id="82c44-123">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="82c44-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="82c44-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="82c44-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="82c44-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="82c44-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="82c44-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="82c44-126">optional</span></span>  <br/> ||<span data-ttu-id="82c44-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="82c44-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="82c44-128">Имя</span><span class="sxs-lookup"><span data-stu-id="82c44-128">Name</span></span>  <br/> |<span data-ttu-id="82c44-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="82c44-129">xsd:string</span></span>  <br/> |<span data-ttu-id="82c44-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="82c44-130">optional</span></span>  <br/> ||<span data-ttu-id="82c44-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="82c44-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="82c44-132">NameU</span><span class="sxs-lookup"><span data-stu-id="82c44-132">NameU</span></span>  <br/> |<span data-ttu-id="82c44-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="82c44-133">xsd:string</span></span>  <br/> |<span data-ttu-id="82c44-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="82c44-134">optional</span></span>  <br/> ||<span data-ttu-id="82c44-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="82c44-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="82c44-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="82c44-136">UniqueID</span></span>  <br/> |<span data-ttu-id="82c44-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="82c44-137">xsd:string</span></span>  <br/> |<span data-ttu-id="82c44-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="82c44-138">optional</span></span>  <br/> ||<span data-ttu-id="82c44-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="82c44-139">Values of the xsd:string type.</span></span>  <br/> |
   

