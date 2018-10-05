---
title: DataRecordSets_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388562"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="5aeb9-102">DataRecordSets_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5aeb9-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5aeb9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5aeb9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5aeb9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5aeb9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5aeb9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5aeb9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5aeb9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5aeb9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="5aeb9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5aeb9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="5aeb9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5aeb9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5aeb9-110">Elements and attributes</span></span>

<span data-ttu-id="5aeb9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5aeb9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5aeb9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5aeb9-112">Child elements</span></span>

|<span data-ttu-id="5aeb9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-113">**Element**</span></span>|<span data-ttu-id="5aeb9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-114">**Type**</span></span>|<span data-ttu-id="5aeb9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5aeb9-116">Записей данных</span><span class="sxs-lookup"><span data-stu-id="5aeb9-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5aeb9-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="5aeb9-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5aeb9-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5aeb9-118">Attributes</span></span>

|<span data-ttu-id="5aeb9-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-119">**Attribute**</span></span>|<span data-ttu-id="5aeb9-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-120">**Type**</span></span>|<span data-ttu-id="5aeb9-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-121">**Required**</span></span>|<span data-ttu-id="5aeb9-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-122">**Description**</span></span>|<span data-ttu-id="5aeb9-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5aeb9-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5aeb9-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="5aeb9-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="5aeb9-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5aeb9-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5aeb9-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="5aeb9-126">optional</span></span>  <br/> ||<span data-ttu-id="5aeb9-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5aeb9-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5aeb9-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="5aeb9-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="5aeb9-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="5aeb9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="5aeb9-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="5aeb9-130">optional</span></span>  <br/> ||<span data-ttu-id="5aeb9-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5aeb9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5aeb9-132">NextID</span><span class="sxs-lookup"><span data-stu-id="5aeb9-132">NextID</span></span>  <br/> |<span data-ttu-id="5aeb9-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5aeb9-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5aeb9-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5aeb9-134">required</span></span>  <br/> ||<span data-ttu-id="5aeb9-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5aeb9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

