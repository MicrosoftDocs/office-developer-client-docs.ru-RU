---
title: RefreshConflict_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 44910cd305b484771ca3d4f4d49ef8a09a6fc2dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814555"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="7b319-102">RefreshConflict_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7b319-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b319-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7b319-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b319-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7b319-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b319-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7b319-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b319-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b319-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b319-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="7b319-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b319-108">Нет</span><span class="sxs-lookup"><span data-stu-id="7b319-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b319-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7b319-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7b319-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b319-110">Elements and attributes</span></span>

<span data-ttu-id="7b319-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="7b319-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b319-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7b319-112">Child elements</span></span>

<span data-ttu-id="7b319-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="7b319-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b319-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b319-114">Attributes</span></span>

|<span data-ttu-id="7b319-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7b319-115">**Attribute**</span></span>|<span data-ttu-id="7b319-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7b319-116">**Type**</span></span>|<span data-ttu-id="7b319-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="7b319-117">**Required**</span></span>|<span data-ttu-id="7b319-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b319-118">**Description**</span></span>|<span data-ttu-id="7b319-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7b319-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b319-120">PageID</span><span class="sxs-lookup"><span data-stu-id="7b319-120">PageID</span></span>  <br/> |<span data-ttu-id="7b319-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b319-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b319-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b319-122">required</span></span>  <br/> ||<span data-ttu-id="7b319-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b319-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b319-124">RowID</span><span class="sxs-lookup"><span data-stu-id="7b319-124">RowID</span></span>  <br/> |<span data-ttu-id="7b319-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b319-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b319-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b319-126">required</span></span>  <br/> ||<span data-ttu-id="7b319-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b319-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b319-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7b319-128">ShapeID</span></span>  <br/> |<span data-ttu-id="7b319-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b319-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b319-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7b319-130">required</span></span>  <br/> ||<span data-ttu-id="7b319-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b319-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

