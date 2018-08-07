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
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812923"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="ddaf6-103">элемент прогноза погоды (weatherdata элемент) (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="ddaf6-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ddaf6-104">Задает погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddaf6-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ddaf6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddaf6-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ddaf6-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="ddaf6-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="ddaf6-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ddaf6-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ddaf6-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="ddaf6-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ddaf6-111">Определение</span><span class="sxs-lookup"><span data-stu-id="ddaf6-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ddaf6-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ddaf6-112">Elements and attributes</span></span>

<span data-ttu-id="ddaf6-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ddaf6-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ddaf6-114">Parent elements</span></span>

|<span data-ttu-id="ddaf6-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-115">**Element**</span></span>|<span data-ttu-id="ddaf6-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-116">**Type**</span></span>|<span data-ttu-id="ddaf6-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddaf6-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="ddaf6-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="ddaf6-119">Определяет элемент прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ddaf6-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ddaf6-120">Child elements</span></span>

|<span data-ttu-id="ddaf6-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-121">**Element**</span></span>|<span data-ttu-id="ddaf6-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-122">**Type**</span></span>|<span data-ttu-id="ddaf6-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ddaf6-124">current</span><span class="sxs-lookup"><span data-stu-id="ddaf6-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ddaf6-125">currentType</span><span class="sxs-lookup"><span data-stu-id="ddaf6-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ddaf6-126">Указывает текущий погоды.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="ddaf6-127">Прогноз</span><span class="sxs-lookup"><span data-stu-id="ddaf6-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ddaf6-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="ddaf6-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ddaf6-129">Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ddaf6-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ddaf6-130">Attributes</span></span>

|<span data-ttu-id="ddaf6-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-131">**Attribute**</span></span>|<span data-ttu-id="ddaf6-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-132">**Type**</span></span>|<span data-ttu-id="ddaf6-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-133">**Required**</span></span>|<span data-ttu-id="ddaf6-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-134">**Description**</span></span>|<span data-ttu-id="ddaf6-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ddaf6-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ddaf6-136">атрибуты</span><span class="sxs-lookup"><span data-stu-id="ddaf6-136">attribution</span></span>  <br/> |<span data-ttu-id="ddaf6-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-137">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-138">required</span></span>  <br/> |<span data-ttu-id="ddaf6-139">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="ddaf6-140">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="ddaf6-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ddaf6-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="ddaf6-141">degreetype</span></span>  <br/> |<span data-ttu-id="ddaf6-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-142">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-143">required</span></span>  <br/> |<span data-ttu-id="ddaf6-144">Определяет единицу измерения для температуры расположения, например градусы Цельсия.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="ddaf6-145">C, F</span><span class="sxs-lookup"><span data-stu-id="ddaf6-145">C, F</span></span>  <br/> |
|<span data-ttu-id="ddaf6-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="ddaf6-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="ddaf6-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-147">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-148">required</span></span>  <br/> |<span data-ttu-id="ddaf6-149">URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="ddaf6-150">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="ddaf6-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ddaf6-151">часовой пояс</span><span class="sxs-lookup"><span data-stu-id="ddaf6-151">timezone</span></span>  <br/> |<span data-ttu-id="ddaf6-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ddaf6-152">xs:integer</span></span>  <br/> |<span data-ttu-id="ddaf6-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-153">required</span></span>  <br/> |<span data-ttu-id="ddaf6-154">Задает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="ddaf6-155">Значение в диапазоне от -11 и 12 включительно</span><span class="sxs-lookup"><span data-stu-id="ddaf6-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="ddaf6-156">url</span><span class="sxs-lookup"><span data-stu-id="ddaf6-156">url</span></span>  <br/> |<span data-ttu-id="ddaf6-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-157">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-158">required</span></span>  <br/> |<span data-ttu-id="ddaf6-159">Задает URL-адрес для веб-страницы, которая содержит информацию о погоде для заданного расположения службы прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="ddaf6-160">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="ddaf6-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ddaf6-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="ddaf6-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="ddaf6-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-162">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-163">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-163">required</span></span>  <br/> |<span data-ttu-id="ddaf6-164">Указывает код, который связан с расположением, используемых для различения нескольких расположения, с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="ddaf6-165">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="ddaf6-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ddaf6-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="ddaf6-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="ddaf6-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="ddaf6-167">xs:string</span></span>  <br/> |<span data-ttu-id="ddaf6-168">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ddaf6-168">required</span></span>  <br/> |<span data-ttu-id="ddaf6-169">Указывает имя расположения, которое отображается в элементе управления раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="ddaf6-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="ddaf6-170">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="ddaf6-170">A value of the type xs:string</span></span>  <br/> |
   

