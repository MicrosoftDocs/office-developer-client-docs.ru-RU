---
title: Элемент Публишсеттингс (Висиодокумент_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 7e926021180d0f32c5e8754fd856081908f4925d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345460"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="23953-103">Элемент Публишсеттингс (Висиодокумент_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="23953-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="23953-104">Задает параметры, которые используются при открытии схемы с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="23953-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23953-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="23953-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23953-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="23953-106">**Element type**</span></span> <br/> |[<span data-ttu-id="23953-107">Публишсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="23953-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="23953-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="23953-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="23953-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="23953-109">**Schema file**</span></span> <br/> |<span data-ttu-id="23953-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="23953-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="23953-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="23953-111">**Document parts**</span></span> <br/> |<span data-ttu-id="23953-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="23953-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="23953-113">Определение</span><span class="sxs-lookup"><span data-stu-id="23953-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="23953-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="23953-114">Elements and attributes</span></span>

<span data-ttu-id="23953-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="23953-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="23953-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="23953-116">Parent elements</span></span>

|<span data-ttu-id="23953-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="23953-117">**Element**</span></span>|<span data-ttu-id="23953-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="23953-118">**Type**</span></span>|<span data-ttu-id="23953-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23953-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23953-120">Висиодокумент</span><span class="sxs-lookup"><span data-stu-id="23953-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="23953-121">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="23953-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="23953-122">Задает свойства рисунка.</span><span class="sxs-lookup"><span data-stu-id="23953-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="23953-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="23953-123">Child elements</span></span>

|<span data-ttu-id="23953-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="23953-124">**Element**</span></span>|<span data-ttu-id="23953-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="23953-125">**Type**</span></span>|<span data-ttu-id="23953-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23953-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="23953-127">Публишедпаже</span><span class="sxs-lookup"><span data-stu-id="23953-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23953-128">Публишедпаже_типе</span><span class="sxs-lookup"><span data-stu-id="23953-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="23953-129">Указывает, будет ли страница документа видна в браузере с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="23953-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="23953-130">Рефрешабледата</span><span class="sxs-lookup"><span data-stu-id="23953-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="23953-131">Рефрешабледата_типе</span><span class="sxs-lookup"><span data-stu-id="23953-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="23953-132">Указывает, следует ли обновлять набор записей с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="23953-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="23953-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="23953-133">Attributes</span></span>

<span data-ttu-id="23953-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="23953-134">None.</span></span>
  

