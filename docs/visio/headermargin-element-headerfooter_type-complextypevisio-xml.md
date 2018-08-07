---
title: Элемент HeaderMargin (HeaderFooter_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: Задает поле заголовка документа.
ms.openlocfilehash: a0accb08fd2c781e112b7b54e074dccd4c4e4307
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813894"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="75181-103">Элемент HeaderMargin (HeaderFooter_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="75181-103">HeaderMargin element (HeaderFooter_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="75181-104">Задает поле заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="75181-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75181-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="75181-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75181-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="75181-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75181-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="75181-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75181-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="75181-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75181-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="75181-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75181-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="75181-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75181-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="75181-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75181-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="75181-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75181-113">Определение</span><span class="sxs-lookup"><span data-stu-id="75181-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75181-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="75181-114">Elements and attributes</span></span>

<span data-ttu-id="75181-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="75181-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75181-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="75181-116">Parent elements</span></span>

|<span data-ttu-id="75181-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="75181-117">**Element**</span></span>|<span data-ttu-id="75181-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="75181-118">**Type**</span></span>|<span data-ttu-id="75181-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75181-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75181-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="75181-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75181-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="75181-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75181-122">Содержит элементы для колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="75181-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="75181-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="75181-123">Child elements</span></span>

<span data-ttu-id="75181-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="75181-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75181-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="75181-125">Attributes</span></span>

|<span data-ttu-id="75181-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="75181-126">**Attribute**</span></span>|<span data-ttu-id="75181-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="75181-127">**Type**</span></span>|<span data-ttu-id="75181-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="75181-128">**Required**</span></span>|<span data-ttu-id="75181-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75181-129">**Description**</span></span>|<span data-ttu-id="75181-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="75181-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75181-131">Подразделения</span><span class="sxs-lookup"><span data-stu-id="75181-131">Unit</span></span>  <br/> |<span data-ttu-id="75181-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="75181-132">xsd:string</span></span>  <br/> |<span data-ttu-id="75181-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="75181-133">optional</span></span>  <br/> |<span data-ttu-id="75181-134">Представляет единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="75181-134">Represents a unit of measure.</span></span> <span data-ttu-id="75181-135">Значение по умолчанию — DP.</span><span class="sxs-lookup"><span data-stu-id="75181-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="75181-136">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="75181-136">Values of the xsd:string type.</span></span>  <br/> |
   

