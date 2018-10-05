---
title: Элемент FooterMargin (HeaderFooter_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 047f42cf-4202-50bd-40b4-a71052e2dfb3
description: Задает поле нижнего колонтитула документа.
ms.openlocfilehash: f0c2b8ab1cc7bd1465af3281dfb51766ecba5d8c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401421"
---
# <a name="footermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="39888-103">Элемент FooterMargin (HeaderFooter_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="39888-103">FooterMargin element (HeaderFooter_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="39888-104">Задает поле нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="39888-104">Specifies the margin of a document's footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39888-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="39888-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39888-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="39888-106">**Element type**</span></span> <br/> |[<span data-ttu-id="39888-107">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="39888-107">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="39888-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="39888-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="39888-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="39888-109">**Schema file**</span></span> <br/> |<span data-ttu-id="39888-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="39888-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="39888-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="39888-111">**Document parts**</span></span> <br/> |<span data-ttu-id="39888-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="39888-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39888-113">Определение</span><span class="sxs-lookup"><span data-stu-id="39888-113">Definition</span></span>

```XML
< xs:element name="FooterMargin" type="FooterMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39888-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="39888-114">Elements and attributes</span></span>

<span data-ttu-id="39888-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="39888-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="39888-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="39888-116">Parent elements</span></span>

|<span data-ttu-id="39888-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="39888-117">**Element**</span></span>|<span data-ttu-id="39888-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="39888-118">**Type**</span></span>|<span data-ttu-id="39888-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39888-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39888-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="39888-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="39888-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="39888-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39888-122">Содержит элементы для колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="39888-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39888-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="39888-123">Child elements</span></span>

<span data-ttu-id="39888-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="39888-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39888-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="39888-125">Attributes</span></span>

|<span data-ttu-id="39888-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="39888-126">**Attribute**</span></span>|<span data-ttu-id="39888-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="39888-127">**Type**</span></span>|<span data-ttu-id="39888-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="39888-128">**Required**</span></span>|<span data-ttu-id="39888-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39888-129">**Description**</span></span>|<span data-ttu-id="39888-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="39888-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39888-131">Подразделения</span><span class="sxs-lookup"><span data-stu-id="39888-131">Unit</span></span>  <br/> |<span data-ttu-id="39888-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="39888-132">xsd:string</span></span>  <br/> |<span data-ttu-id="39888-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="39888-133">optional</span></span>  <br/> |<span data-ttu-id="39888-134">Представляет единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="39888-134">Represents a unit of measure.</span></span> <span data-ttu-id="39888-135">Значение по умолчанию — оператора IN.</span><span class="sxs-lookup"><span data-stu-id="39888-135">The default is IN.</span></span>  <br/> |<span data-ttu-id="39888-136">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="39888-136">Values of the xsd:string type.</span></span>  <br/> |
   

