---
title: Висиодокумент_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 3b794f4e7843b89dda2c23216478bc1b72f8753a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285267"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="bf5f4-102">Висиодокумент_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="bf5f4-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bf5f4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf5f4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bf5f4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bf5f4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bf5f4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bf5f4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bf5f4-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="bf5f4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf5f4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bf5f4-109">Definition</span></span>

```XML
          <xs:complexType name="VisioDocument_Type">
          
          <xs:sequence>
    <xs:element name="DocumentSettings"  type="DocumentSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Colors"  type="Colors_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FaceNames"  type="FaceNames_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StyleSheets"  type="StyleSheets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DocumentSheet"  type="DocumentSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="EventList"  type="EventList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooter"  type="HeaderFooter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PublishSettings"  type="PublishSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf5f4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bf5f4-110">Elements and attributes</span></span>

<span data-ttu-id="bf5f4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="bf5f4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bf5f4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bf5f4-112">Child elements</span></span>

|<span data-ttu-id="bf5f4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-113">**Element**</span></span>|<span data-ttu-id="bf5f4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-114">**Type**</span></span>|<span data-ttu-id="bf5f4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf5f4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf5f4-116">Colors</span><span class="sxs-lookup"><span data-stu-id="bf5f4-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-117">Колорс_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-118">Документсеттингс</span><span class="sxs-lookup"><span data-stu-id="bf5f4-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-119">Документсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="bf5f4-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-121">Документшит_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-122">EventList</span><span class="sxs-lookup"><span data-stu-id="bf5f4-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-123">Евентлист_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-124">Фаценамес</span><span class="sxs-lookup"><span data-stu-id="bf5f4-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-125">Фаценамес_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="bf5f4-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-127">Хеадерфутер_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-128">Публишсеттингс</span><span class="sxs-lookup"><span data-stu-id="bf5f4-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-129">Публишсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bf5f4-130">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="bf5f4-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf5f4-131">Стилешитс_типе</span><span class="sxs-lookup"><span data-stu-id="bf5f4-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bf5f4-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bf5f4-132">Attributes</span></span>

<span data-ttu-id="bf5f4-133">Нет.</span><span class="sxs-lookup"><span data-stu-id="bf5f4-133">None.</span></span>
  

