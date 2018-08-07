---
title: Row_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: dfa3a90aaec51ba89845934c1d4fad484914afa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814680"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="d7936-102">Row_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d7936-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d7936-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d7936-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7936-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d7936-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d7936-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d7936-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d7936-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d7936-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d7936-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d7936-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d7936-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d7936-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7936-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d7936-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d7936-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d7936-110">Elements and attributes</span></span>

<span data-ttu-id="d7936-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d7936-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d7936-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d7936-112">Child elements</span></span>

|<span data-ttu-id="d7936-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d7936-113">**Element**</span></span>|<span data-ttu-id="d7936-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d7936-114">**Type**</span></span>|<span data-ttu-id="d7936-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d7936-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7936-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d7936-116">Cell</span></span>](http://msdn.microsoft.com/library/5e060a3f-e804-834f-531b-78a544fee61f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d7936-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d7936-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d7936-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="d7936-118">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d7936-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="d7936-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d7936-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d7936-120">Attributes</span></span>

|<span data-ttu-id="d7936-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d7936-121">**Attribute**</span></span>|<span data-ttu-id="d7936-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d7936-122">**Type**</span></span>|<span data-ttu-id="d7936-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d7936-123">**Required**</span></span>|<span data-ttu-id="d7936-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d7936-124">**Description**</span></span>|<span data-ttu-id="d7936-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d7936-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7936-126">DEL</span><span class="sxs-lookup"><span data-stu-id="d7936-126">Del</span></span>  <br/> |<span data-ttu-id="d7936-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d7936-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d7936-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="d7936-128">optional</span></span>  <br/> ||<span data-ttu-id="d7936-129">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d7936-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d7936-130">IX</span><span class="sxs-lookup"><span data-stu-id="d7936-130">IX</span></span>  <br/> |<span data-ttu-id="d7936-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d7936-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d7936-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="d7936-132">optional</span></span>  <br/> ||<span data-ttu-id="d7936-133">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d7936-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d7936-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="d7936-134">LocalName</span></span>  <br/> |<span data-ttu-id="d7936-135">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d7936-135">xsd:string</span></span>  <br/> |<span data-ttu-id="d7936-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="d7936-136">optional</span></span>  <br/> ||<span data-ttu-id="d7936-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d7936-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7936-138">N</span><span class="sxs-lookup"><span data-stu-id="d7936-138">N</span></span>  <br/> |<span data-ttu-id="d7936-139">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d7936-139">xsd:string</span></span>  <br/> |<span data-ttu-id="d7936-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="d7936-140">optional</span></span>  <br/> ||<span data-ttu-id="d7936-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d7936-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d7936-142">T</span><span class="sxs-lookup"><span data-stu-id="d7936-142">T</span></span>  <br/> |<span data-ttu-id="d7936-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d7936-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d7936-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="d7936-144">optional</span></span>  <br/> ||<span data-ttu-id="d7936-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d7936-145">Values of the xsd:string type.</span></span>  <br/> |
   

