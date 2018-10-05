---
title: Cell_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389465"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="ada97-102">Cell_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ada97-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ada97-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ada97-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ada97-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ada97-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ada97-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ada97-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ada97-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ada97-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ada97-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ada97-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ada97-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ada97-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ada97-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ada97-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ada97-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ada97-110">Elements and attributes</span></span>

<span data-ttu-id="ada97-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ada97-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ada97-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ada97-112">Child elements</span></span>

|<span data-ttu-id="ada97-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ada97-113">**Element**</span></span>|<span data-ttu-id="ada97-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ada97-114">**Type**</span></span>|<span data-ttu-id="ada97-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ada97-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ada97-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="ada97-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ada97-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ada97-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ada97-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ada97-118">Attributes</span></span>

|<span data-ttu-id="ada97-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ada97-119">**Attribute**</span></span>|<span data-ttu-id="ada97-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ada97-120">**Type**</span></span>|<span data-ttu-id="ada97-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ada97-121">**Required**</span></span>|<span data-ttu-id="ada97-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ada97-122">**Description**</span></span>|<span data-ttu-id="ada97-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ada97-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ada97-124">E</span><span class="sxs-lookup"><span data-stu-id="ada97-124">E</span></span>  <br/> |<span data-ttu-id="ada97-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ada97-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ada97-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="ada97-126">optional</span></span>  <br/> ||<span data-ttu-id="ada97-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ada97-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ada97-128">F</span><span class="sxs-lookup"><span data-stu-id="ada97-128">F</span></span>  <br/> |<span data-ttu-id="ada97-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ada97-129">xsd:string</span></span>  <br/> |<span data-ttu-id="ada97-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="ada97-130">optional</span></span>  <br/> ||<span data-ttu-id="ada97-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ada97-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ada97-132">N</span><span class="sxs-lookup"><span data-stu-id="ada97-132">N</span></span>  <br/> |<span data-ttu-id="ada97-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ada97-133">xsd:string</span></span>  <br/> |<span data-ttu-id="ada97-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ada97-134">required</span></span>  <br/> ||<span data-ttu-id="ada97-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ada97-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ada97-136">U</span><span class="sxs-lookup"><span data-stu-id="ada97-136">U</span></span>  <br/> |<span data-ttu-id="ada97-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ada97-137">xsd:string</span></span>  <br/> |<span data-ttu-id="ada97-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ada97-138">optional</span></span>  <br/> ||<span data-ttu-id="ada97-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ada97-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ada97-140">V</span><span class="sxs-lookup"><span data-stu-id="ada97-140">V</span></span>  <br/> |<span data-ttu-id="ada97-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ada97-141">xsd:string</span></span>  <br/> |<span data-ttu-id="ada97-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="ada97-142">optional</span></span>  <br/> ||<span data-ttu-id="ada97-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ada97-143">Values of the xsd:string type.</span></span>  <br/> |
   

