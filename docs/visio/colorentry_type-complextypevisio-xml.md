---
title: Колорентри_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: c5f2cafba60cd8157f80dc548cea328d179e74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358781"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="96f45-102">Колорентри_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="96f45-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="96f45-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="96f45-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96f45-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="96f45-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="96f45-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="96f45-105">**Schema file**</span></span> <br/> |<span data-ttu-id="96f45-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="96f45-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="96f45-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="96f45-107">**Extension base**</span></span> <br/> |<span data-ttu-id="96f45-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="96f45-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96f45-109">Определение</span><span class="sxs-lookup"><span data-stu-id="96f45-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="96f45-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="96f45-110">Elements and attributes</span></span>

<span data-ttu-id="96f45-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="96f45-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="96f45-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="96f45-112">Child elements</span></span>

<span data-ttu-id="96f45-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="96f45-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96f45-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="96f45-114">Attributes</span></span>

|<span data-ttu-id="96f45-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="96f45-115">**Attribute**</span></span>|<span data-ttu-id="96f45-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="96f45-116">**Type**</span></span>|<span data-ttu-id="96f45-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="96f45-117">**Required**</span></span>|<span data-ttu-id="96f45-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96f45-118">**Description**</span></span>|<span data-ttu-id="96f45-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="96f45-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96f45-120">IX</span><span class="sxs-lookup"><span data-stu-id="96f45-120">IX</span></span>  <br/> |<span data-ttu-id="96f45-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="96f45-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="96f45-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96f45-122">required</span></span>  <br/> ||<span data-ttu-id="96f45-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="96f45-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="96f45-124">RGB</span><span class="sxs-lookup"><span data-stu-id="96f45-124">RGB</span></span>  <br/> |<span data-ttu-id="96f45-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="96f45-125">xsd:string</span></span>  <br/> |<span data-ttu-id="96f45-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96f45-126">required</span></span>  <br/> ||<span data-ttu-id="96f45-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="96f45-127">Values of the xsd:string type.</span></span>  <br/> |
   

