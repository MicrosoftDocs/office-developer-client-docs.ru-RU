---
title: Элемент PublishedPage (PublishSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Указывает, является ли страницу документа для просмотра в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 5cdbb03aaac3393c16c6ed0169842153374f668e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814505"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="b301a-103">Элемент PublishedPage (PublishSettings_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b301a-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b301a-104">Указывает, является ли страницу документа для просмотра в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b301a-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b301a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b301a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b301a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b301a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b301a-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="b301a-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b301a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b301a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b301a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b301a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b301a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b301a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b301a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b301a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b301a-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="b301a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b301a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b301a-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b301a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b301a-114">Elements and attributes</span></span>

<span data-ttu-id="b301a-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="b301a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b301a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b301a-116">Parent elements</span></span>

|<span data-ttu-id="b301a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b301a-117">**Element**</span></span>|<span data-ttu-id="b301a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b301a-118">**Type**</span></span>|<span data-ttu-id="b301a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b301a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b301a-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="b301a-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b301a-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b301a-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b301a-122">Задает параметры, используемые при открытии диаграммы с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="b301a-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b301a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b301a-123">Child elements</span></span>

<span data-ttu-id="b301a-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b301a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b301a-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b301a-125">Attributes</span></span>

|<span data-ttu-id="b301a-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b301a-126">**Attribute**</span></span>|<span data-ttu-id="b301a-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b301a-127">**Type**</span></span>|<span data-ttu-id="b301a-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="b301a-128">**Required**</span></span>|<span data-ttu-id="b301a-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b301a-129">**Description**</span></span>|<span data-ttu-id="b301a-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b301a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b301a-131">ID</span><span class="sxs-lookup"><span data-stu-id="b301a-131">ID</span></span>  <br/> |<span data-ttu-id="b301a-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b301a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b301a-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b301a-133">required</span></span>  <br/> |<span data-ttu-id="b301a-134">Идентификатор страницы рисунка.</span><span class="sxs-lookup"><span data-stu-id="b301a-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="b301a-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b301a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

