---
title: Сектион_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 48dd7a0ffc487b4a7a4200505f08d0aca42fd3c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542130"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="29bf2-102">Сектион_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="29bf2-102">Section_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="29bf2-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="29bf2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29bf2-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="29bf2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="29bf2-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="29bf2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="29bf2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="29bf2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="29bf2-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="29bf2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="29bf2-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="29bf2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29bf2-109">Определение</span><span class="sxs-lookup"><span data-stu-id="29bf2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="29bf2-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="29bf2-110">Elements and attributes</span></span>

<span data-ttu-id="29bf2-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="29bf2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="29bf2-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="29bf2-112">Child elements</span></span>

|<span data-ttu-id="29bf2-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="29bf2-113">**Element**</span></span>|<span data-ttu-id="29bf2-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29bf2-114">**Type**</span></span>|<span data-ttu-id="29bf2-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29bf2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29bf2-116">Cell</span><span class="sxs-lookup"><span data-stu-id="29bf2-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="29bf2-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="29bf2-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="29bf2-118">Row</span><span class="sxs-lookup"><span data-stu-id="29bf2-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="29bf2-119">Ров_типе</span><span class="sxs-lookup"><span data-stu-id="29bf2-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="29bf2-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="29bf2-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="29bf2-121">Тригжер_типе</span><span class="sxs-lookup"><span data-stu-id="29bf2-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="29bf2-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="29bf2-122">Attributes</span></span>

|<span data-ttu-id="29bf2-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="29bf2-123">**Attribute**</span></span>|<span data-ttu-id="29bf2-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29bf2-124">**Type**</span></span>|<span data-ttu-id="29bf2-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="29bf2-125">**Required**</span></span>|<span data-ttu-id="29bf2-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29bf2-126">**Description**</span></span>|<span data-ttu-id="29bf2-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="29bf2-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29bf2-128">Del</span><span class="sxs-lookup"><span data-stu-id="29bf2-128">Del</span></span>  <br/> |<span data-ttu-id="29bf2-129">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="29bf2-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29bf2-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="29bf2-130">optional</span></span>  <br/> ||<span data-ttu-id="29bf2-131">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="29bf2-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29bf2-132">IX</span><span class="sxs-lookup"><span data-stu-id="29bf2-132">IX</span></span>  <br/> |<span data-ttu-id="29bf2-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="29bf2-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29bf2-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="29bf2-134">optional</span></span>  <br/> ||<span data-ttu-id="29bf2-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="29bf2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29bf2-136">N</span><span class="sxs-lookup"><span data-stu-id="29bf2-136">N</span></span>  <br/> |<span data-ttu-id="29bf2-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="29bf2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="29bf2-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29bf2-138">required</span></span>  <br/> ||<span data-ttu-id="29bf2-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="29bf2-139">Values of the xsd:string type.</span></span>  <br/> |
   

