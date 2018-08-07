---
title: HeaderFooter_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 9c567542061ec419de9c4347209059b0486bdf88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813878"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="46b49-102">HeaderFooter_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="46b49-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="46b49-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="46b49-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46b49-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="46b49-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="46b49-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="46b49-105">**Schema file**</span></span> <br/> |<span data-ttu-id="46b49-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="46b49-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="46b49-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="46b49-107">**Extension base**</span></span> <br/> |<span data-ttu-id="46b49-108">Нет</span><span class="sxs-lookup"><span data-stu-id="46b49-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46b49-109">Определение</span><span class="sxs-lookup"><span data-stu-id="46b49-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46b49-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="46b49-110">Elements and attributes</span></span>

<span data-ttu-id="46b49-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="46b49-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="46b49-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46b49-112">Child elements</span></span>

|<span data-ttu-id="46b49-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="46b49-113">**Element**</span></span>|<span data-ttu-id="46b49-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46b49-114">**Type**</span></span>|<span data-ttu-id="46b49-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46b49-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46b49-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="46b49-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="46b49-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="46b49-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="46b49-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="46b49-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="46b49-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="46b49-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="46b49-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="46b49-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="46b49-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46b49-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="46b49-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="46b49-134">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="46b49-134">Attributes</span></span>

|<span data-ttu-id="46b49-135">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="46b49-135">**Attribute**</span></span>|<span data-ttu-id="46b49-136">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46b49-136">**Type**</span></span>|<span data-ttu-id="46b49-137">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="46b49-137">**Required**</span></span>|<span data-ttu-id="46b49-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46b49-138">**Description**</span></span>|<span data-ttu-id="46b49-139">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="46b49-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="46b49-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="46b49-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="46b49-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="46b49-141">xsd:string</span></span>  <br/> |<span data-ttu-id="46b49-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="46b49-142">optional</span></span>  <br/> ||<span data-ttu-id="46b49-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="46b49-143">Values of the xsd:string type.</span></span>  <br/> |
   

