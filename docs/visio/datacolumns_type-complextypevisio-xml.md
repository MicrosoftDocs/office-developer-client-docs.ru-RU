---
title: Датаколумнс_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: ffe0fbfeaf0b0b67386a6cadd1beb78058819d39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541150"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="46715-102">Датаколумнс_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="46715-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="46715-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="46715-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46715-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="46715-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="46715-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="46715-105">**Schema file**</span></span> <br/> |<span data-ttu-id="46715-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="46715-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="46715-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="46715-107">**Extension base**</span></span> <br/> |<span data-ttu-id="46715-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="46715-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46715-109">Определение</span><span class="sxs-lookup"><span data-stu-id="46715-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46715-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="46715-110">Elements and attributes</span></span>

<span data-ttu-id="46715-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="46715-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="46715-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46715-112">Child elements</span></span>

|<span data-ttu-id="46715-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="46715-113">**Element**</span></span>|<span data-ttu-id="46715-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46715-114">**Type**</span></span>|<span data-ttu-id="46715-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46715-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46715-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="46715-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46715-117">Датаколумн_типе</span><span class="sxs-lookup"><span data-stu-id="46715-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="46715-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="46715-118">Attributes</span></span>

|<span data-ttu-id="46715-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="46715-119">**Attribute**</span></span>|<span data-ttu-id="46715-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46715-120">**Type**</span></span>|<span data-ttu-id="46715-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="46715-121">**Required**</span></span>|<span data-ttu-id="46715-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46715-122">**Description**</span></span>|<span data-ttu-id="46715-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="46715-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="46715-124">Сортаск</span><span class="sxs-lookup"><span data-stu-id="46715-124">SortAsc</span></span>  <br/> |<span data-ttu-id="46715-125">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="46715-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="46715-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="46715-126">optional</span></span>  <br/> ||<span data-ttu-id="46715-127">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="46715-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="46715-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="46715-128">SortColumn</span></span>  <br/> |<span data-ttu-id="46715-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="46715-129">xsd:string</span></span>  <br/> |<span data-ttu-id="46715-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="46715-130">optional</span></span>  <br/> ||<span data-ttu-id="46715-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="46715-131">Values of the xsd:string type.</span></span>  <br/> |
   

