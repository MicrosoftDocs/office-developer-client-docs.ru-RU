---
title: Элемент Рефрешабледата (Публишсеттингс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Указывает, следует ли обновлять набор записей с помощью служб Visio в Microsoft SharePoint Server 2013.
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346475"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="f27ef-103">Элемент Рефрешабледата (Публишсеттингс_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f27ef-103">RefreshableData element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f27ef-104">Указывает, следует ли обновлять набор записей с помощью служб Visio в Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f27ef-104">Specifies whether a recordset is refreshable using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f27ef-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f27ef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f27ef-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f27ef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f27ef-107">Рефрешабледата_типе</span><span class="sxs-lookup"><span data-stu-id="f27ef-107">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f27ef-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f27ef-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f27ef-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f27ef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f27ef-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f27ef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f27ef-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f27ef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f27ef-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="f27ef-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f27ef-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f27ef-113">Definition</span></span>

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a><span data-ttu-id="f27ef-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f27ef-114">Elements and attributes</span></span>

<span data-ttu-id="f27ef-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f27ef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f27ef-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f27ef-116">Parent elements</span></span>

|<span data-ttu-id="f27ef-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f27ef-117">**Element**</span></span>|<span data-ttu-id="f27ef-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f27ef-118">**Type**</span></span>|<span data-ttu-id="f27ef-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f27ef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f27ef-120">Публишсеттингс</span><span class="sxs-lookup"><span data-stu-id="f27ef-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f27ef-121">Публишсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="f27ef-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f27ef-122">Задает параметры, которые используются при открытии схемы с помощью служб Visio.</span><span class="sxs-lookup"><span data-stu-id="f27ef-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f27ef-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f27ef-123">Child elements</span></span>

<span data-ttu-id="f27ef-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="f27ef-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f27ef-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f27ef-125">Attributes</span></span>

|<span data-ttu-id="f27ef-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f27ef-126">**Attribute**</span></span>|<span data-ttu-id="f27ef-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f27ef-127">**Type**</span></span>|<span data-ttu-id="f27ef-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f27ef-128">**Required**</span></span>|<span data-ttu-id="f27ef-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f27ef-129">**Description**</span></span>|<span data-ttu-id="f27ef-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f27ef-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f27ef-131">ИД</span><span class="sxs-lookup"><span data-stu-id="f27ef-131">ID</span></span>  <br/> |<span data-ttu-id="f27ef-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="f27ef-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f27ef-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f27ef-133">required</span></span>  <br/> |<span data-ttu-id="f27ef-134">Идентификатор объекта Recordset.</span><span class="sxs-lookup"><span data-stu-id="f27ef-134">The identifier of a recordset.</span></span>  <br/> |<span data-ttu-id="f27ef-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="f27ef-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

