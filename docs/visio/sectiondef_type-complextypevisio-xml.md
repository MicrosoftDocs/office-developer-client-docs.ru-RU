---
title: SectionDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: cd85dd97a8de7bc9a9ca34fd19669dd294fe6905
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589758"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="59d8b-102">SectionDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="59d8b-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="59d8b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="59d8b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59d8b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="59d8b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="59d8b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="59d8b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="59d8b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="59d8b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="59d8b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="59d8b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="59d8b-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="59d8b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59d8b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="59d8b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="59d8b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="59d8b-110">Elements and attributes</span></span>

<span data-ttu-id="59d8b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="59d8b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="59d8b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="59d8b-112">Child elements</span></span>

|<span data-ttu-id="59d8b-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="59d8b-113">**Element**</span></span>|<span data-ttu-id="59d8b-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="59d8b-114">**Type**</span></span>|<span data-ttu-id="59d8b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59d8b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="59d8b-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="59d8b-116">CellDef</span></span> <br/> |[<span data-ttu-id="59d8b-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="59d8b-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="59d8b-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="59d8b-118">RowDef</span></span> <br/> |[<span data-ttu-id="59d8b-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="59d8b-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="59d8b-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="59d8b-120">Attributes</span></span>

|<span data-ttu-id="59d8b-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="59d8b-121">**Attribute**</span></span>|<span data-ttu-id="59d8b-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="59d8b-122">**Type**</span></span>|<span data-ttu-id="59d8b-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="59d8b-123">**Required**</span></span>|<span data-ttu-id="59d8b-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59d8b-124">**Description**</span></span>|<span data-ttu-id="59d8b-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="59d8b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59d8b-126">N</span><span class="sxs-lookup"><span data-stu-id="59d8b-126">N</span></span>  <br/> |<span data-ttu-id="59d8b-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="59d8b-127">xsd:string</span></span>  <br/> |<span data-ttu-id="59d8b-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="59d8b-128">required</span></span>  <br/> ||<span data-ttu-id="59d8b-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="59d8b-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59d8b-130">s</span><span class="sxs-lookup"><span data-stu-id="59d8b-130">S</span></span>  <br/> |<span data-ttu-id="59d8b-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="59d8b-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="59d8b-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="59d8b-132">optional</span></span>  <br/> ||<span data-ttu-id="59d8b-133">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="59d8b-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="59d8b-134">T</span><span class="sxs-lookup"><span data-stu-id="59d8b-134">T</span></span>  <br/> |<span data-ttu-id="59d8b-135">XSD:String</span><span class="sxs-lookup"><span data-stu-id="59d8b-135">xsd:string</span></span>  <br/> |<span data-ttu-id="59d8b-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="59d8b-136">optional</span></span>  <br/> ||<span data-ttu-id="59d8b-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="59d8b-137">Values of the xsd:string type.</span></span>  <br/> |
   

