---
title: Row_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: 6ebd483ae9b0748a3afa15360bf2c88feae44aeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586902"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="0ec33-102">Row_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0ec33-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0ec33-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0ec33-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ec33-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0ec33-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0ec33-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0ec33-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0ec33-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0ec33-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0ec33-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0ec33-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0ec33-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0ec33-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ec33-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0ec33-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ec33-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0ec33-110">Elements and attributes</span></span>

<span data-ttu-id="0ec33-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0ec33-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0ec33-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0ec33-112">Child elements</span></span>

|<span data-ttu-id="0ec33-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0ec33-113">**Element**</span></span>|<span data-ttu-id="0ec33-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0ec33-114">**Type**</span></span>|<span data-ttu-id="0ec33-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ec33-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ec33-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0ec33-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="0ec33-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0ec33-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0ec33-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="0ec33-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="0ec33-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="0ec33-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0ec33-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0ec33-120">Attributes</span></span>

|<span data-ttu-id="0ec33-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0ec33-121">**Attribute**</span></span>|<span data-ttu-id="0ec33-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0ec33-122">**Type**</span></span>|<span data-ttu-id="0ec33-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0ec33-123">**Required**</span></span>|<span data-ttu-id="0ec33-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ec33-124">**Description**</span></span>|<span data-ttu-id="0ec33-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0ec33-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0ec33-126">DEL</span><span class="sxs-lookup"><span data-stu-id="0ec33-126">Del</span></span>  <br/> |<span data-ttu-id="0ec33-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="0ec33-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0ec33-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="0ec33-128">optional</span></span>  <br/> ||<span data-ttu-id="0ec33-129">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0ec33-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0ec33-130">IX</span><span class="sxs-lookup"><span data-stu-id="0ec33-130">IX</span></span>  <br/> |<span data-ttu-id="0ec33-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0ec33-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0ec33-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="0ec33-132">optional</span></span>  <br/> ||<span data-ttu-id="0ec33-133">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0ec33-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0ec33-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="0ec33-134">LocalName</span></span>  <br/> |<span data-ttu-id="0ec33-135">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0ec33-135">xsd:string</span></span>  <br/> |<span data-ttu-id="0ec33-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="0ec33-136">optional</span></span>  <br/> ||<span data-ttu-id="0ec33-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0ec33-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0ec33-138">N</span><span class="sxs-lookup"><span data-stu-id="0ec33-138">N</span></span>  <br/> |<span data-ttu-id="0ec33-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0ec33-139">xsd:string</span></span>  <br/> |<span data-ttu-id="0ec33-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="0ec33-140">optional</span></span>  <br/> ||<span data-ttu-id="0ec33-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0ec33-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0ec33-142">T</span><span class="sxs-lookup"><span data-stu-id="0ec33-142">T</span></span>  <br/> |<span data-ttu-id="0ec33-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="0ec33-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0ec33-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="0ec33-144">optional</span></span>  <br/> ||<span data-ttu-id="0ec33-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0ec33-145">Values of the xsd:string type.</span></span>  <br/> |
   

