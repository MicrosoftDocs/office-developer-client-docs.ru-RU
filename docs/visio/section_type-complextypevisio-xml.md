---
title: Сектион_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326098"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="d74b1-102">Сектион_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d74b1-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d74b1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d74b1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d74b1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d74b1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d74b1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d74b1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d74b1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d74b1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d74b1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="d74b1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d74b1-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="d74b1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d74b1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d74b1-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
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
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d74b1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d74b1-110">Elements and attributes</span></span>

<span data-ttu-id="d74b1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d74b1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d74b1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d74b1-112">Child elements</span></span>

|<span data-ttu-id="d74b1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d74b1-113">**Element**</span></span>|<span data-ttu-id="d74b1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d74b1-114">**Type**</span></span>|<span data-ttu-id="d74b1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d74b1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d74b1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d74b1-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="d74b1-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="d74b1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d74b1-118">Row</span><span class="sxs-lookup"><span data-stu-id="d74b1-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d74b1-119">Ров_типе</span><span class="sxs-lookup"><span data-stu-id="d74b1-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d74b1-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="d74b1-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="d74b1-121">Тригжер_типе</span><span class="sxs-lookup"><span data-stu-id="d74b1-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d74b1-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d74b1-122">Attributes</span></span>

|<span data-ttu-id="d74b1-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d74b1-123">**Attribute**</span></span>|<span data-ttu-id="d74b1-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d74b1-124">**Type**</span></span>|<span data-ttu-id="d74b1-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d74b1-125">**Required**</span></span>|<span data-ttu-id="d74b1-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d74b1-126">**Description**</span></span>|<span data-ttu-id="d74b1-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d74b1-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d74b1-128">Del</span><span class="sxs-lookup"><span data-stu-id="d74b1-128">Del</span></span>  <br/> |<span data-ttu-id="d74b1-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="d74b1-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d74b1-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="d74b1-130">optional</span></span>  <br/> ||<span data-ttu-id="d74b1-131">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="d74b1-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d74b1-132">IX</span><span class="sxs-lookup"><span data-stu-id="d74b1-132">IX</span></span>  <br/> |<span data-ttu-id="d74b1-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="d74b1-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d74b1-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="d74b1-134">optional</span></span>  <br/> ||<span data-ttu-id="d74b1-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="d74b1-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d74b1-136">N</span><span class="sxs-lookup"><span data-stu-id="d74b1-136">N</span></span>  <br/> |<span data-ttu-id="d74b1-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d74b1-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d74b1-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d74b1-138">required</span></span>  <br/> ||<span data-ttu-id="d74b1-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="d74b1-139">Values of the xsd:string type.</span></span>  <br/> |
   

