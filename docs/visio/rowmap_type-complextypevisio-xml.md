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
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="886ee-102">RowMap_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="886ee-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="886ee-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="886ee-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="886ee-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="886ee-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="886ee-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="886ee-105">**Schema file**</span></span> <br/> |<span data-ttu-id="886ee-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="886ee-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="886ee-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="886ee-107">**Extension base**</span></span> <br/> |<span data-ttu-id="886ee-108">Нет</span><span class="sxs-lookup"><span data-stu-id="886ee-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="886ee-109">Определение</span><span class="sxs-lookup"><span data-stu-id="886ee-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="886ee-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="886ee-110">Elements and attributes</span></span>

<span data-ttu-id="886ee-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="886ee-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="886ee-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="886ee-112">Child elements</span></span>

<span data-ttu-id="886ee-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="886ee-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="886ee-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="886ee-114">Attributes</span></span>

|<span data-ttu-id="886ee-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="886ee-115">**Attribute**</span></span>|<span data-ttu-id="886ee-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="886ee-116">**Type**</span></span>|<span data-ttu-id="886ee-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="886ee-117">**Required**</span></span>|<span data-ttu-id="886ee-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="886ee-118">**Description**</span></span>|<span data-ttu-id="886ee-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="886ee-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="886ee-120">PageID</span><span class="sxs-lookup"><span data-stu-id="886ee-120">PageID</span></span>  <br/> |<span data-ttu-id="886ee-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="886ee-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="886ee-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="886ee-122">required</span></span>  <br/> ||<span data-ttu-id="886ee-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="886ee-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="886ee-124">RowID</span><span class="sxs-lookup"><span data-stu-id="886ee-124">RowID</span></span>  <br/> |<span data-ttu-id="886ee-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="886ee-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="886ee-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="886ee-126">required</span></span>  <br/> ||<span data-ttu-id="886ee-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="886ee-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="886ee-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="886ee-128">ShapeID</span></span>  <br/> |<span data-ttu-id="886ee-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="886ee-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="886ee-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="886ee-130">required</span></span>  <br/> ||<span data-ttu-id="886ee-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="886ee-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

