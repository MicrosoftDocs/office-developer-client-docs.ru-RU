---
title: Row_Type ComplexType (Visio XML)
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
# <a name="row_type-complextype-visio-xml"></a><span data-ttu-id="a4bb1-102">Row_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a4bb1-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a4bb1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a4bb1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4bb1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a4bb1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a4bb1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a4bb1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a4bb1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a4bb1-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a4bb1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4bb1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a4bb1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a4bb1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a4bb1-110">Elements and attributes</span></span>

<span data-ttu-id="a4bb1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a4bb1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a4bb1-112">Child elements</span></span>

|<span data-ttu-id="a4bb1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-113">**Element**</span></span>|<span data-ttu-id="a4bb1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-114">**Type**</span></span>|<span data-ttu-id="a4bb1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4bb1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a4bb1-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a4bb1-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a4bb1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a4bb1-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="a4bb1-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="a4bb1-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="a4bb1-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a4bb1-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a4bb1-120">Attributes</span></span>

|<span data-ttu-id="a4bb1-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-121">**Attribute**</span></span>|<span data-ttu-id="a4bb1-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-122">**Type**</span></span>|<span data-ttu-id="a4bb1-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-123">**Required**</span></span>|<span data-ttu-id="a4bb1-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-124">**Description**</span></span>|<span data-ttu-id="a4bb1-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a4bb1-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4bb1-126">Del</span><span class="sxs-lookup"><span data-stu-id="a4bb1-126">Del</span></span>  <br/> |<span data-ttu-id="a4bb1-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a4bb1-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a4bb1-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="a4bb1-128">optional</span></span>  <br/> ||<span data-ttu-id="a4bb1-129">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a4bb1-130">IX</span><span class="sxs-lookup"><span data-stu-id="a4bb1-130">IX</span></span>  <br/> |<span data-ttu-id="a4bb1-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a4bb1-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a4bb1-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="a4bb1-132">optional</span></span>  <br/> ||<span data-ttu-id="a4bb1-133">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a4bb1-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="a4bb1-134">LocalName</span></span>  <br/> |<span data-ttu-id="a4bb1-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4bb1-135">xsd:string</span></span>  <br/> |<span data-ttu-id="a4bb1-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="a4bb1-136">optional</span></span>  <br/> ||<span data-ttu-id="a4bb1-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4bb1-138">Нет</span><span class="sxs-lookup"><span data-stu-id="a4bb1-138">N</span></span>  <br/> |<span data-ttu-id="a4bb1-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4bb1-139">xsd:string</span></span>  <br/> |<span data-ttu-id="a4bb1-140">необязательный</span><span class="sxs-lookup"><span data-stu-id="a4bb1-140">optional</span></span>  <br/> ||<span data-ttu-id="a4bb1-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4bb1-142">T</span><span class="sxs-lookup"><span data-stu-id="a4bb1-142">T</span></span>  <br/> |<span data-ttu-id="a4bb1-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4bb1-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a4bb1-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="a4bb1-144">optional</span></span>  <br/> ||<span data-ttu-id="a4bb1-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-145">Values of the xsd:string type.</span></span>  <br/> |
   

