---
title: ColorEntry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394911"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="07593-102">ColorEntry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="07593-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="07593-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="07593-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07593-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="07593-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="07593-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="07593-105">**Schema file**</span></span> <br/> |<span data-ttu-id="07593-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="07593-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="07593-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="07593-107">**Extension base**</span></span> <br/> |<span data-ttu-id="07593-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="07593-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="07593-109">Определение</span><span class="sxs-lookup"><span data-stu-id="07593-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="07593-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="07593-110">Elements and attributes</span></span>

<span data-ttu-id="07593-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="07593-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="07593-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="07593-112">Child elements</span></span>

<span data-ttu-id="07593-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="07593-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07593-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="07593-114">Attributes</span></span>

|<span data-ttu-id="07593-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="07593-115">**Attribute**</span></span>|<span data-ttu-id="07593-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="07593-116">**Type**</span></span>|<span data-ttu-id="07593-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="07593-117">**Required**</span></span>|<span data-ttu-id="07593-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07593-118">**Description**</span></span>|<span data-ttu-id="07593-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="07593-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="07593-120">IX</span><span class="sxs-lookup"><span data-stu-id="07593-120">IX</span></span>  <br/> |<span data-ttu-id="07593-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="07593-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="07593-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="07593-122">required</span></span>  <br/> ||<span data-ttu-id="07593-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="07593-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="07593-124">RGB</span><span class="sxs-lookup"><span data-stu-id="07593-124">RGB</span></span>  <br/> |<span data-ttu-id="07593-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="07593-125">xsd:string</span></span>  <br/> |<span data-ttu-id="07593-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="07593-126">required</span></span>  <br/> ||<span data-ttu-id="07593-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="07593-127">Values of the xsd:string type.</span></span>  <br/> |
   

