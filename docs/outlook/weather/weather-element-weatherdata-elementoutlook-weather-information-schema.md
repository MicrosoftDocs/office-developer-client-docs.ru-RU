---
title: элемент weather (элемент weatherdata) (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Указывает погодные условия расположения.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541269"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="a19b8-103">элемент weather (элемент weatherdata) (Outlook схема сведений о погоде)</span><span class="sxs-lookup"><span data-stu-id="a19b8-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a19b8-104">Указывает погодные условия расположения.</span><span class="sxs-lookup"><span data-stu-id="a19b8-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a19b8-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a19b8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a19b8-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a19b8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a19b8-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="a19b8-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="a19b8-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a19b8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a19b8-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a19b8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a19b8-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="a19b8-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a19b8-111">Определение</span><span class="sxs-lookup"><span data-stu-id="a19b8-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="a19b8-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a19b8-112">Elements and attributes</span></span>

<span data-ttu-id="a19b8-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a19b8-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a19b8-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a19b8-114">Parent elements</span></span>

|<span data-ttu-id="a19b8-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a19b8-115">**Element**</span></span>|<span data-ttu-id="a19b8-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a19b8-116">**Type**</span></span>|<span data-ttu-id="a19b8-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a19b8-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a19b8-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="a19b8-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="a19b8-119">Определяет элемент погоды.</span><span class="sxs-lookup"><span data-stu-id="a19b8-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a19b8-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a19b8-120">Child elements</span></span>

|<span data-ttu-id="a19b8-121">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a19b8-121">**Element**</span></span>|<span data-ttu-id="a19b8-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a19b8-122">**Type**</span></span>|<span data-ttu-id="a19b8-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a19b8-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a19b8-124">текущий</span><span class="sxs-lookup"><span data-stu-id="a19b8-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a19b8-125">currentType</span><span class="sxs-lookup"><span data-stu-id="a19b8-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a19b8-126">Указывает текущие погодные условия.</span><span class="sxs-lookup"><span data-stu-id="a19b8-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="a19b8-127">прогноз</span><span class="sxs-lookup"><span data-stu-id="a19b8-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a19b8-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="a19b8-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a19b8-129">Указывает будущие погодные условия по крайней мере на три дня вперед, в том числе сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="a19b8-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a19b8-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a19b8-130">Attributes</span></span>

|<span data-ttu-id="a19b8-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a19b8-131">**Attribute**</span></span>|<span data-ttu-id="a19b8-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a19b8-132">**Type**</span></span>|<span data-ttu-id="a19b8-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a19b8-133">**Required**</span></span>|<span data-ttu-id="a19b8-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a19b8-134">**Description**</span></span>|<span data-ttu-id="a19b8-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a19b8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a19b8-136">атрибуция</span><span class="sxs-lookup"><span data-stu-id="a19b8-136">attribution</span></span>  <br/> |<span data-ttu-id="a19b8-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-137">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-138">required</span></span>  <br/> |<span data-ttu-id="a19b8-139">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="a19b8-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="a19b8-140">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a19b8-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="a19b8-141">degreetype</span></span>  <br/> |<span data-ttu-id="a19b8-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-142">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-143">required</span></span>  <br/> |<span data-ttu-id="a19b8-144">Указывает устройство для температуры расположения, например По Цельсию.</span><span class="sxs-lookup"><span data-stu-id="a19b8-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="a19b8-145">C, F</span><span class="sxs-lookup"><span data-stu-id="a19b8-145">C, F</span></span>  <br/> |
|<span data-ttu-id="a19b8-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="a19b8-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="a19b8-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-147">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-148">required</span></span>  <br/> |<span data-ttu-id="a19b8-149">Указывает URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="a19b8-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="a19b8-150">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a19b8-151">timezone</span><span class="sxs-lookup"><span data-stu-id="a19b8-151">timezone</span></span>  <br/> |<span data-ttu-id="a19b8-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a19b8-152">xs:integer</span></span>  <br/> |<span data-ttu-id="a19b8-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-153">required</span></span>  <br/> |<span data-ttu-id="a19b8-154">Указывает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="a19b8-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="a19b8-155">Значение между -11 и 12 включительно</span><span class="sxs-lookup"><span data-stu-id="a19b8-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="a19b8-156">url</span><span class="sxs-lookup"><span data-stu-id="a19b8-156">url</span></span>  <br/> |<span data-ttu-id="a19b8-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-157">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-158">required</span></span>  <br/> |<span data-ttu-id="a19b8-159">Указывает URL-адрес веб-страницы службы погоды, которая содержит сведения о погоде для указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="a19b8-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="a19b8-160">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a19b8-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="a19b8-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="a19b8-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-162">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-163">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-163">required</span></span>  <br/> |<span data-ttu-id="a19b8-164">Указывает код, связанный с расположением, используемым для различий нескольких расположений с одинаковым именем.</span><span class="sxs-lookup"><span data-stu-id="a19b8-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="a19b8-165">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a19b8-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="a19b8-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="a19b8-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-167">xs:string</span></span>  <br/> |<span data-ttu-id="a19b8-168">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a19b8-168">required</span></span>  <br/> |<span data-ttu-id="a19b8-169">Указывает имя расположения, которое отображается в выпадаемом контроле.</span><span class="sxs-lookup"><span data-stu-id="a19b8-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="a19b8-170">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="a19b8-170">A value of the type xs:string</span></span>  <br/> |
   

