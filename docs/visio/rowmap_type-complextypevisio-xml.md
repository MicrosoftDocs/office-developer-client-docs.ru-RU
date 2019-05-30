---
title: Ровмап_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538776"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="36d6b-102">Ровмап_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="36d6b-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="36d6b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="36d6b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36d6b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="36d6b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36d6b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="36d6b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36d6b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="36d6b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36d6b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="36d6b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36d6b-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="36d6b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36d6b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="36d6b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36d6b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="36d6b-110">Elements and attributes</span></span>

<span data-ttu-id="36d6b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="36d6b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36d6b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36d6b-112">Child elements</span></span>

<span data-ttu-id="36d6b-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="36d6b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36d6b-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36d6b-114">Attributes</span></span>

|<span data-ttu-id="36d6b-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="36d6b-115">**Attribute**</span></span>|<span data-ttu-id="36d6b-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="36d6b-116">**Type**</span></span>|<span data-ttu-id="36d6b-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="36d6b-117">**Required**</span></span>|<span data-ttu-id="36d6b-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36d6b-118">**Description**</span></span>|<span data-ttu-id="36d6b-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="36d6b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="36d6b-120">PageID</span><span class="sxs-lookup"><span data-stu-id="36d6b-120">PageID</span></span>  <br/> |<span data-ttu-id="36d6b-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="36d6b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36d6b-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="36d6b-122">required</span></span>  <br/> ||<span data-ttu-id="36d6b-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="36d6b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36d6b-124">RowID</span><span class="sxs-lookup"><span data-stu-id="36d6b-124">RowID</span></span>  <br/> |<span data-ttu-id="36d6b-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="36d6b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36d6b-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="36d6b-126">required</span></span>  <br/> ||<span data-ttu-id="36d6b-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="36d6b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36d6b-128">Шапеид</span><span class="sxs-lookup"><span data-stu-id="36d6b-128">ShapeID</span></span>  <br/> |<span data-ttu-id="36d6b-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="36d6b-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36d6b-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="36d6b-130">required</span></span>  <br/> ||<span data-ttu-id="36d6b-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="36d6b-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

