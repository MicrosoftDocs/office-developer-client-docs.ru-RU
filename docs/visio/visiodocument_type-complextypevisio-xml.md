---
title: VisioDocument_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5003f98e-4fed-73f8-be55-5b068d9cbffe
ms.openlocfilehash: f56ec2f09ebd14683952c70b62f84cffb97f2e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815160"
---
# <a name="visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ee4fb-102">VisioDocument_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ee4fb-102">VisioDocument_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ee4fb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ee4fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee4fb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ee4fb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ee4fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ee4fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ee4fb-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ee4fb-108">Нет</span><span class="sxs-lookup"><span data-stu-id="ee4fb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ee4fb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ee4fb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ee4fb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee4fb-110">Elements and attributes</span></span>

<span data-ttu-id="ee4fb-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ee4fb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ee4fb-112">Child elements</span></span>

|<span data-ttu-id="ee4fb-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-113">**Element**</span></span>|<span data-ttu-id="ee4fb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-114">**Type**</span></span>|<span data-ttu-id="ee4fb-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee4fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ee4fb-116">Цвета</span><span class="sxs-lookup"><span data-stu-id="ee4fb-116">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-117">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-117">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-118">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="ee4fb-118">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-119">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-119">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-120">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="ee4fb-120">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-121">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-121">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-122">EventList</span><span class="sxs-lookup"><span data-stu-id="ee4fb-122">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-123">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-123">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-124">FaceNames</span><span class="sxs-lookup"><span data-stu-id="ee4fb-124">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-125">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-125">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-126">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="ee4fb-126">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-127">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-127">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-128">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="ee4fb-128">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-129">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-129">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee4fb-130">Таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="ee4fb-130">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee4fb-131">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="ee4fb-131">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ee4fb-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee4fb-132">Attributes</span></span>

<span data-ttu-id="ee4fb-133">Нет.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-133">None.</span></span>
  

