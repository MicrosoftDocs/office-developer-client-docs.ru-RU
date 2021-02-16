---
title: DataColumns_Type complexType (Visio XML)
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
# <a name="datacolumns_type-complextype-visio-xml"></a><span data-ttu-id="6f927-102">DataColumns_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6f927-102">DataColumns_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6f927-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6f927-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f927-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6f927-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6f927-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6f927-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6f927-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6f927-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6f927-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6f927-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6f927-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="6f927-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f927-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6f927-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6f927-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6f927-110">Elements and attributes</span></span>

<span data-ttu-id="6f927-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6f927-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6f927-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6f927-112">Child elements</span></span>

|<span data-ttu-id="6f927-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6f927-113">**Element**</span></span>|<span data-ttu-id="6f927-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6f927-114">**Type**</span></span>|<span data-ttu-id="6f927-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f927-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6f927-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="6f927-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6f927-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="6f927-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6f927-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6f927-118">Attributes</span></span>

|<span data-ttu-id="6f927-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6f927-119">**Attribute**</span></span>|<span data-ttu-id="6f927-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6f927-120">**Type**</span></span>|<span data-ttu-id="6f927-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6f927-121">**Required**</span></span>|<span data-ttu-id="6f927-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f927-122">**Description**</span></span>|<span data-ttu-id="6f927-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6f927-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6f927-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="6f927-124">SortAsc</span></span>  <br/> |<span data-ttu-id="6f927-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6f927-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6f927-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="6f927-126">optional</span></span>  <br/> ||<span data-ttu-id="6f927-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6f927-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6f927-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="6f927-128">SortColumn</span></span>  <br/> |<span data-ttu-id="6f927-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6f927-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6f927-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="6f927-130">optional</span></span>  <br/> ||<span data-ttu-id="6f927-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6f927-131">Values of the xsd:string type.</span></span>  <br/> |
   

