---
title: элемент Weather (элемент веасердата) (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Задает условия для расположения в прогнозе погоды.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541269"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="5928e-103">элемент Weather (элемент веасердата) (схема сведений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="5928e-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="5928e-104">Задает условия для расположения в прогнозе погоды.</span><span class="sxs-lookup"><span data-stu-id="5928e-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5928e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5928e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5928e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5928e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5928e-107">веасертипе</span><span class="sxs-lookup"><span data-stu-id="5928e-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="5928e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5928e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="5928e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5928e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5928e-110">жетвеасеринфо. xsd</span><span class="sxs-lookup"><span data-stu-id="5928e-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5928e-111">Определение</span><span class="sxs-lookup"><span data-stu-id="5928e-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="5928e-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5928e-112">Elements and attributes</span></span>

<span data-ttu-id="5928e-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5928e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5928e-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5928e-114">Parent elements</span></span>

|<span data-ttu-id="5928e-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5928e-115">**Element**</span></span>|<span data-ttu-id="5928e-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5928e-116">**Type**</span></span>|<span data-ttu-id="5928e-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5928e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5928e-118">веасердата</span><span class="sxs-lookup"><span data-stu-id="5928e-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="5928e-119">Определяет элемент weather.</span><span class="sxs-lookup"><span data-stu-id="5928e-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5928e-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5928e-120">Child elements</span></span>

|<span data-ttu-id="5928e-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5928e-121">**Element**</span></span>|<span data-ttu-id="5928e-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5928e-122">**Type**</span></span>|<span data-ttu-id="5928e-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5928e-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5928e-124">этой</span><span class="sxs-lookup"><span data-stu-id="5928e-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="5928e-125">курренттипе</span><span class="sxs-lookup"><span data-stu-id="5928e-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="5928e-126">Задает текущие условия погоды.</span><span class="sxs-lookup"><span data-stu-id="5928e-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="5928e-127">прогнозирует</span><span class="sxs-lookup"><span data-stu-id="5928e-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="5928e-128">форекасттипе</span><span class="sxs-lookup"><span data-stu-id="5928e-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="5928e-129">Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.</span><span class="sxs-lookup"><span data-stu-id="5928e-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5928e-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5928e-130">Attributes</span></span>

|<span data-ttu-id="5928e-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5928e-131">**Attribute**</span></span>|<span data-ttu-id="5928e-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5928e-132">**Type**</span></span>|<span data-ttu-id="5928e-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5928e-133">**Required**</span></span>|<span data-ttu-id="5928e-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5928e-134">**Description**</span></span>|<span data-ttu-id="5928e-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5928e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5928e-136">Attribution</span><span class="sxs-lookup"><span data-stu-id="5928e-136">attribution</span></span>  <br/> |<span data-ttu-id="5928e-137">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-137">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-138">required</span></span>  <br/> |<span data-ttu-id="5928e-139">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="5928e-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="5928e-140">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="5928e-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5928e-141">дегритипе</span><span class="sxs-lookup"><span data-stu-id="5928e-141">degreetype</span></span>  <br/> |<span data-ttu-id="5928e-142">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-142">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-143">required</span></span>  <br/> |<span data-ttu-id="5928e-144">Задает единицу измерения температуры местоположения, например "Цельсия".</span><span class="sxs-lookup"><span data-stu-id="5928e-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="5928e-145">C, F</span><span class="sxs-lookup"><span data-stu-id="5928e-145">C, F</span></span>  <br/> |
|<span data-ttu-id="5928e-146">имажерелативеурл</span><span class="sxs-lookup"><span data-stu-id="5928e-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="5928e-147">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-147">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-148">required</span></span>  <br/> |<span data-ttu-id="5928e-149">Задает URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="5928e-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="5928e-150">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="5928e-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5928e-151">часовой</span><span class="sxs-lookup"><span data-stu-id="5928e-151">timezone</span></span>  <br/> |<span data-ttu-id="5928e-152">xs: integer</span><span class="sxs-lookup"><span data-stu-id="5928e-152">xs:integer</span></span>  <br/> |<span data-ttu-id="5928e-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-153">required</span></span>  <br/> |<span data-ttu-id="5928e-154">Указывает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="5928e-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="5928e-155">Значение в диапазоне от – 11 до 12 включительно</span><span class="sxs-lookup"><span data-stu-id="5928e-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="5928e-156">url</span><span class="sxs-lookup"><span data-stu-id="5928e-156">url</span></span>  <br/> |<span data-ttu-id="5928e-157">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-157">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-158">required</span></span>  <br/> |<span data-ttu-id="5928e-159">Задает URL-адрес веб-страницы службы погоды, содержащей сведения о погоде для указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="5928e-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="5928e-160">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="5928e-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5928e-161">веасерлокатионкоде</span><span class="sxs-lookup"><span data-stu-id="5928e-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="5928e-162">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-162">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-163">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-163">required</span></span>  <br/> |<span data-ttu-id="5928e-164">Указывает код, связанный с расположением, используемым для различения нескольких расположений с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="5928e-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="5928e-165">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="5928e-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5928e-166">веасерлокатионнаме</span><span class="sxs-lookup"><span data-stu-id="5928e-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="5928e-167">xs: String</span><span class="sxs-lookup"><span data-stu-id="5928e-167">xs:string</span></span>  <br/> |<span data-ttu-id="5928e-168">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5928e-168">required</span></span>  <br/> |<span data-ttu-id="5928e-169">Задает имя расположения, которое отображается в раскрывающемся элементе управления.</span><span class="sxs-lookup"><span data-stu-id="5928e-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="5928e-170">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="5928e-170">A value of the type xs:string</span></span>  <br/> |
   

