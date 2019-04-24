---
title: Элемент Публишедпаже (Публишсеттингс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Указывает, будет ли страница документа видна в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: 313cabbdd59930df67c807ee3c89df1a6e8c17a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326798"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="728c0-103">Элемент Публишедпаже (Публишсеттингс_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="728c0-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="728c0-104">Указывает, будет ли страница документа видна в браузере с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="728c0-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="728c0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="728c0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="728c0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="728c0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="728c0-107">Публишедпаже_типе</span><span class="sxs-lookup"><span data-stu-id="728c0-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="728c0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="728c0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="728c0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="728c0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="728c0-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="728c0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="728c0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="728c0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="728c0-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="728c0-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="728c0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="728c0-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="728c0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="728c0-114">Elements and attributes</span></span>

<span data-ttu-id="728c0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="728c0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="728c0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="728c0-116">Parent elements</span></span>

|<span data-ttu-id="728c0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="728c0-117">**Element**</span></span>|<span data-ttu-id="728c0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="728c0-118">**Type**</span></span>|<span data-ttu-id="728c0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="728c0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="728c0-120">Публишсеттингс</span><span class="sxs-lookup"><span data-stu-id="728c0-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="728c0-121">Публишсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="728c0-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="728c0-122">Задает параметры, которые используются при открытии схемы с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="728c0-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="728c0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="728c0-123">Child elements</span></span>

<span data-ttu-id="728c0-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="728c0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="728c0-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="728c0-125">Attributes</span></span>

|<span data-ttu-id="728c0-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="728c0-126">**Attribute**</span></span>|<span data-ttu-id="728c0-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="728c0-127">**Type**</span></span>|<span data-ttu-id="728c0-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="728c0-128">**Required**</span></span>|<span data-ttu-id="728c0-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="728c0-129">**Description**</span></span>|<span data-ttu-id="728c0-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="728c0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="728c0-131">ИД</span><span class="sxs-lookup"><span data-stu-id="728c0-131">ID</span></span>  <br/> |<span data-ttu-id="728c0-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="728c0-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="728c0-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="728c0-133">required</span></span>  <br/> |<span data-ttu-id="728c0-134">Идентификатор страницы документа.</span><span class="sxs-lookup"><span data-stu-id="728c0-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="728c0-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="728c0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

