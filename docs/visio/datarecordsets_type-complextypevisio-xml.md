---
title: Датарекордсетс_типе complexType (XML для Visio)
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
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="1a89a-102">Датарекордсетс_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1a89a-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1a89a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1a89a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a89a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1a89a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a89a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1a89a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a89a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a89a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a89a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1a89a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a89a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1a89a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a89a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1a89a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1a89a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a89a-110">Elements and attributes</span></span>

<span data-ttu-id="1a89a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1a89a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a89a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1a89a-112">Child elements</span></span>

|<span data-ttu-id="1a89a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1a89a-113">**Element**</span></span>|<span data-ttu-id="1a89a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1a89a-114">**Type**</span></span>|<span data-ttu-id="1a89a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a89a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a89a-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="1a89a-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1a89a-117">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="1a89a-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1a89a-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a89a-118">Attributes</span></span>

|<span data-ttu-id="1a89a-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1a89a-119">**Attribute**</span></span>|<span data-ttu-id="1a89a-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1a89a-120">**Type**</span></span>|<span data-ttu-id="1a89a-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1a89a-121">**Required**</span></span>|<span data-ttu-id="1a89a-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a89a-122">**Description**</span></span>|<span data-ttu-id="1a89a-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1a89a-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1a89a-124">Активерекордсетид</span><span class="sxs-lookup"><span data-stu-id="1a89a-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="1a89a-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="1a89a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1a89a-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1a89a-126">optional</span></span>  <br/> ||<span data-ttu-id="1a89a-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="1a89a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1a89a-128">Датавиндовордер</span><span class="sxs-lookup"><span data-stu-id="1a89a-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="1a89a-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1a89a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1a89a-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="1a89a-130">optional</span></span>  <br/> ||<span data-ttu-id="1a89a-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1a89a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1a89a-132">Некстид</span><span class="sxs-lookup"><span data-stu-id="1a89a-132">NextID</span></span>  <br/> |<span data-ttu-id="1a89a-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="1a89a-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1a89a-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1a89a-134">required</span></span>  <br/> ||<span data-ttu-id="1a89a-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="1a89a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

