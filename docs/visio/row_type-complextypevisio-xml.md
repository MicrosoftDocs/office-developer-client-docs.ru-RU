---
title: Ров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: ebd3b666590e6144d2a3cb6e0059b64eb6e8dab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331649"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="651ef-102">Ров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="651ef-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="651ef-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="651ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="651ef-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="651ef-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="651ef-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="651ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="651ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="651ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="651ef-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="651ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="651ef-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="651ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="651ef-109">Определение</span><span class="sxs-lookup"><span data-stu-id="651ef-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="651ef-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="651ef-110">Elements and attributes</span></span>

<span data-ttu-id="651ef-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="651ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="651ef-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="651ef-112">Child elements</span></span>

|<span data-ttu-id="651ef-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="651ef-113">**Element**</span></span>|<span data-ttu-id="651ef-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="651ef-114">**Type**</span></span>|<span data-ttu-id="651ef-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="651ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="651ef-116">Cell</span><span class="sxs-lookup"><span data-stu-id="651ef-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="651ef-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="651ef-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="651ef-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="651ef-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="651ef-119">Тригжер_типе</span><span class="sxs-lookup"><span data-stu-id="651ef-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="651ef-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="651ef-120">Attributes</span></span>

|<span data-ttu-id="651ef-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="651ef-121">**Attribute**</span></span>|<span data-ttu-id="651ef-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="651ef-122">**Type**</span></span>|<span data-ttu-id="651ef-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="651ef-123">**Required**</span></span>|<span data-ttu-id="651ef-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="651ef-124">**Description**</span></span>|<span data-ttu-id="651ef-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="651ef-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="651ef-126">Del</span><span class="sxs-lookup"><span data-stu-id="651ef-126">Del</span></span>  <br/> |<span data-ttu-id="651ef-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="651ef-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="651ef-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="651ef-128">optional</span></span>  <br/> ||<span data-ttu-id="651ef-129">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="651ef-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="651ef-130">IX</span><span class="sxs-lookup"><span data-stu-id="651ef-130">IX</span></span>  <br/> |<span data-ttu-id="651ef-131">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="651ef-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="651ef-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="651ef-132">optional</span></span>  <br/> ||<span data-ttu-id="651ef-133">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="651ef-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="651ef-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="651ef-134">LocalName</span></span>  <br/> |<span data-ttu-id="651ef-135">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="651ef-135">xsd:string</span></span>  <br/> |<span data-ttu-id="651ef-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="651ef-136">optional</span></span>  <br/> ||<span data-ttu-id="651ef-137">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="651ef-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="651ef-138">N</span><span class="sxs-lookup"><span data-stu-id="651ef-138">N</span></span>  <br/> |<span data-ttu-id="651ef-139">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="651ef-139">xsd:string</span></span>  <br/> |<span data-ttu-id="651ef-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="651ef-140">optional</span></span>  <br/> ||<span data-ttu-id="651ef-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="651ef-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="651ef-142">Д</span><span class="sxs-lookup"><span data-stu-id="651ef-142">T</span></span>  <br/> |<span data-ttu-id="651ef-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="651ef-143">xsd:string</span></span>  <br/> |<span data-ttu-id="651ef-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="651ef-144">optional</span></span>  <br/> ||<span data-ttu-id="651ef-145">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="651ef-145">Values of the xsd:string type.</span></span>  <br/> |
   

