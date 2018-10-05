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
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398327"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="7eaeb-103">Прогноз элемент (weatherType complexType) (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="7eaeb-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="7eaeb-104">Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7eaeb-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7eaeb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7eaeb-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7eaeb-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="7eaeb-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="7eaeb-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="7eaeb-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7eaeb-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="7eaeb-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7eaeb-111">Определение</span><span class="sxs-lookup"><span data-stu-id="7eaeb-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="7eaeb-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7eaeb-112">Elements and attributes</span></span>

<span data-ttu-id="7eaeb-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7eaeb-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7eaeb-114">Parent elements</span></span>

|<span data-ttu-id="7eaeb-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-115">**Element**</span></span>|<span data-ttu-id="7eaeb-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-116">**Type**</span></span>|<span data-ttu-id="7eaeb-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7eaeb-118">прогноза погоды</span><span class="sxs-lookup"><span data-stu-id="7eaeb-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="7eaeb-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="7eaeb-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="7eaeb-120">Задает погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7eaeb-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7eaeb-121">Child elements</span></span>

<span data-ttu-id="7eaeb-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7eaeb-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7eaeb-123">Attributes</span></span>

|<span data-ttu-id="7eaeb-124">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-124">**Attribute**</span></span>|<span data-ttu-id="7eaeb-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-125">**Type**</span></span>|<span data-ttu-id="7eaeb-126">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-126">**Required**</span></span>|<span data-ttu-id="7eaeb-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-127">**Description**</span></span>|<span data-ttu-id="7eaeb-128">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7eaeb-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7eaeb-129">date</span><span class="sxs-lookup"><span data-stu-id="7eaeb-129">date</span></span>  <br/> |<span data-ttu-id="7eaeb-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="7eaeb-130">xs:date</span></span>  <br/> |<span data-ttu-id="7eaeb-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-131">required</span></span>  <br/> |<span data-ttu-id="7eaeb-132">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="7eaeb-133">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="7eaeb-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="7eaeb-134">день</span><span class="sxs-lookup"><span data-stu-id="7eaeb-134">day</span></span>  <br/> |<span data-ttu-id="7eaeb-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="7eaeb-135">xs:string</span></span>  <br/> |<span data-ttu-id="7eaeb-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-136">required</span></span>  <br/> |<span data-ttu-id="7eaeb-137">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="7eaeb-138">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7eaeb-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7eaeb-139">Высокая</span><span class="sxs-lookup"><span data-stu-id="7eaeb-139">high</span></span>  <br/> |<span data-ttu-id="7eaeb-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-140">xs:integer</span></span>  <br/> |<span data-ttu-id="7eaeb-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-141">required</span></span>  <br/> |<span data-ttu-id="7eaeb-142">Задает прогнозируемому количеству наибольший температуры.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="7eaeb-143">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7eaeb-144">Низкая</span><span class="sxs-lookup"><span data-stu-id="7eaeb-144">low</span></span>  <br/> |<span data-ttu-id="7eaeb-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-145">xs:integer</span></span>  <br/> |<span data-ttu-id="7eaeb-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-146">required</span></span>  <br/> |<span data-ttu-id="7eaeb-147">Задает прогнозируемому количеству низшего температуры.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="7eaeb-148">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7eaeb-149">precip</span><span class="sxs-lookup"><span data-stu-id="7eaeb-149">precip</span></span>  <br/> |<span data-ttu-id="7eaeb-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-150">xs:integer</span></span>  <br/> |<span data-ttu-id="7eaeb-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-151">required</span></span>  <br/> |<span data-ttu-id="7eaeb-152">Указывает процент возможность precipitation.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="7eaeb-153">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7eaeb-154">shortday</span><span class="sxs-lookup"><span data-stu-id="7eaeb-154">shortday</span></span>  <br/> |<span data-ttu-id="7eaeb-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="7eaeb-155">xs:string</span></span>  <br/> |<span data-ttu-id="7eaeb-156">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-156">required</span></span>  <br/> |<span data-ttu-id="7eaeb-157">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="7eaeb-158">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7eaeb-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7eaeb-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="7eaeb-159">skycodeday</span></span>  <br/> |<span data-ttu-id="7eaeb-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-160">xs:integer</span></span>  <br/> |<span data-ttu-id="7eaeb-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-161">required</span></span>  <br/> |<span data-ttu-id="7eaeb-162">Указывает код прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="7eaeb-163">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7eaeb-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7eaeb-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="7eaeb-164">skytextday</span></span>  <br/> |<span data-ttu-id="7eaeb-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="7eaeb-165">xs:string</span></span>  <br/> |<span data-ttu-id="7eaeb-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7eaeb-166">required</span></span>  <br/> |<span data-ttu-id="7eaeb-167">Указывает один или два слова, которые описывают прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="7eaeb-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="7eaeb-168">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7eaeb-168">A value of the type xs:string</span></span>  <br/> |
   

