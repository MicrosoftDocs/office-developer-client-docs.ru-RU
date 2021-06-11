---
title: элемент weather (элемент weatherdata) (Outlook схема расположения погоды)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Указывает расположение для отчета о погоде.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539014"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="725e9-103">элемент weather (элемент weatherdata) (Outlook схема расположения погоды)</span><span class="sxs-lookup"><span data-stu-id="725e9-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="725e9-104">Указывает расположение для отчета о погоде.</span><span class="sxs-lookup"><span data-stu-id="725e9-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="725e9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="725e9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="725e9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="725e9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="725e9-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="725e9-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="725e9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="725e9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="725e9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="725e9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="725e9-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="725e9-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="725e9-111">Определение</span><span class="sxs-lookup"><span data-stu-id="725e9-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="725e9-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="725e9-112">Elements and attributes</span></span>

<span data-ttu-id="725e9-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="725e9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="725e9-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="725e9-114">Parent elements</span></span>

|<span data-ttu-id="725e9-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="725e9-115">**Element**</span></span>|<span data-ttu-id="725e9-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="725e9-116">**Type**</span></span>|<span data-ttu-id="725e9-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="725e9-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="725e9-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="725e9-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="725e9-119">Определяет элемент погоды.</span><span class="sxs-lookup"><span data-stu-id="725e9-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="725e9-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="725e9-120">Child elements</span></span>

<span data-ttu-id="725e9-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="725e9-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="725e9-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="725e9-122">Attributes</span></span>

|<span data-ttu-id="725e9-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="725e9-123">**Attribute**</span></span>|<span data-ttu-id="725e9-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="725e9-124">**Type**</span></span>|<span data-ttu-id="725e9-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="725e9-125">**Required**</span></span>|<span data-ttu-id="725e9-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="725e9-126">**Description**</span></span>|<span data-ttu-id="725e9-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="725e9-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="725e9-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="725e9-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="725e9-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="725e9-129">xs:string</span></span>  <br/> |<span data-ttu-id="725e9-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="725e9-130">required</span></span>  <br/> |<span data-ttu-id="725e9-131">Указывает код, связанный с расположением, чтобы различать несколько расположений с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="725e9-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="725e9-132">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="725e9-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="725e9-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="725e9-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="725e9-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="725e9-134">xs:string</span></span>  <br/> |<span data-ttu-id="725e9-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="725e9-135">required</span></span>  <br/> |<span data-ttu-id="725e9-136">Указывает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="725e9-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="725e9-137">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="725e9-137">A value of the type xs:string</span></span>  <br/> |
   

