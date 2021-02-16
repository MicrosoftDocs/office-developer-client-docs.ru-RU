---
title: Элемент forecast (weatherType complexType) (схема данных о погоде в Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Указывает будущие прогнозы погоды по крайней мере на три дня вперед, включая сегодня: сегодня, завтра, день после завтра.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540982"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="13c87-103">Элемент forecast (weatherType complexType) (схема данных о погоде в Outlook)</span><span class="sxs-lookup"><span data-stu-id="13c87-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="13c87-104">Указывает будущие прогнозы погоды по крайней мере на три дня вперед, включая сегодня: сегодня, завтра, день после завтра.</span><span class="sxs-lookup"><span data-stu-id="13c87-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13c87-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="13c87-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13c87-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="13c87-106">**Element type**</span></span> <br/> |[<span data-ttu-id="13c87-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="13c87-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="13c87-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="13c87-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="13c87-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="13c87-109">**Schema file**</span></span> <br/> |<span data-ttu-id="13c87-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="13c87-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13c87-111">Определение</span><span class="sxs-lookup"><span data-stu-id="13c87-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="13c87-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="13c87-112">Elements and attributes</span></span>

<span data-ttu-id="13c87-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="13c87-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="13c87-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="13c87-114">Parent elements</span></span>

|<span data-ttu-id="13c87-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="13c87-115">**Element**</span></span>|<span data-ttu-id="13c87-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="13c87-116">**Type**</span></span>|<span data-ttu-id="13c87-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13c87-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13c87-118">погода</span><span class="sxs-lookup"><span data-stu-id="13c87-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="13c87-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="13c87-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="13c87-120">Указывает погоду расположения.</span><span class="sxs-lookup"><span data-stu-id="13c87-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13c87-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="13c87-121">Child elements</span></span>

<span data-ttu-id="13c87-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="13c87-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13c87-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="13c87-123">Attributes</span></span>

|<span data-ttu-id="13c87-124">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="13c87-124">**Attribute**</span></span>|<span data-ttu-id="13c87-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="13c87-125">**Type**</span></span>|<span data-ttu-id="13c87-126">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="13c87-126">**Required**</span></span>|<span data-ttu-id="13c87-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="13c87-127">**Description**</span></span>|<span data-ttu-id="13c87-128">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="13c87-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13c87-129">date</span><span class="sxs-lookup"><span data-stu-id="13c87-129">date</span></span>  <br/> |<span data-ttu-id="13c87-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="13c87-130">xs:date</span></span>  <br/> |<span data-ttu-id="13c87-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-131">required</span></span>  <br/> |<span data-ttu-id="13c87-132">Указывает дату прогноза.</span><span class="sxs-lookup"><span data-stu-id="13c87-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="13c87-133">Значение типа xs:date</span><span class="sxs-lookup"><span data-stu-id="13c87-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="13c87-134">day</span><span class="sxs-lookup"><span data-stu-id="13c87-134">day</span></span>  <br/> |<span data-ttu-id="13c87-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-135">xs:string</span></span>  <br/> |<span data-ttu-id="13c87-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-136">required</span></span>  <br/> |<span data-ttu-id="13c87-137">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="13c87-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="13c87-138">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="13c87-139">high</span><span class="sxs-lookup"><span data-stu-id="13c87-139">high</span></span>  <br/> |<span data-ttu-id="13c87-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-140">xs:integer</span></span>  <br/> |<span data-ttu-id="13c87-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-141">required</span></span>  <br/> |<span data-ttu-id="13c87-142">Указывает прогнозируемую наивысшую температуру.</span><span class="sxs-lookup"><span data-stu-id="13c87-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="13c87-143">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="13c87-144">low</span><span class="sxs-lookup"><span data-stu-id="13c87-144">low</span></span>  <br/> |<span data-ttu-id="13c87-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-145">xs:integer</span></span>  <br/> |<span data-ttu-id="13c87-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-146">required</span></span>  <br/> |<span data-ttu-id="13c87-147">Указывает прогнозируемую минимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="13c87-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="13c87-148">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="13c87-149">precip</span><span class="sxs-lookup"><span data-stu-id="13c87-149">precip</span></span>  <br/> |<span data-ttu-id="13c87-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-150">xs:integer</span></span>  <br/> |<span data-ttu-id="13c87-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-151">required</span></span>  <br/> |<span data-ttu-id="13c87-152">Указывает процентную вероятность хлама.</span><span class="sxs-lookup"><span data-stu-id="13c87-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="13c87-153">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="13c87-154">shortday</span><span class="sxs-lookup"><span data-stu-id="13c87-154">shortday</span></span>  <br/> |<span data-ttu-id="13c87-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-155">xs:string</span></span>  <br/> |<span data-ttu-id="13c87-156">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-156">required</span></span>  <br/> |<span data-ttu-id="13c87-157">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="13c87-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="13c87-158">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="13c87-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="13c87-159">skycodeday</span></span>  <br/> |<span data-ttu-id="13c87-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-160">xs:integer</span></span>  <br/> |<span data-ttu-id="13c87-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-161">required</span></span>  <br/> |<span data-ttu-id="13c87-162">Указывает код для прогнозируемых условий.</span><span class="sxs-lookup"><span data-stu-id="13c87-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="13c87-163">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="13c87-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="13c87-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="13c87-164">skytextday</span></span>  <br/> |<span data-ttu-id="13c87-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-165">xs:string</span></span>  <br/> |<span data-ttu-id="13c87-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="13c87-166">required</span></span>  <br/> |<span data-ttu-id="13c87-167">Указывает от одного до двух слов, которые описывают прогнозируемые условия.</span><span class="sxs-lookup"><span data-stu-id="13c87-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="13c87-168">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="13c87-168">A value of the type xs:string</span></span>  <br/> |
   

