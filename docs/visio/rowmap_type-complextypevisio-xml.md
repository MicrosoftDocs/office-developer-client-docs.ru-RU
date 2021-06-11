---
title: RowMap_Type ComplexType (Visio XML)
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
# <a name="rowmap_type-complextype-visio-xml"></a><span data-ttu-id="76b61-102">RowMap_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="76b61-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="76b61-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="76b61-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76b61-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="76b61-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="76b61-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="76b61-105">**Schema file**</span></span> <br/> |<span data-ttu-id="76b61-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="76b61-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="76b61-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="76b61-107">**Extension base**</span></span> <br/> |<span data-ttu-id="76b61-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="76b61-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76b61-109">Определение</span><span class="sxs-lookup"><span data-stu-id="76b61-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="76b61-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="76b61-110">Elements and attributes</span></span>

<span data-ttu-id="76b61-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="76b61-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="76b61-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76b61-112">Child elements</span></span>

<span data-ttu-id="76b61-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="76b61-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76b61-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76b61-114">Attributes</span></span>

|<span data-ttu-id="76b61-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="76b61-115">**Attribute**</span></span>|<span data-ttu-id="76b61-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76b61-116">**Type**</span></span>|<span data-ttu-id="76b61-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="76b61-117">**Required**</span></span>|<span data-ttu-id="76b61-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76b61-118">**Description**</span></span>|<span data-ttu-id="76b61-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="76b61-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="76b61-120">PageID</span><span class="sxs-lookup"><span data-stu-id="76b61-120">PageID</span></span>  <br/> |<span data-ttu-id="76b61-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76b61-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76b61-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76b61-122">required</span></span>  <br/> ||<span data-ttu-id="76b61-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76b61-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76b61-124">RowID</span><span class="sxs-lookup"><span data-stu-id="76b61-124">RowID</span></span>  <br/> |<span data-ttu-id="76b61-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76b61-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76b61-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76b61-126">required</span></span>  <br/> ||<span data-ttu-id="76b61-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76b61-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76b61-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="76b61-128">ShapeID</span></span>  <br/> |<span data-ttu-id="76b61-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76b61-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76b61-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76b61-130">required</span></span>  <br/> ||<span data-ttu-id="76b61-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="76b61-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

