---
title: Сектиондеф_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326077"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="7ac40-102">Сектиондеф_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7ac40-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7ac40-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7ac40-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ac40-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7ac40-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7ac40-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7ac40-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7ac40-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7ac40-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7ac40-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7ac40-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7ac40-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7ac40-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ac40-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7ac40-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7ac40-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ac40-110">Elements and attributes</span></span>

<span data-ttu-id="7ac40-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7ac40-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7ac40-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7ac40-112">Child elements</span></span>

|<span data-ttu-id="7ac40-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7ac40-113">**Element**</span></span>|<span data-ttu-id="7ac40-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ac40-114">**Type**</span></span>|<span data-ttu-id="7ac40-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ac40-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ac40-116">Целлдеф</span><span class="sxs-lookup"><span data-stu-id="7ac40-116">CellDef</span></span> <br/> |[<span data-ttu-id="7ac40-117">Целлдеф_типе</span><span class="sxs-lookup"><span data-stu-id="7ac40-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="7ac40-118">Ровдеф</span><span class="sxs-lookup"><span data-stu-id="7ac40-118">RowDef</span></span> <br/> |[<span data-ttu-id="7ac40-119">Ровдеф_типе</span><span class="sxs-lookup"><span data-stu-id="7ac40-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7ac40-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ac40-120">Attributes</span></span>

|<span data-ttu-id="7ac40-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7ac40-121">**Attribute**</span></span>|<span data-ttu-id="7ac40-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ac40-122">**Type**</span></span>|<span data-ttu-id="7ac40-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7ac40-123">**Required**</span></span>|<span data-ttu-id="7ac40-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ac40-124">**Description**</span></span>|<span data-ttu-id="7ac40-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7ac40-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7ac40-126">N</span><span class="sxs-lookup"><span data-stu-id="7ac40-126">N</span></span>  <br/> |<span data-ttu-id="7ac40-127">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7ac40-127">xsd:string</span></span>  <br/> |<span data-ttu-id="7ac40-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ac40-128">required</span></span>  <br/> ||<span data-ttu-id="7ac40-129">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7ac40-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7ac40-130">S</span><span class="sxs-lookup"><span data-stu-id="7ac40-130">S</span></span>  <br/> |<span data-ttu-id="7ac40-131">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="7ac40-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7ac40-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ac40-132">optional</span></span>  <br/> ||<span data-ttu-id="7ac40-133">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="7ac40-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7ac40-134">Д</span><span class="sxs-lookup"><span data-stu-id="7ac40-134">T</span></span>  <br/> |<span data-ttu-id="7ac40-135">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7ac40-135">xsd:string</span></span>  <br/> |<span data-ttu-id="7ac40-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="7ac40-136">optional</span></span>  <br/> ||<span data-ttu-id="7ac40-137">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7ac40-137">Values of the xsd:string type.</span></span>  <br/> |
   

