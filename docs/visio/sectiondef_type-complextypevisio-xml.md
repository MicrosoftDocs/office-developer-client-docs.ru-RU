---
title: SectionDef_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814739"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="f4b00-102">SectionDef_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f4b00-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f4b00-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f4b00-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4b00-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f4b00-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f4b00-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f4b00-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f4b00-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f4b00-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f4b00-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="f4b00-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f4b00-108">Нет</span><span class="sxs-lookup"><span data-stu-id="f4b00-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4b00-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f4b00-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4b00-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f4b00-110">Elements and attributes</span></span>

<span data-ttu-id="f4b00-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f4b00-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f4b00-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f4b00-112">Child elements</span></span>

|<span data-ttu-id="f4b00-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f4b00-113">**Element**</span></span>|<span data-ttu-id="f4b00-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f4b00-114">**Type**</span></span>|<span data-ttu-id="f4b00-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f4b00-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4b00-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="f4b00-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f4b00-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="f4b00-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f4b00-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="f4b00-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f4b00-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="f4b00-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f4b00-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f4b00-120">Attributes</span></span>

|<span data-ttu-id="f4b00-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f4b00-121">**Attribute**</span></span>|<span data-ttu-id="f4b00-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f4b00-122">**Type**</span></span>|<span data-ttu-id="f4b00-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="f4b00-123">**Required**</span></span>|<span data-ttu-id="f4b00-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f4b00-124">**Description**</span></span>|<span data-ttu-id="f4b00-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f4b00-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4b00-126">N</span><span class="sxs-lookup"><span data-stu-id="f4b00-126">N</span></span>  <br/> |<span data-ttu-id="f4b00-127">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f4b00-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f4b00-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f4b00-128">required</span></span>  <br/> ||<span data-ttu-id="f4b00-129">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f4b00-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f4b00-130">s</span><span class="sxs-lookup"><span data-stu-id="f4b00-130">S</span></span>  <br/> |<span data-ttu-id="f4b00-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f4b00-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="f4b00-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="f4b00-132">optional</span></span>  <br/> ||<span data-ttu-id="f4b00-133">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="f4b00-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="f4b00-134">T</span><span class="sxs-lookup"><span data-stu-id="f4b00-134">T</span></span>  <br/> |<span data-ttu-id="f4b00-135">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f4b00-135">xsd:string</span></span>  <br/> |<span data-ttu-id="f4b00-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="f4b00-136">optional</span></span>  <br/> ||<span data-ttu-id="f4b00-137">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f4b00-137">Values of the xsd:string type.</span></span>  <br/> |
   

