---
title: Sheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388751"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="075cb-102">Sheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="075cb-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="075cb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="075cb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="075cb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="075cb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="075cb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="075cb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="075cb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="075cb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="075cb-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="075cb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="075cb-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="075cb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="075cb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="075cb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="075cb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="075cb-110">Elements and attributes</span></span>

<span data-ttu-id="075cb-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="075cb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="075cb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="075cb-112">Child elements</span></span>

|<span data-ttu-id="075cb-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="075cb-113">**Element**</span></span>|<span data-ttu-id="075cb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="075cb-114">**Type**</span></span>|<span data-ttu-id="075cb-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="075cb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="075cb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="075cb-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="075cb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="075cb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="075cb-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="075cb-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="075cb-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="075cb-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="075cb-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="075cb-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="075cb-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="075cb-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="075cb-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="075cb-122">Attributes</span></span>

|<span data-ttu-id="075cb-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="075cb-123">**Attribute**</span></span>|<span data-ttu-id="075cb-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="075cb-124">**Type**</span></span>|<span data-ttu-id="075cb-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="075cb-125">**Required**</span></span>|<span data-ttu-id="075cb-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="075cb-126">**Description**</span></span>|<span data-ttu-id="075cb-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="075cb-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="075cb-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="075cb-128">FillStyle</span></span>  <br/> |<span data-ttu-id="075cb-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="075cb-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="075cb-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="075cb-130">optional</span></span>  <br/> ||<span data-ttu-id="075cb-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="075cb-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="075cb-132">Стиль линии</span><span class="sxs-lookup"><span data-stu-id="075cb-132">LineStyle</span></span>  <br/> |<span data-ttu-id="075cb-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="075cb-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="075cb-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="075cb-134">optional</span></span>  <br/> ||<span data-ttu-id="075cb-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="075cb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="075cb-136">Стиля текста</span><span class="sxs-lookup"><span data-stu-id="075cb-136">TextStyle</span></span>  <br/> |<span data-ttu-id="075cb-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="075cb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="075cb-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="075cb-138">optional</span></span>  <br/> ||<span data-ttu-id="075cb-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="075cb-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

