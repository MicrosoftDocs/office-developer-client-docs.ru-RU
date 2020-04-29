---
title: Элемент Публишсеттингс (VisioDocument_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 611dfe477228995bca6aedff27b468a2d57e7e85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541360"
---
# <a name="publishsettings-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="b7421-103">Элемент Публишсеттингс (VisioDocument_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b7421-103">PublishSettings element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b7421-104">Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7421-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7421-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7421-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7421-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b7421-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b7421-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="b7421-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b7421-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b7421-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b7421-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b7421-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b7421-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b7421-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b7421-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b7421-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b7421-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="b7421-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7421-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b7421-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7421-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7421-114">Elements and attributes</span></span>

<span data-ttu-id="b7421-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b7421-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b7421-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7421-116">Parent elements</span></span>

|<span data-ttu-id="b7421-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7421-117">**Element**</span></span>|<span data-ttu-id="b7421-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7421-118">**Type**</span></span>|<span data-ttu-id="b7421-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7421-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7421-120">висиодокумент</span><span class="sxs-lookup"><span data-stu-id="b7421-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="b7421-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="b7421-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7421-122">Задает свойства рисунка.</span><span class="sxs-lookup"><span data-stu-id="b7421-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7421-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7421-123">Child elements</span></span>

|<span data-ttu-id="b7421-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7421-124">**Element**</span></span>|<span data-ttu-id="b7421-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7421-125">**Type**</span></span>|<span data-ttu-id="b7421-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7421-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7421-127">публишедпаже</span><span class="sxs-lookup"><span data-stu-id="b7421-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7421-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="b7421-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7421-129">Указывает, будет ли страница документа видна в браузере с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="b7421-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="b7421-130">рефрешабледата</span><span class="sxs-lookup"><span data-stu-id="b7421-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7421-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="b7421-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7421-132">Указывает, следует ли обновлять набор записей с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="b7421-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b7421-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7421-133">Attributes</span></span>

<span data-ttu-id="b7421-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7421-134">None.</span></span>
  

