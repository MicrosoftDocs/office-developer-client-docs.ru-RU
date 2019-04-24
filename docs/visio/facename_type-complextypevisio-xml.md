---
title: Фаценаме_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322556"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="9559e-102">Фаценаме_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9559e-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9559e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9559e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9559e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9559e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9559e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9559e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9559e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9559e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9559e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9559e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9559e-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9559e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9559e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9559e-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9559e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9559e-110">Elements and attributes</span></span>

<span data-ttu-id="9559e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9559e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9559e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9559e-112">Child elements</span></span>

<span data-ttu-id="9559e-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9559e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9559e-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9559e-114">Attributes</span></span>

|<span data-ttu-id="9559e-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9559e-115">**Attribute**</span></span>|<span data-ttu-id="9559e-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9559e-116">**Type**</span></span>|<span data-ttu-id="9559e-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9559e-117">**Required**</span></span>|<span data-ttu-id="9559e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9559e-118">**Description**</span></span>|<span data-ttu-id="9559e-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9559e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9559e-120">Чарсетс</span><span class="sxs-lookup"><span data-stu-id="9559e-120">CharSets</span></span>  <br/> |<span data-ttu-id="9559e-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9559e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="9559e-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-122">optional</span></span>  <br/> ||<span data-ttu-id="9559e-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="9559e-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9559e-124">Flags</span><span class="sxs-lookup"><span data-stu-id="9559e-124">Flags</span></span>  <br/> |<span data-ttu-id="9559e-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="9559e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9559e-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-126">optional</span></span>  <br/> ||<span data-ttu-id="9559e-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="9559e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9559e-128">NameU</span><span class="sxs-lookup"><span data-stu-id="9559e-128">NameU</span></span>  <br/> |<span data-ttu-id="9559e-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9559e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9559e-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-130">required</span></span>  <br/> ||<span data-ttu-id="9559e-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="9559e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9559e-132">Панос</span><span class="sxs-lookup"><span data-stu-id="9559e-132">Panos</span></span>  <br/> |<span data-ttu-id="9559e-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9559e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="9559e-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-134">optional</span></span>  <br/> ||<span data-ttu-id="9559e-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="9559e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9559e-136">Паносе</span><span class="sxs-lookup"><span data-stu-id="9559e-136">Panose</span></span>  <br/> |<span data-ttu-id="9559e-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9559e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9559e-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-138">optional</span></span>  <br/> ||<span data-ttu-id="9559e-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="9559e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9559e-140">Уникодеранжес</span><span class="sxs-lookup"><span data-stu-id="9559e-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="9559e-141">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="9559e-141">xsd:string</span></span>  <br/> |<span data-ttu-id="9559e-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="9559e-142">optional</span></span>  <br/> ||<span data-ttu-id="9559e-143">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="9559e-143">Values of the xsd:string type.</span></span>  <br/> |
   

