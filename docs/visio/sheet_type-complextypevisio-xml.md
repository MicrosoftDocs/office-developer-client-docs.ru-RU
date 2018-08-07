---
title: Sheet_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814836"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="d9f44-102">Sheet_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d9f44-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d9f44-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d9f44-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9f44-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d9f44-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d9f44-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d9f44-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d9f44-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d9f44-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d9f44-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d9f44-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d9f44-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d9f44-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9f44-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d9f44-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d9f44-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d9f44-110">Elements and attributes</span></span>

<span data-ttu-id="d9f44-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d9f44-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d9f44-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d9f44-112">Child elements</span></span>

|<span data-ttu-id="d9f44-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d9f44-113">**Element**</span></span>|<span data-ttu-id="d9f44-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d9f44-114">**Type**</span></span>|<span data-ttu-id="d9f44-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9f44-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9f44-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d9f44-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="d9f44-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d9f44-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d9f44-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="d9f44-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9f44-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d9f44-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d9f44-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f44-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="d9f44-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="d9f44-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d9f44-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d9f44-122">Attributes</span></span>

|<span data-ttu-id="d9f44-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d9f44-123">**Attribute**</span></span>|<span data-ttu-id="d9f44-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d9f44-124">**Type**</span></span>|<span data-ttu-id="d9f44-125">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d9f44-125">**Required**</span></span>|<span data-ttu-id="d9f44-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9f44-126">**Description**</span></span>|<span data-ttu-id="d9f44-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d9f44-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d9f44-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="d9f44-128">FillStyle</span></span>  <br/> |<span data-ttu-id="d9f44-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9f44-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9f44-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="d9f44-130">optional</span></span>  <br/> ||<span data-ttu-id="d9f44-131">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9f44-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9f44-132">Стиль линии</span><span class="sxs-lookup"><span data-stu-id="d9f44-132">LineStyle</span></span>  <br/> |<span data-ttu-id="d9f44-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9f44-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9f44-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="d9f44-134">optional</span></span>  <br/> ||<span data-ttu-id="d9f44-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9f44-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9f44-136">Стиля текста</span><span class="sxs-lookup"><span data-stu-id="d9f44-136">TextStyle</span></span>  <br/> |<span data-ttu-id="d9f44-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9f44-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9f44-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d9f44-138">optional</span></span>  <br/> ||<span data-ttu-id="d9f44-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9f44-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

