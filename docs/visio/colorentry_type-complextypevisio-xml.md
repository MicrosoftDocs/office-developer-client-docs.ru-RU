---
title: ColorEntry_Type ComplexType (Visio XML)
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
# <a name="colorentry_type-complextype-visio-xml"></a><span data-ttu-id="3a2f0-102">ColorEntry_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3a2f0-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3a2f0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3a2f0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a2f0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3a2f0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3a2f0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3a2f0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3a2f0-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3a2f0-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="3a2f0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3a2f0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3a2f0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3a2f0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3a2f0-110">Elements and attributes</span></span>

<span data-ttu-id="3a2f0-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3a2f0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3a2f0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3a2f0-112">Child elements</span></span>

<span data-ttu-id="3a2f0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="3a2f0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a2f0-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3a2f0-114">Attributes</span></span>

|<span data-ttu-id="3a2f0-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-115">**Attribute**</span></span>|<span data-ttu-id="3a2f0-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-116">**Type**</span></span>|<span data-ttu-id="3a2f0-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-117">**Required**</span></span>|<span data-ttu-id="3a2f0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-118">**Description**</span></span>|<span data-ttu-id="3a2f0-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3a2f0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3a2f0-120">IX</span><span class="sxs-lookup"><span data-stu-id="3a2f0-120">IX</span></span>  <br/> |<span data-ttu-id="3a2f0-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3a2f0-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a2f0-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3a2f0-122">required</span></span>  <br/> ||<span data-ttu-id="3a2f0-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3a2f0-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3a2f0-124">RGB</span><span class="sxs-lookup"><span data-stu-id="3a2f0-124">RGB</span></span>  <br/> |<span data-ttu-id="3a2f0-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3a2f0-125">xsd:string</span></span>  <br/> |<span data-ttu-id="3a2f0-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3a2f0-126">required</span></span>  <br/> ||<span data-ttu-id="3a2f0-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3a2f0-127">Values of the xsd:string type.</span></span>  <br/> |
   

