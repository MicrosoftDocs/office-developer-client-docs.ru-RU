---
title: Датарекордсетс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360349"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="c8c9f-102">Датарекордсетс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c8c9f-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c8c9f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c8c9f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8c9f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8c9f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8c9f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c8c9f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8c9f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8c9f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="c8c9f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8c9f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c8c9f-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c8c9f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c8c9f-110">Elements and attributes</span></span>

<span data-ttu-id="c8c9f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c8c9f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8c9f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c8c9f-112">Child elements</span></span>

|<span data-ttu-id="c8c9f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-113">**Element**</span></span>|<span data-ttu-id="c8c9f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-114">**Type**</span></span>|<span data-ttu-id="c8c9f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8c9f-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="c8c9f-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8c9f-117">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="c8c9f-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8c9f-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c8c9f-118">Attributes</span></span>

|<span data-ttu-id="c8c9f-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-119">**Attribute**</span></span>|<span data-ttu-id="c8c9f-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-120">**Type**</span></span>|<span data-ttu-id="c8c9f-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-121">**Required**</span></span>|<span data-ttu-id="c8c9f-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-122">**Description**</span></span>|<span data-ttu-id="c8c9f-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c8c9f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c8c9f-124">Активерекордсетид</span><span class="sxs-lookup"><span data-stu-id="c8c9f-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="c8c9f-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c8c9f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c8c9f-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="c8c9f-126">optional</span></span>  <br/> ||<span data-ttu-id="c8c9f-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c8c9f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c8c9f-128">Датавиндовордер</span><span class="sxs-lookup"><span data-stu-id="c8c9f-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="c8c9f-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="c8c9f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c8c9f-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="c8c9f-130">optional</span></span>  <br/> ||<span data-ttu-id="c8c9f-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="c8c9f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c8c9f-132">Некстид</span><span class="sxs-lookup"><span data-stu-id="c8c9f-132">NextID</span></span>  <br/> |<span data-ttu-id="c8c9f-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c8c9f-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c8c9f-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c8c9f-134">required</span></span>  <br/> ||<span data-ttu-id="c8c9f-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c8c9f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

