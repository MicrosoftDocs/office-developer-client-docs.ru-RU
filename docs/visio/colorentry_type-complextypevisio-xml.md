---
title: ColorEntry_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540149"
---
# <a name="colorentry_type-complextype-visio-xml"></a><span data-ttu-id="dc5da-102">ColorEntry_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="dc5da-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="dc5da-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="dc5da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc5da-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="dc5da-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dc5da-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="dc5da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dc5da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dc5da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dc5da-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="dc5da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dc5da-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="dc5da-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc5da-109">Определение</span><span class="sxs-lookup"><span data-stu-id="dc5da-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc5da-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="dc5da-110">Elements and attributes</span></span>

<span data-ttu-id="dc5da-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="dc5da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dc5da-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dc5da-112">Child elements</span></span>

<span data-ttu-id="dc5da-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="dc5da-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc5da-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dc5da-114">Attributes</span></span>

|<span data-ttu-id="dc5da-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="dc5da-115">**Attribute**</span></span>|<span data-ttu-id="dc5da-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dc5da-116">**Type**</span></span>|<span data-ttu-id="dc5da-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="dc5da-117">**Required**</span></span>|<span data-ttu-id="dc5da-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc5da-118">**Description**</span></span>|<span data-ttu-id="dc5da-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="dc5da-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc5da-120">IX</span><span class="sxs-lookup"><span data-stu-id="dc5da-120">IX</span></span>  <br/> |<span data-ttu-id="dc5da-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="dc5da-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc5da-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dc5da-122">required</span></span>  <br/> ||<span data-ttu-id="dc5da-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="dc5da-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc5da-124">RGB</span><span class="sxs-lookup"><span data-stu-id="dc5da-124">RGB</span></span>  <br/> |<span data-ttu-id="dc5da-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="dc5da-125">xsd:string</span></span>  <br/> |<span data-ttu-id="dc5da-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dc5da-126">required</span></span>  <br/> ||<span data-ttu-id="dc5da-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="dc5da-127">Values of the xsd:string type.</span></span>  <br/> |
   

