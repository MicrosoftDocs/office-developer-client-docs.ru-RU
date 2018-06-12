---
title: RowMap_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814684"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="45edc-102">RowMap_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="45edc-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="45edc-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="45edc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45edc-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="45edc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="45edc-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="45edc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="45edc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="45edc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="45edc-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="45edc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="45edc-108">Нет</span><span class="sxs-lookup"><span data-stu-id="45edc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="45edc-109">Определение</span><span class="sxs-lookup"><span data-stu-id="45edc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="45edc-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="45edc-110">Elements and attributes</span></span>

<span data-ttu-id="45edc-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="45edc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="45edc-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="45edc-112">Child elements</span></span>

<span data-ttu-id="45edc-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="45edc-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45edc-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="45edc-114">Attributes</span></span>

|<span data-ttu-id="45edc-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="45edc-115">**Attribute**</span></span>|<span data-ttu-id="45edc-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="45edc-116">**Type**</span></span>|<span data-ttu-id="45edc-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="45edc-117">**Required**</span></span>|<span data-ttu-id="45edc-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45edc-118">**Description**</span></span>|<span data-ttu-id="45edc-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="45edc-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="45edc-120">PageID</span><span class="sxs-lookup"><span data-stu-id="45edc-120">PageID</span></span>  <br/> |<span data-ttu-id="45edc-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="45edc-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45edc-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45edc-122">required</span></span>  <br/> ||<span data-ttu-id="45edc-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="45edc-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45edc-124">RowID</span><span class="sxs-lookup"><span data-stu-id="45edc-124">RowID</span></span>  <br/> |<span data-ttu-id="45edc-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="45edc-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45edc-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45edc-126">required</span></span>  <br/> ||<span data-ttu-id="45edc-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="45edc-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45edc-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="45edc-128">ShapeID</span></span>  <br/> |<span data-ttu-id="45edc-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="45edc-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45edc-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45edc-130">required</span></span>  <br/> ||<span data-ttu-id="45edc-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="45edc-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

