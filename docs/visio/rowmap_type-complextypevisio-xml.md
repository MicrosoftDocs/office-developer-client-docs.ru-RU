---
title: Ровмап_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355736"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="49fe0-102">Ровмап_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="49fe0-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="49fe0-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="49fe0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49fe0-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="49fe0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="49fe0-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="49fe0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="49fe0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="49fe0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="49fe0-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="49fe0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="49fe0-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="49fe0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="49fe0-109">Определение</span><span class="sxs-lookup"><span data-stu-id="49fe0-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="49fe0-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="49fe0-110">Elements and attributes</span></span>

<span data-ttu-id="49fe0-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="49fe0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="49fe0-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="49fe0-112">Child elements</span></span>

<span data-ttu-id="49fe0-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="49fe0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49fe0-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="49fe0-114">Attributes</span></span>

|<span data-ttu-id="49fe0-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="49fe0-115">**Attribute**</span></span>|<span data-ttu-id="49fe0-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="49fe0-116">**Type**</span></span>|<span data-ttu-id="49fe0-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="49fe0-117">**Required**</span></span>|<span data-ttu-id="49fe0-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="49fe0-118">**Description**</span></span>|<span data-ttu-id="49fe0-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="49fe0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="49fe0-120">PageID</span><span class="sxs-lookup"><span data-stu-id="49fe0-120">PageID</span></span>  <br/> |<span data-ttu-id="49fe0-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="49fe0-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="49fe0-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="49fe0-122">required</span></span>  <br/> ||<span data-ttu-id="49fe0-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="49fe0-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="49fe0-124">RowID</span><span class="sxs-lookup"><span data-stu-id="49fe0-124">RowID</span></span>  <br/> |<span data-ttu-id="49fe0-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="49fe0-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="49fe0-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="49fe0-126">required</span></span>  <br/> ||<span data-ttu-id="49fe0-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="49fe0-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="49fe0-128">Шапеид</span><span class="sxs-lookup"><span data-stu-id="49fe0-128">ShapeID</span></span>  <br/> |<span data-ttu-id="49fe0-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="49fe0-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="49fe0-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="49fe0-130">required</span></span>  <br/> ||<span data-ttu-id="49fe0-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="49fe0-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

