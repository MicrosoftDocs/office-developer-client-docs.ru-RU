---
title: VisioDocument_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: 3b794f4e7843b89dda2c23216478bc1b72f8753a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389850"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="13430-102">VisioDocument_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="13430-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="13430-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="13430-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13430-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="13430-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="13430-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="13430-105">**Schema file**</span></span> <br/> |<span data-ttu-id="13430-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="13430-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="13430-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="13430-107">**Extension base**</span></span> <br/> |<span data-ttu-id="13430-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="13430-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13430-109">Определение</span><span class="sxs-lookup"><span data-stu-id="13430-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="13430-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="13430-110">Elements and attributes</span></span>

<span data-ttu-id="13430-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="13430-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="13430-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="13430-112">Child elements</span></span>

|<span data-ttu-id="13430-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="13430-113">**Element**</span></span>|<span data-ttu-id="13430-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="13430-114">**Type**</span></span>|<span data-ttu-id="13430-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13430-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13430-116">цвета;</span><span class="sxs-lookup"><span data-stu-id="13430-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="13430-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="13430-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="13430-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="13430-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="13430-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-122">EventList</span><span class="sxs-lookup"><span data-stu-id="13430-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="13430-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="13430-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="13430-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="13430-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="13430-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="13430-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="13430-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="13430-130">Таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="13430-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13430-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="13430-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="13430-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="13430-132">Attributes</span></span>

<span data-ttu-id="13430-133">Нет.</span><span class="sxs-lookup"><span data-stu-id="13430-133">None.</span></span>
  

