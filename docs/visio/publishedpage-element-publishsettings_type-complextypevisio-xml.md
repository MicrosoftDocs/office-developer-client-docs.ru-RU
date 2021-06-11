---
title: Элемент PublishedPage (PublishSettings_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Указывает, просматривается ли страница рисования в браузере с Visio служб в Microsoft SharePoint Server 2013 г.
ms.openlocfilehash: 614c01f12b9a7525620704e5417a106e8703c983
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538377"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a><span data-ttu-id="c02d4-103">Элемент PublishedPage (PublishSettings_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c02d4-103">PublishedPage element (PublishSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c02d4-104">Указывает, просматривается ли страница рисования в браузере с Visio служб в Microsoft SharePoint Server 2013 г.</span><span class="sxs-lookup"><span data-stu-id="c02d4-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c02d4-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c02d4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c02d4-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c02d4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c02d4-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="c02d4-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c02d4-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c02d4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c02d4-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c02d4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c02d4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c02d4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c02d4-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c02d4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c02d4-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="c02d4-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c02d4-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c02d4-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c02d4-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c02d4-114">Elements and attributes</span></span>

<span data-ttu-id="c02d4-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c02d4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c02d4-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c02d4-116">Parent elements</span></span>

|<span data-ttu-id="c02d4-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c02d4-117">**Element**</span></span>|<span data-ttu-id="c02d4-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c02d4-118">**Type**</span></span>|<span data-ttu-id="c02d4-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c02d4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c02d4-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="c02d4-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c02d4-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c02d4-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c02d4-122">Указывает параметры, используемые при открываемой схеме с помощью Visio Services.</span><span class="sxs-lookup"><span data-stu-id="c02d4-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c02d4-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c02d4-123">Child elements</span></span>

<span data-ttu-id="c02d4-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="c02d4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c02d4-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c02d4-125">Attributes</span></span>

|<span data-ttu-id="c02d4-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c02d4-126">**Attribute**</span></span>|<span data-ttu-id="c02d4-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c02d4-127">**Type**</span></span>|<span data-ttu-id="c02d4-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c02d4-128">**Required**</span></span>|<span data-ttu-id="c02d4-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c02d4-129">**Description**</span></span>|<span data-ttu-id="c02d4-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c02d4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c02d4-131">ID</span><span class="sxs-lookup"><span data-stu-id="c02d4-131">ID</span></span>  <br/> |<span data-ttu-id="c02d4-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c02d4-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c02d4-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c02d4-133">required</span></span>  <br/> |<span data-ttu-id="c02d4-134">Идентификатор страницы рисования.</span><span class="sxs-lookup"><span data-stu-id="c02d4-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="c02d4-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c02d4-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

