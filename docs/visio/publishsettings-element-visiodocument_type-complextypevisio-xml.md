---
title: Элемент PublishSettings (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, используемые при открытии диаграммы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397214"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="4ed45-103">Элемент PublishSettings (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4ed45-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4ed45-104">Задает параметры, используемые при открытии диаграммы с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4ed45-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ed45-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4ed45-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ed45-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4ed45-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4ed45-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4ed45-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4ed45-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4ed45-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4ed45-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4ed45-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4ed45-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4ed45-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4ed45-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4ed45-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4ed45-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="4ed45-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ed45-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4ed45-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4ed45-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4ed45-114">Elements and attributes</span></span>

<span data-ttu-id="4ed45-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4ed45-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4ed45-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4ed45-116">Parent elements</span></span>

|<span data-ttu-id="4ed45-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4ed45-117">**Element**</span></span>|<span data-ttu-id="4ed45-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4ed45-118">**Type**</span></span>|<span data-ttu-id="4ed45-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ed45-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ed45-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4ed45-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4ed45-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4ed45-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4ed45-122">Задает свойства документа.</span><span class="sxs-lookup"><span data-stu-id="4ed45-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ed45-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4ed45-123">Child elements</span></span>

|<span data-ttu-id="4ed45-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4ed45-124">**Element**</span></span>|<span data-ttu-id="4ed45-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4ed45-125">**Type**</span></span>|<span data-ttu-id="4ed45-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ed45-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ed45-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="4ed45-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ed45-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="4ed45-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4ed45-129">Указывает, является ли страницу документа для просмотра в браузере с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="4ed45-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="4ed45-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="4ed45-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4ed45-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="4ed45-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4ed45-132">Указывает, является ли набор записей обновляемый, с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="4ed45-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4ed45-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4ed45-133">Attributes</span></span>

<span data-ttu-id="4ed45-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="4ed45-134">None.</span></span>
  

