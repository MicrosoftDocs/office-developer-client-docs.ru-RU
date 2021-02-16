---
title: Элемент FooterMargin (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 047f42cf-4202-50bd-40b4-a71052e2dfb3
description: Указывает поле для footer документа.
ms.openlocfilehash: 5a147dbb8b94d9077836cb2269dd2ff72dae3b3a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538664"
---
# <a name="footermargin-element-headerfooter_type-complextype-visio-xml"></a><span data-ttu-id="5cf92-103">Элемент FooterMargin (HeaderFooter_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5cf92-103">FooterMargin element (HeaderFooter_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5cf92-104">Указывает поле для footer документа.</span><span class="sxs-lookup"><span data-stu-id="5cf92-104">Specifies the margin of a document's footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cf92-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5cf92-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cf92-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5cf92-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5cf92-107">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="5cf92-107">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5cf92-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5cf92-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5cf92-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5cf92-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5cf92-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5cf92-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5cf92-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5cf92-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5cf92-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="5cf92-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5cf92-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5cf92-113">Definition</span></span>

```XML
< xs:element name="FooterMargin" type="FooterMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5cf92-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5cf92-114">Elements and attributes</span></span>

<span data-ttu-id="5cf92-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5cf92-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5cf92-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5cf92-116">Parent elements</span></span>

|<span data-ttu-id="5cf92-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5cf92-117">**Element**</span></span>|<span data-ttu-id="5cf92-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5cf92-118">**Type**</span></span>|<span data-ttu-id="5cf92-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cf92-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5cf92-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="5cf92-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5cf92-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="5cf92-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5cf92-122">Содержит элементы для опорного и footer-элементов документа.</span><span class="sxs-lookup"><span data-stu-id="5cf92-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5cf92-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5cf92-123">Child elements</span></span>

<span data-ttu-id="5cf92-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="5cf92-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cf92-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5cf92-125">Attributes</span></span>

|<span data-ttu-id="5cf92-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5cf92-126">**Attribute**</span></span>|<span data-ttu-id="5cf92-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5cf92-127">**Type**</span></span>|<span data-ttu-id="5cf92-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5cf92-128">**Required**</span></span>|<span data-ttu-id="5cf92-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cf92-129">**Description**</span></span>|<span data-ttu-id="5cf92-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5cf92-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5cf92-131">Unit</span><span class="sxs-lookup"><span data-stu-id="5cf92-131">Unit</span></span>  <br/> |<span data-ttu-id="5cf92-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5cf92-132">xsd:string</span></span>  <br/> |<span data-ttu-id="5cf92-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="5cf92-133">optional</span></span>  <br/> |<span data-ttu-id="5cf92-134">Представляет единицу измерения.</span><span class="sxs-lookup"><span data-stu-id="5cf92-134">Represents a unit of measure.</span></span> <span data-ttu-id="5cf92-135">Значение по умолчанию — IN.</span><span class="sxs-lookup"><span data-stu-id="5cf92-135">The default is IN.</span></span>  <br/> |<span data-ttu-id="5cf92-136">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="5cf92-136">Values of the xsd:string type.</span></span>  <br/> |
   

