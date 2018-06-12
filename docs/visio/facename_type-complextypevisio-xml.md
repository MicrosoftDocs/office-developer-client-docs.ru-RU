---
title: FaceName_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813720"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="3b460-102">FaceName_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3b460-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3b460-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3b460-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b460-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3b460-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3b460-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3b460-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3b460-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3b460-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3b460-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="3b460-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3b460-108">Нет</span><span class="sxs-lookup"><span data-stu-id="3b460-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b460-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3b460-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3b460-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3b460-110">Elements and attributes</span></span>

<span data-ttu-id="3b460-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="3b460-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3b460-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3b460-112">Child elements</span></span>

<span data-ttu-id="3b460-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="3b460-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b460-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3b460-114">Attributes</span></span>

|<span data-ttu-id="3b460-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3b460-115">**Attribute**</span></span>|<span data-ttu-id="3b460-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3b460-116">**Type**</span></span>|<span data-ttu-id="3b460-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="3b460-117">**Required**</span></span>|<span data-ttu-id="3b460-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b460-118">**Description**</span></span>|<span data-ttu-id="3b460-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3b460-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b460-120">Наборов символов</span><span class="sxs-lookup"><span data-stu-id="3b460-120">CharSets</span></span>  <br/> |<span data-ttu-id="3b460-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3b460-121">xsd:string</span></span>  <br/> |<span data-ttu-id="3b460-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-122">optional</span></span>  <br/> ||<span data-ttu-id="3b460-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b460-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b460-124">Флаги</span><span class="sxs-lookup"><span data-stu-id="3b460-124">Flags</span></span>  <br/> |<span data-ttu-id="3b460-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3b460-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3b460-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-126">optional</span></span>  <br/> ||<span data-ttu-id="3b460-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3b460-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3b460-128">NameU</span><span class="sxs-lookup"><span data-stu-id="3b460-128">NameU</span></span>  <br/> |<span data-ttu-id="3b460-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3b460-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3b460-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-130">required</span></span>  <br/> ||<span data-ttu-id="3b460-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b460-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b460-132">Panos</span><span class="sxs-lookup"><span data-stu-id="3b460-132">Panos</span></span>  <br/> |<span data-ttu-id="3b460-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3b460-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3b460-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-134">optional</span></span>  <br/> ||<span data-ttu-id="3b460-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b460-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b460-136">Сходстве</span><span class="sxs-lookup"><span data-stu-id="3b460-136">Panose</span></span>  <br/> |<span data-ttu-id="3b460-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3b460-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3b460-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-138">optional</span></span>  <br/> ||<span data-ttu-id="3b460-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b460-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b460-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="3b460-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="3b460-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3b460-141">xsd:string</span></span>  <br/> |<span data-ttu-id="3b460-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="3b460-142">optional</span></span>  <br/> ||<span data-ttu-id="3b460-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3b460-143">Values of the xsd:string type.</span></span>  <br/> |
   

