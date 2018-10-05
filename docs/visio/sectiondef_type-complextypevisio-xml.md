---
title: SectionDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395079"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="dbbeb-102">SectionDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="dbbeb-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="dbbeb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="dbbeb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbbeb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dbbeb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dbbeb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="dbbeb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dbbeb-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dbbeb-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="dbbeb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dbbeb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="dbbeb-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dbbeb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="dbbeb-110">Elements and attributes</span></span>

<span data-ttu-id="dbbeb-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="dbbeb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dbbeb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dbbeb-112">Child elements</span></span>

|<span data-ttu-id="dbbeb-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-113">**Element**</span></span>|<span data-ttu-id="dbbeb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-114">**Type**</span></span>|<span data-ttu-id="dbbeb-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dbbeb-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="dbbeb-116">CellDef</span></span> <br/> |[<span data-ttu-id="dbbeb-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="dbbeb-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="dbbeb-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="dbbeb-118">RowDef</span></span> <br/> |[<span data-ttu-id="dbbeb-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="dbbeb-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="dbbeb-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dbbeb-120">Attributes</span></span>

|<span data-ttu-id="dbbeb-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-121">**Attribute**</span></span>|<span data-ttu-id="dbbeb-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-122">**Type**</span></span>|<span data-ttu-id="dbbeb-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-123">**Required**</span></span>|<span data-ttu-id="dbbeb-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-124">**Description**</span></span>|<span data-ttu-id="dbbeb-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="dbbeb-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dbbeb-126">N</span><span class="sxs-lookup"><span data-stu-id="dbbeb-126">N</span></span>  <br/> |<span data-ttu-id="dbbeb-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="dbbeb-127">xsd:string</span></span>  <br/> |<span data-ttu-id="dbbeb-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dbbeb-128">required</span></span>  <br/> ||<span data-ttu-id="dbbeb-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dbbeb-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dbbeb-130">s</span><span class="sxs-lookup"><span data-stu-id="dbbeb-130">S</span></span>  <br/> |<span data-ttu-id="dbbeb-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dbbeb-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="dbbeb-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="dbbeb-132">optional</span></span>  <br/> ||<span data-ttu-id="dbbeb-133">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="dbbeb-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="dbbeb-134">T</span><span class="sxs-lookup"><span data-stu-id="dbbeb-134">T</span></span>  <br/> |<span data-ttu-id="dbbeb-135">XSD:String</span><span class="sxs-lookup"><span data-stu-id="dbbeb-135">xsd:string</span></span>  <br/> |<span data-ttu-id="dbbeb-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="dbbeb-136">optional</span></span>  <br/> ||<span data-ttu-id="dbbeb-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dbbeb-137">Values of the xsd:string type.</span></span>  <br/> |
   

