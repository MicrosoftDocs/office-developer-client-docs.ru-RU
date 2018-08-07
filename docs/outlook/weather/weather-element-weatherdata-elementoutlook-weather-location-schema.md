---
title: элемент прогноза погоды (weatherdata элемент) (схема местоположения погоды Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Указывает местоположение для прогноза погоды отчет на.
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812926"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="b5a23-103">элемент прогноза погоды (weatherdata элемент) (схема местоположения погоды Outlook)</span><span class="sxs-lookup"><span data-stu-id="b5a23-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="b5a23-104">Указывает местоположение для прогноза погоды отчет на.</span><span class="sxs-lookup"><span data-stu-id="b5a23-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5a23-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b5a23-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5a23-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b5a23-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5a23-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="b5a23-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="b5a23-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b5a23-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="b5a23-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b5a23-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5a23-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="b5a23-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5a23-111">Определение</span><span class="sxs-lookup"><span data-stu-id="b5a23-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5a23-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5a23-112">Elements and attributes</span></span>

<span data-ttu-id="b5a23-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="b5a23-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5a23-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b5a23-114">Parent elements</span></span>

|<span data-ttu-id="b5a23-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b5a23-115">**Element**</span></span>|<span data-ttu-id="b5a23-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5a23-116">**Type**</span></span>|<span data-ttu-id="b5a23-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5a23-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5a23-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="b5a23-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="b5a23-119">Определяет элемент прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="b5a23-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5a23-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b5a23-120">Child elements</span></span>

<span data-ttu-id="b5a23-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="b5a23-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5a23-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5a23-122">Attributes</span></span>

|<span data-ttu-id="b5a23-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b5a23-123">**Attribute**</span></span>|<span data-ttu-id="b5a23-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5a23-124">**Type**</span></span>|<span data-ttu-id="b5a23-125">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="b5a23-125">**Required**</span></span>|<span data-ttu-id="b5a23-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5a23-126">**Description**</span></span>|<span data-ttu-id="b5a23-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b5a23-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5a23-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="b5a23-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b5a23-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="b5a23-129">xs:string</span></span>  <br/> |<span data-ttu-id="b5a23-130">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5a23-130">required</span></span>  <br/> |<span data-ttu-id="b5a23-131">Указывает код, связанный с расположением для различения нескольких расположений с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="b5a23-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="b5a23-132">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="b5a23-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b5a23-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="b5a23-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b5a23-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="b5a23-134">xs:string</span></span>  <br/> |<span data-ttu-id="b5a23-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5a23-135">required</span></span>  <br/> |<span data-ttu-id="b5a23-136">Указывает имя расположения.</span><span class="sxs-lookup"><span data-stu-id="b5a23-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="b5a23-137">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="b5a23-137">A value of the type xs:string</span></span>  <br/> |
   

