---
title: DataRecordSets_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 77a6588a1b5fba05d14e91a39ba570d21142f953
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539160"
---
# <a name="datarecordsets_type-complextype-visio-xml"></a><span data-ttu-id="435d9-102">DataRecordSets_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="435d9-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="435d9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="435d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="435d9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="435d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="435d9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="435d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="435d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="435d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="435d9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="435d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="435d9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="435d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="435d9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="435d9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="435d9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="435d9-110">Elements and attributes</span></span>

<span data-ttu-id="435d9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="435d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="435d9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="435d9-112">Child elements</span></span>

|<span data-ttu-id="435d9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="435d9-113">**Element**</span></span>|<span data-ttu-id="435d9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="435d9-114">**Type**</span></span>|<span data-ttu-id="435d9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="435d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="435d9-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="435d9-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="435d9-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="435d9-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="435d9-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="435d9-118">Attributes</span></span>

|<span data-ttu-id="435d9-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="435d9-119">**Attribute**</span></span>|<span data-ttu-id="435d9-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="435d9-120">**Type**</span></span>|<span data-ttu-id="435d9-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="435d9-121">**Required**</span></span>|<span data-ttu-id="435d9-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="435d9-122">**Description**</span></span>|<span data-ttu-id="435d9-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="435d9-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="435d9-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="435d9-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="435d9-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="435d9-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="435d9-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="435d9-126">optional</span></span>  <br/> ||<span data-ttu-id="435d9-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="435d9-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="435d9-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="435d9-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="435d9-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="435d9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="435d9-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="435d9-130">optional</span></span>  <br/> ||<span data-ttu-id="435d9-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="435d9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="435d9-132">NextID</span><span class="sxs-lookup"><span data-stu-id="435d9-132">NextID</span></span>  <br/> |<span data-ttu-id="435d9-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="435d9-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="435d9-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="435d9-134">required</span></span>  <br/> ||<span data-ttu-id="435d9-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="435d9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

