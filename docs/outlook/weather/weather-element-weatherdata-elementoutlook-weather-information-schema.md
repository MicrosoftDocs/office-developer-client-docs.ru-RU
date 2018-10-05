---
title: элемент прогноза погоды (weatherdata элемент) (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Задает погоды расположения.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390662"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="0db8b-103">элемент прогноза погоды (weatherdata элемент) (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="0db8b-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="0db8b-104">Задает погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="0db8b-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0db8b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0db8b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0db8b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0db8b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0db8b-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="0db8b-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="0db8b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0db8b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="0db8b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0db8b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0db8b-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="0db8b-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0db8b-111">Определение</span><span class="sxs-lookup"><span data-stu-id="0db8b-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="0db8b-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0db8b-112">Elements and attributes</span></span>

<span data-ttu-id="0db8b-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0db8b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0db8b-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0db8b-114">Parent elements</span></span>

|<span data-ttu-id="0db8b-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0db8b-115">**Element**</span></span>|<span data-ttu-id="0db8b-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0db8b-116">**Type**</span></span>|<span data-ttu-id="0db8b-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0db8b-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0db8b-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="0db8b-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="0db8b-119">Определяет элемент прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="0db8b-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0db8b-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0db8b-120">Child elements</span></span>

|<span data-ttu-id="0db8b-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0db8b-121">**Element**</span></span>|<span data-ttu-id="0db8b-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0db8b-122">**Type**</span></span>|<span data-ttu-id="0db8b-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0db8b-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0db8b-124">current</span><span class="sxs-lookup"><span data-stu-id="0db8b-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="0db8b-125">currentType</span><span class="sxs-lookup"><span data-stu-id="0db8b-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="0db8b-126">Указывает текущий погоды.</span><span class="sxs-lookup"><span data-stu-id="0db8b-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="0db8b-127">Прогноз</span><span class="sxs-lookup"><span data-stu-id="0db8b-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="0db8b-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="0db8b-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="0db8b-129">Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="0db8b-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0db8b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0db8b-130">Attributes</span></span>

|<span data-ttu-id="0db8b-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0db8b-131">**Attribute**</span></span>|<span data-ttu-id="0db8b-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0db8b-132">**Type**</span></span>|<span data-ttu-id="0db8b-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0db8b-133">**Required**</span></span>|<span data-ttu-id="0db8b-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0db8b-134">**Description**</span></span>|<span data-ttu-id="0db8b-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0db8b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0db8b-136">атрибуты</span><span class="sxs-lookup"><span data-stu-id="0db8b-136">attribution</span></span>  <br/> |<span data-ttu-id="0db8b-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-137">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-138">required</span></span>  <br/> |<span data-ttu-id="0db8b-139">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="0db8b-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="0db8b-140">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="0db8b-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0db8b-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="0db8b-141">degreetype</span></span>  <br/> |<span data-ttu-id="0db8b-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-142">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-143">required</span></span>  <br/> |<span data-ttu-id="0db8b-144">Определяет единицу измерения для температуры расположения, например градусы Цельсия.</span><span class="sxs-lookup"><span data-stu-id="0db8b-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="0db8b-145">C, F</span><span class="sxs-lookup"><span data-stu-id="0db8b-145">C, F</span></span>  <br/> |
|<span data-ttu-id="0db8b-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="0db8b-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="0db8b-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-147">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-148">required</span></span>  <br/> |<span data-ttu-id="0db8b-149">URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="0db8b-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="0db8b-150">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="0db8b-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0db8b-151">часовой пояс</span><span class="sxs-lookup"><span data-stu-id="0db8b-151">timezone</span></span>  <br/> |<span data-ttu-id="0db8b-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0db8b-152">xs:integer</span></span>  <br/> |<span data-ttu-id="0db8b-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-153">required</span></span>  <br/> |<span data-ttu-id="0db8b-154">Задает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="0db8b-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="0db8b-155">Значение в диапазоне от -11 и 12 включительно</span><span class="sxs-lookup"><span data-stu-id="0db8b-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="0db8b-156">url</span><span class="sxs-lookup"><span data-stu-id="0db8b-156">url</span></span>  <br/> |<span data-ttu-id="0db8b-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-157">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-158">required</span></span>  <br/> |<span data-ttu-id="0db8b-159">Задает URL-адрес для веб-страницы, которая содержит информацию о погоде для заданного расположения службы прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="0db8b-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="0db8b-160">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="0db8b-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0db8b-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="0db8b-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="0db8b-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-162">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-163">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-163">required</span></span>  <br/> |<span data-ttu-id="0db8b-164">Указывает код, который связан с расположением, используемых для различения нескольких расположения, с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="0db8b-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="0db8b-165">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="0db8b-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0db8b-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="0db8b-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="0db8b-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="0db8b-167">xs:string</span></span>  <br/> |<span data-ttu-id="0db8b-168">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0db8b-168">required</span></span>  <br/> |<span data-ttu-id="0db8b-169">Указывает имя расположения, которое отображается в элементе управления раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="0db8b-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="0db8b-170">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="0db8b-170">A value of the type xs:string</span></span>  <br/> |
   

