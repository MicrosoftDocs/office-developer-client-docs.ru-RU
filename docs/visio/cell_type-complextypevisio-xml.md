---
title: Cell_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813357"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="1ba51-102">Cell_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1ba51-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ba51-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1ba51-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ba51-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1ba51-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ba51-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1ba51-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ba51-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ba51-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ba51-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="1ba51-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ba51-108">Нет</span><span class="sxs-lookup"><span data-stu-id="1ba51-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ba51-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1ba51-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ba51-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ba51-110">Elements and attributes</span></span>

<span data-ttu-id="1ba51-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="1ba51-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ba51-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1ba51-112">Child elements</span></span>

|<span data-ttu-id="1ba51-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1ba51-113">**Element**</span></span>|<span data-ttu-id="1ba51-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1ba51-114">**Type**</span></span>|<span data-ttu-id="1ba51-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ba51-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ba51-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="1ba51-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ba51-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="1ba51-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1ba51-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1ba51-118">Attributes</span></span>

|<span data-ttu-id="1ba51-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1ba51-119">**Attribute**</span></span>|<span data-ttu-id="1ba51-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1ba51-120">**Type**</span></span>|<span data-ttu-id="1ba51-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="1ba51-121">**Required**</span></span>|<span data-ttu-id="1ba51-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1ba51-122">**Description**</span></span>|<span data-ttu-id="1ba51-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1ba51-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ba51-124">E</span><span class="sxs-lookup"><span data-stu-id="1ba51-124">E</span></span>  <br/> |<span data-ttu-id="1ba51-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ba51-125">xsd:string</span></span>  <br/> |<span data-ttu-id="1ba51-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ba51-126">optional</span></span>  <br/> ||<span data-ttu-id="1ba51-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ba51-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ba51-128">F</span><span class="sxs-lookup"><span data-stu-id="1ba51-128">F</span></span>  <br/> |<span data-ttu-id="1ba51-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ba51-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1ba51-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ba51-130">optional</span></span>  <br/> ||<span data-ttu-id="1ba51-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ba51-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ba51-132">N</span><span class="sxs-lookup"><span data-stu-id="1ba51-132">N</span></span>  <br/> |<span data-ttu-id="1ba51-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ba51-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1ba51-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1ba51-134">required</span></span>  <br/> ||<span data-ttu-id="1ba51-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ba51-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ba51-136">U</span><span class="sxs-lookup"><span data-stu-id="1ba51-136">U</span></span>  <br/> |<span data-ttu-id="1ba51-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ba51-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1ba51-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ba51-138">optional</span></span>  <br/> ||<span data-ttu-id="1ba51-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ba51-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ba51-140">V</span><span class="sxs-lookup"><span data-stu-id="1ba51-140">V</span></span>  <br/> |<span data-ttu-id="1ba51-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1ba51-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1ba51-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="1ba51-142">optional</span></span>  <br/> ||<span data-ttu-id="1ba51-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1ba51-143">Values of the xsd:string type.</span></span>  <br/> |
   

