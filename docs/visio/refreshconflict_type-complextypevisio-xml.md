---
title: Рефрешконфликт_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542830"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="0c92a-102">Рефрешконфликт_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0c92a-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0c92a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0c92a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c92a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0c92a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c92a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0c92a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c92a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c92a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c92a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0c92a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c92a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0c92a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c92a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0c92a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c92a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c92a-110">Elements and attributes</span></span>

<span data-ttu-id="0c92a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0c92a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c92a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0c92a-112">Child elements</span></span>

<span data-ttu-id="0c92a-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="0c92a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c92a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c92a-114">Attributes</span></span>

|<span data-ttu-id="0c92a-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0c92a-115">**Attribute**</span></span>|<span data-ttu-id="0c92a-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0c92a-116">**Type**</span></span>|<span data-ttu-id="0c92a-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0c92a-117">**Required**</span></span>|<span data-ttu-id="0c92a-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c92a-118">**Description**</span></span>|<span data-ttu-id="0c92a-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0c92a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c92a-120">PageID</span><span class="sxs-lookup"><span data-stu-id="0c92a-120">PageID</span></span>  <br/> |<span data-ttu-id="0c92a-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0c92a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c92a-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c92a-122">required</span></span>  <br/> ||<span data-ttu-id="0c92a-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0c92a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c92a-124">RowID</span><span class="sxs-lookup"><span data-stu-id="0c92a-124">RowID</span></span>  <br/> |<span data-ttu-id="0c92a-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0c92a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c92a-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c92a-126">required</span></span>  <br/> ||<span data-ttu-id="0c92a-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0c92a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0c92a-128">Шапеид</span><span class="sxs-lookup"><span data-stu-id="0c92a-128">ShapeID</span></span>  <br/> |<span data-ttu-id="0c92a-129">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0c92a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c92a-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c92a-130">required</span></span>  <br/> ||<span data-ttu-id="0c92a-131">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0c92a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

