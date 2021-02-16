---
title: Элемент PublishSettings (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Указывает параметры, используемые при открытие схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541360"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="96426-103">Элемент PublishSettings (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="96426-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="96426-104">Указывает параметры, используемые при открытие схемы с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="96426-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96426-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="96426-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96426-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="96426-106">**Element type**</span></span> <br/> |[<span data-ttu-id="96426-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="96426-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="96426-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="96426-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="96426-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="96426-109">**Schema file**</span></span> <br/> |<span data-ttu-id="96426-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="96426-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="96426-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="96426-111">**Document parts**</span></span> <br/> |<span data-ttu-id="96426-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="96426-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96426-113">Определение</span><span class="sxs-lookup"><span data-stu-id="96426-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="96426-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="96426-114">Elements and attributes</span></span>

<span data-ttu-id="96426-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="96426-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="96426-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="96426-116">Parent elements</span></span>

|<span data-ttu-id="96426-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="96426-117">**Element**</span></span>|<span data-ttu-id="96426-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="96426-118">**Type**</span></span>|<span data-ttu-id="96426-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96426-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96426-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="96426-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="96426-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="96426-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96426-122">Указывает свойства рисунка.</span><span class="sxs-lookup"><span data-stu-id="96426-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="96426-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="96426-123">Child elements</span></span>

|<span data-ttu-id="96426-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="96426-124">**Element**</span></span>|<span data-ttu-id="96426-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="96426-125">**Type**</span></span>|<span data-ttu-id="96426-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96426-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96426-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="96426-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96426-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="96426-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96426-129">Указывает, можно ли просматривать страницу рисования в браузере с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="96426-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="96426-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="96426-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96426-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="96426-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96426-132">Указывает, можно ли обновлять набор записей с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="96426-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="96426-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="96426-133">Attributes</span></span>

<span data-ttu-id="96426-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="96426-134">None.</span></span>
  

