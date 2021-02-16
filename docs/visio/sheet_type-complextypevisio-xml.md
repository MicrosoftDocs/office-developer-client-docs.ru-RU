---
title: Sheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: b747f2257f2b09083b72a17a59856be0a985b270
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540408"
---
# <a name="sheet_type-complextype-visio-xml"></a><span data-ttu-id="eafd5-102">Sheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="eafd5-102">Sheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="eafd5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="eafd5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eafd5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="eafd5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eafd5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="eafd5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eafd5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eafd5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eafd5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="eafd5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eafd5-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="eafd5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eafd5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="eafd5-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
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
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eafd5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="eafd5-110">Elements and attributes</span></span>

<span data-ttu-id="eafd5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="eafd5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eafd5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eafd5-112">Child elements</span></span>

|<span data-ttu-id="eafd5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="eafd5-113">**Element**</span></span>|<span data-ttu-id="eafd5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eafd5-114">**Type**</span></span>|<span data-ttu-id="eafd5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eafd5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eafd5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="eafd5-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="eafd5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="eafd5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="eafd5-118">Section</span><span class="sxs-lookup"><span data-stu-id="eafd5-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eafd5-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="eafd5-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="eafd5-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="eafd5-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="eafd5-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="eafd5-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="eafd5-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eafd5-122">Attributes</span></span>

|<span data-ttu-id="eafd5-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="eafd5-123">**Attribute**</span></span>|<span data-ttu-id="eafd5-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eafd5-124">**Type**</span></span>|<span data-ttu-id="eafd5-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="eafd5-125">**Required**</span></span>|<span data-ttu-id="eafd5-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eafd5-126">**Description**</span></span>|<span data-ttu-id="eafd5-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="eafd5-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eafd5-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="eafd5-128">FillStyle</span></span>  <br/> |<span data-ttu-id="eafd5-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eafd5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eafd5-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="eafd5-130">optional</span></span>  <br/> ||<span data-ttu-id="eafd5-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eafd5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eafd5-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="eafd5-132">LineStyle</span></span>  <br/> |<span data-ttu-id="eafd5-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eafd5-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eafd5-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="eafd5-134">optional</span></span>  <br/> ||<span data-ttu-id="eafd5-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eafd5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eafd5-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="eafd5-136">TextStyle</span></span>  <br/> |<span data-ttu-id="eafd5-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eafd5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eafd5-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="eafd5-138">optional</span></span>  <br/> ||<span data-ttu-id="eafd5-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eafd5-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

