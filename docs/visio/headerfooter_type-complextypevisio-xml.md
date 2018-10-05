---
title: HeaderFooter_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384509"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="7b156-102">HeaderFooter_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7b156-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b156-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7b156-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b156-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7b156-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b156-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7b156-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b156-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b156-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b156-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7b156-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b156-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7b156-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b156-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7b156-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7b156-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b156-110">Elements and attributes</span></span>

<span data-ttu-id="7b156-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7b156-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b156-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7b156-112">Child elements</span></span>

|<span data-ttu-id="7b156-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7b156-113">**Element**</span></span>|<span data-ttu-id="7b156-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7b156-114">**Type**</span></span>|<span data-ttu-id="7b156-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b156-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b156-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="7b156-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="7b156-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="7b156-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="7b156-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="7b156-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="7b156-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="7b156-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="7b156-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7b156-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="7b156-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b156-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="7b156-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7b156-134">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b156-134">Attributes</span></span>

|<span data-ttu-id="7b156-135">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7b156-135">**Attribute**</span></span>|<span data-ttu-id="7b156-136">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7b156-136">**Type**</span></span>|<span data-ttu-id="7b156-137">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7b156-137">**Required**</span></span>|<span data-ttu-id="7b156-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b156-138">**Description**</span></span>|<span data-ttu-id="7b156-139">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7b156-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b156-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="7b156-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="7b156-141">XSD:String</span><span class="sxs-lookup"><span data-stu-id="7b156-141">xsd:string</span></span>  <br/> |<span data-ttu-id="7b156-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="7b156-142">optional</span></span>  <br/> ||<span data-ttu-id="7b156-143">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b156-143">Values of the xsd:string type.</span></span>  <br/> |
   

