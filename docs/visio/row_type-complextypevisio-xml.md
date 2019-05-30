---
title: Ров_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: d728363e6a3e7cd7fca2b95d91469f0d50ae1c39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538160"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="aa60a-102">Ров_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="aa60a-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="aa60a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="aa60a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa60a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="aa60a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aa60a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="aa60a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aa60a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aa60a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aa60a-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="aa60a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aa60a-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="aa60a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa60a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="aa60a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="aa60a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="aa60a-110">Elements and attributes</span></span>

<span data-ttu-id="aa60a-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="aa60a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aa60a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aa60a-112">Child elements</span></span>

|<span data-ttu-id="aa60a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="aa60a-113">**Element**</span></span>|<span data-ttu-id="aa60a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aa60a-114">**Type**</span></span>|<span data-ttu-id="aa60a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa60a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa60a-116">Cell</span><span class="sxs-lookup"><span data-stu-id="aa60a-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="aa60a-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="aa60a-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="aa60a-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="aa60a-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="aa60a-119">Тригжер_типе</span><span class="sxs-lookup"><span data-stu-id="aa60a-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aa60a-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aa60a-120">Attributes</span></span>

|<span data-ttu-id="aa60a-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="aa60a-121">**Attribute**</span></span>|<span data-ttu-id="aa60a-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aa60a-122">**Type**</span></span>|<span data-ttu-id="aa60a-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="aa60a-123">**Required**</span></span>|<span data-ttu-id="aa60a-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa60a-124">**Description**</span></span>|<span data-ttu-id="aa60a-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="aa60a-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa60a-126">Del</span><span class="sxs-lookup"><span data-stu-id="aa60a-126">Del</span></span>  <br/> |<span data-ttu-id="aa60a-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="aa60a-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aa60a-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="aa60a-128">optional</span></span>  <br/> ||<span data-ttu-id="aa60a-129">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="aa60a-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aa60a-130">IX</span><span class="sxs-lookup"><span data-stu-id="aa60a-130">IX</span></span>  <br/> |<span data-ttu-id="aa60a-131">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="aa60a-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="aa60a-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="aa60a-132">optional</span></span>  <br/> ||<span data-ttu-id="aa60a-133">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="aa60a-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="aa60a-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="aa60a-134">LocalName</span></span>  <br/> |<span data-ttu-id="aa60a-135">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="aa60a-135">xsd:string</span></span>  <br/> |<span data-ttu-id="aa60a-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="aa60a-136">optional</span></span>  <br/> ||<span data-ttu-id="aa60a-137">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="aa60a-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa60a-138">N</span><span class="sxs-lookup"><span data-stu-id="aa60a-138">N</span></span>  <br/> |<span data-ttu-id="aa60a-139">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="aa60a-139">xsd:string</span></span>  <br/> |<span data-ttu-id="aa60a-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="aa60a-140">optional</span></span>  <br/> ||<span data-ttu-id="aa60a-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="aa60a-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="aa60a-142">Д</span><span class="sxs-lookup"><span data-stu-id="aa60a-142">T</span></span>  <br/> |<span data-ttu-id="aa60a-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="aa60a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="aa60a-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="aa60a-144">optional</span></span>  <br/> ||<span data-ttu-id="aa60a-145">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="aa60a-145">Values of the xsd:string type.</span></span>  <br/> |
   

