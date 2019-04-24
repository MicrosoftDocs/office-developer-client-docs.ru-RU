---
title: Рефрешконфликт_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346482"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="a1bb2-102">Рефрешконфликт_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a1bb2-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a1bb2-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a1bb2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1bb2-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1bb2-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1bb2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1bb2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1bb2-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1bb2-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a1bb2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1bb2-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a1bb2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a1bb2-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1bb2-110">Elements and attributes</span></span>

<span data-ttu-id="a1bb2-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a1bb2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1bb2-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a1bb2-112">Child elements</span></span>

<span data-ttu-id="a1bb2-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="a1bb2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1bb2-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1bb2-114">Attributes</span></span>

|<span data-ttu-id="a1bb2-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-115">**Attribute**</span></span>|<span data-ttu-id="a1bb2-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-116">**Type**</span></span>|<span data-ttu-id="a1bb2-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-117">**Required**</span></span>|<span data-ttu-id="a1bb2-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-118">**Description**</span></span>|<span data-ttu-id="a1bb2-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a1bb2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a1bb2-120">PageID</span><span class="sxs-lookup"><span data-stu-id="a1bb2-120">PageID</span></span>  <br/> |<span data-ttu-id="a1bb2-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a1bb2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1bb2-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1bb2-122">required</span></span>  <br/> ||<span data-ttu-id="a1bb2-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a1bb2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a1bb2-124">RowID</span><span class="sxs-lookup"><span data-stu-id="a1bb2-124">RowID</span></span>  <br/> |<span data-ttu-id="a1bb2-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a1bb2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1bb2-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1bb2-126">required</span></span>  <br/> ||<span data-ttu-id="a1bb2-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a1bb2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a1bb2-128">Шапеид</span><span class="sxs-lookup"><span data-stu-id="a1bb2-128">ShapeID</span></span>  <br/> |<span data-ttu-id="a1bb2-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a1bb2-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1bb2-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1bb2-130">required</span></span>  <br/> ||<span data-ttu-id="a1bb2-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a1bb2-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

