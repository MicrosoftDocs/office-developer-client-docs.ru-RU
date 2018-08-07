---
title: DataColumns_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813535"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="2bd76-102">DataColumns_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2bd76-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2bd76-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2bd76-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bd76-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2bd76-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2bd76-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2bd76-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2bd76-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2bd76-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2bd76-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="2bd76-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2bd76-108">Нет</span><span class="sxs-lookup"><span data-stu-id="2bd76-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2bd76-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2bd76-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2bd76-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2bd76-110">Elements and attributes</span></span>

<span data-ttu-id="2bd76-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="2bd76-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2bd76-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2bd76-112">Child elements</span></span>

|<span data-ttu-id="2bd76-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2bd76-113">**Element**</span></span>|<span data-ttu-id="2bd76-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2bd76-114">**Type**</span></span>|<span data-ttu-id="2bd76-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2bd76-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2bd76-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="2bd76-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2bd76-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="2bd76-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2bd76-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2bd76-118">Attributes</span></span>

|<span data-ttu-id="2bd76-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="2bd76-119">**Attribute**</span></span>|<span data-ttu-id="2bd76-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2bd76-120">**Type**</span></span>|<span data-ttu-id="2bd76-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="2bd76-121">**Required**</span></span>|<span data-ttu-id="2bd76-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2bd76-122">**Description**</span></span>|<span data-ttu-id="2bd76-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="2bd76-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2bd76-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="2bd76-124">SortAsc</span></span>  <br/> |<span data-ttu-id="2bd76-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="2bd76-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2bd76-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="2bd76-126">optional</span></span>  <br/> ||<span data-ttu-id="2bd76-127">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2bd76-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2bd76-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="2bd76-128">SortColumn</span></span>  <br/> |<span data-ttu-id="2bd76-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2bd76-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2bd76-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="2bd76-130">optional</span></span>  <br/> ||<span data-ttu-id="2bd76-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2bd76-131">Values of the xsd:string type.</span></span>  <br/> |
   

