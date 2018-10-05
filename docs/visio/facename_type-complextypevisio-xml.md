---
title: FaceName_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382444"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="7cf4f-102">FaceName_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7cf4f-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7cf4f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7cf4f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cf4f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7cf4f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7cf4f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7cf4f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7cf4f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7cf4f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7cf4f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cf4f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7cf4f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7cf4f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cf4f-110">Elements and attributes</span></span>

<span data-ttu-id="7cf4f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7cf4f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7cf4f-112">Child elements</span></span>

<span data-ttu-id="7cf4f-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cf4f-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cf4f-114">Attributes</span></span>

|<span data-ttu-id="7cf4f-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-115">**Attribute**</span></span>|<span data-ttu-id="7cf4f-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-116">**Type**</span></span>|<span data-ttu-id="7cf4f-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-117">**Required**</span></span>|<span data-ttu-id="7cf4f-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-118">**Description**</span></span>|<span data-ttu-id="7cf4f-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7cf4f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7cf4f-120">Наборов символов</span><span class="sxs-lookup"><span data-stu-id="7cf4f-120">CharSets</span></span>  <br/> |<span data-ttu-id="7cf4f-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7cf4f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf4f-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-122">optional</span></span>  <br/> ||<span data-ttu-id="7cf4f-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf4f-124">Флаги</span><span class="sxs-lookup"><span data-stu-id="7cf4f-124">Flags</span></span>  <br/> |<span data-ttu-id="7cf4f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7cf4f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7cf4f-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-126">optional</span></span>  <br/> ||<span data-ttu-id="7cf4f-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7cf4f-128">NameU</span><span class="sxs-lookup"><span data-stu-id="7cf4f-128">NameU</span></span>  <br/> |<span data-ttu-id="7cf4f-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7cf4f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf4f-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-130">required</span></span>  <br/> ||<span data-ttu-id="7cf4f-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf4f-132">Panos</span><span class="sxs-lookup"><span data-stu-id="7cf4f-132">Panos</span></span>  <br/> |<span data-ttu-id="7cf4f-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7cf4f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf4f-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-134">optional</span></span>  <br/> ||<span data-ttu-id="7cf4f-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf4f-136">Сходстве</span><span class="sxs-lookup"><span data-stu-id="7cf4f-136">Panose</span></span>  <br/> |<span data-ttu-id="7cf4f-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7cf4f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf4f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-138">optional</span></span>  <br/> ||<span data-ttu-id="7cf4f-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf4f-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="7cf4f-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="7cf4f-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7cf4f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf4f-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="7cf4f-142">optional</span></span>  <br/> ||<span data-ttu-id="7cf4f-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7cf4f-143">Values of the xsd:string type.</span></span>  <br/> |
   

