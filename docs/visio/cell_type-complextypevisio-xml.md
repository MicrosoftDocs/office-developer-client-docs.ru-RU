---
title: Cell_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542305"
---
# <a name="cell_type-complextype-visio-xml"></a><span data-ttu-id="76595-102">Cell_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="76595-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="76595-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="76595-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76595-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="76595-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="76595-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="76595-105">**Schema file**</span></span> <br/> |<span data-ttu-id="76595-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="76595-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="76595-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="76595-107">**Extension base**</span></span> <br/> |<span data-ttu-id="76595-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="76595-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76595-109">Определение</span><span class="sxs-lookup"><span data-stu-id="76595-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="76595-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="76595-110">Elements and attributes</span></span>

<span data-ttu-id="76595-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="76595-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="76595-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76595-112">Child elements</span></span>

|<span data-ttu-id="76595-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="76595-113">**Element**</span></span>|<span data-ttu-id="76595-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76595-114">**Type**</span></span>|<span data-ttu-id="76595-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76595-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="76595-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="76595-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="76595-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="76595-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="76595-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76595-118">Attributes</span></span>

|<span data-ttu-id="76595-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="76595-119">**Attribute**</span></span>|<span data-ttu-id="76595-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="76595-120">**Type**</span></span>|<span data-ttu-id="76595-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="76595-121">**Required**</span></span>|<span data-ttu-id="76595-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76595-122">**Description**</span></span>|<span data-ttu-id="76595-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="76595-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="76595-124">E</span><span class="sxs-lookup"><span data-stu-id="76595-124">E</span></span>  <br/> |<span data-ttu-id="76595-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="76595-125">xsd:string</span></span>  <br/> |<span data-ttu-id="76595-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="76595-126">optional</span></span>  <br/> ||<span data-ttu-id="76595-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="76595-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="76595-128">F</span><span class="sxs-lookup"><span data-stu-id="76595-128">F</span></span>  <br/> |<span data-ttu-id="76595-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="76595-129">xsd:string</span></span>  <br/> |<span data-ttu-id="76595-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="76595-130">optional</span></span>  <br/> ||<span data-ttu-id="76595-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="76595-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="76595-132">N</span><span class="sxs-lookup"><span data-stu-id="76595-132">N</span></span>  <br/> |<span data-ttu-id="76595-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="76595-133">xsd:string</span></span>  <br/> |<span data-ttu-id="76595-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="76595-134">required</span></span>  <br/> ||<span data-ttu-id="76595-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="76595-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="76595-136">U</span><span class="sxs-lookup"><span data-stu-id="76595-136">U</span></span>  <br/> |<span data-ttu-id="76595-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="76595-137">xsd:string</span></span>  <br/> |<span data-ttu-id="76595-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="76595-138">optional</span></span>  <br/> ||<span data-ttu-id="76595-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="76595-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="76595-140">V</span><span class="sxs-lookup"><span data-stu-id="76595-140">V</span></span>  <br/> |<span data-ttu-id="76595-141">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="76595-141">xsd:string</span></span>  <br/> |<span data-ttu-id="76595-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="76595-142">optional</span></span>  <br/> ||<span data-ttu-id="76595-143">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="76595-143">Values of the xsd:string type.</span></span>  <br/> |
   

