---
title: Прогноз элемент (weatherType complexType) (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812851"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="35c49-103">Прогноз элемент (weatherType complexType) (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="35c49-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="35c49-104">Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="35c49-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35c49-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="35c49-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35c49-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="35c49-106">**Element type**</span></span> <br/> |[<span data-ttu-id="35c49-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="35c49-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="35c49-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="35c49-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="35c49-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="35c49-109">**Schema file**</span></span> <br/> |<span data-ttu-id="35c49-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="35c49-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35c49-111">Определение</span><span class="sxs-lookup"><span data-stu-id="35c49-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="35c49-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="35c49-112">Elements and attributes</span></span>

<span data-ttu-id="35c49-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="35c49-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="35c49-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="35c49-114">Parent elements</span></span>

|<span data-ttu-id="35c49-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="35c49-115">**Element**</span></span>|<span data-ttu-id="35c49-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35c49-116">**Type**</span></span>|<span data-ttu-id="35c49-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35c49-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="35c49-118">прогноза погоды</span><span class="sxs-lookup"><span data-stu-id="35c49-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="35c49-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="35c49-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="35c49-120">Задает погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="35c49-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="35c49-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="35c49-121">Child elements</span></span>

<span data-ttu-id="35c49-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="35c49-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35c49-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="35c49-123">Attributes</span></span>

|<span data-ttu-id="35c49-124">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="35c49-124">**Attribute**</span></span>|<span data-ttu-id="35c49-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35c49-125">**Type**</span></span>|<span data-ttu-id="35c49-126">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="35c49-126">**Required**</span></span>|<span data-ttu-id="35c49-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35c49-127">**Description**</span></span>|<span data-ttu-id="35c49-128">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="35c49-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35c49-129">date</span><span class="sxs-lookup"><span data-stu-id="35c49-129">date</span></span>  <br/> |<span data-ttu-id="35c49-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="35c49-130">xs:date</span></span>  <br/> |<span data-ttu-id="35c49-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-131">required</span></span>  <br/> |<span data-ttu-id="35c49-132">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="35c49-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="35c49-133">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="35c49-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="35c49-134">день</span><span class="sxs-lookup"><span data-stu-id="35c49-134">day</span></span>  <br/> |<span data-ttu-id="35c49-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="35c49-135">xs:string</span></span>  <br/> |<span data-ttu-id="35c49-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-136">required</span></span>  <br/> |<span data-ttu-id="35c49-137">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="35c49-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="35c49-138">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="35c49-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="35c49-139">Высокая</span><span class="sxs-lookup"><span data-stu-id="35c49-139">high</span></span>  <br/> |<span data-ttu-id="35c49-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35c49-140">xs:integer</span></span>  <br/> |<span data-ttu-id="35c49-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-141">required</span></span>  <br/> |<span data-ttu-id="35c49-142">Задает прогнозируемому количеству наибольший температуры.</span><span class="sxs-lookup"><span data-stu-id="35c49-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="35c49-143">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="35c49-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="35c49-144">Низкая</span><span class="sxs-lookup"><span data-stu-id="35c49-144">low</span></span>  <br/> |<span data-ttu-id="35c49-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35c49-145">xs:integer</span></span>  <br/> |<span data-ttu-id="35c49-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-146">required</span></span>  <br/> |<span data-ttu-id="35c49-147">Задает прогнозируемому количеству низшего температуры.</span><span class="sxs-lookup"><span data-stu-id="35c49-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="35c49-148">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="35c49-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="35c49-149">precip</span><span class="sxs-lookup"><span data-stu-id="35c49-149">precip</span></span>  <br/> |<span data-ttu-id="35c49-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35c49-150">xs:integer</span></span>  <br/> |<span data-ttu-id="35c49-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-151">required</span></span>  <br/> |<span data-ttu-id="35c49-152">Указывает процент возможность precipitation.</span><span class="sxs-lookup"><span data-stu-id="35c49-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="35c49-153">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="35c49-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="35c49-154">shortday</span><span class="sxs-lookup"><span data-stu-id="35c49-154">shortday</span></span>  <br/> |<span data-ttu-id="35c49-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="35c49-155">xs:string</span></span>  <br/> |<span data-ttu-id="35c49-156">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-156">required</span></span>  <br/> |<span data-ttu-id="35c49-157">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="35c49-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="35c49-158">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="35c49-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="35c49-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="35c49-159">skycodeday</span></span>  <br/> |<span data-ttu-id="35c49-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="35c49-160">xs:integer</span></span>  <br/> |<span data-ttu-id="35c49-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-161">required</span></span>  <br/> |<span data-ttu-id="35c49-162">Указывает код прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="35c49-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="35c49-163">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="35c49-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="35c49-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="35c49-164">skytextday</span></span>  <br/> |<span data-ttu-id="35c49-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="35c49-165">xs:string</span></span>  <br/> |<span data-ttu-id="35c49-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35c49-166">required</span></span>  <br/> |<span data-ttu-id="35c49-167">Указывает один или два слова, которые описывают прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="35c49-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="35c49-168">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="35c49-168">A value of the type xs:string</span></span>  <br/> |
   

