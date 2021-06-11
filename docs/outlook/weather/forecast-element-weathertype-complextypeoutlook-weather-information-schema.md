---
title: Элемент forecast (weatherType complexType) (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Указывает будущие погодные условия по крайней мере на три дня вперед, в том числе сегодня: сегодня, завтра, послезавтра.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540982"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="dad81-103">Элемент forecast (weatherType complexType) (Outlook схема сведений о погоде)</span><span class="sxs-lookup"><span data-stu-id="dad81-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="dad81-104">Указывает будущие погодные условия по крайней мере на три дня вперед, в том числе сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="dad81-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dad81-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dad81-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dad81-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="dad81-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dad81-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="dad81-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="dad81-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="dad81-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="dad81-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="dad81-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dad81-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="dad81-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dad81-111">Определение</span><span class="sxs-lookup"><span data-stu-id="dad81-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="dad81-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="dad81-112">Elements and attributes</span></span>

<span data-ttu-id="dad81-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="dad81-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dad81-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dad81-114">Parent elements</span></span>

|<span data-ttu-id="dad81-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="dad81-115">**Element**</span></span>|<span data-ttu-id="dad81-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dad81-116">**Type**</span></span>|<span data-ttu-id="dad81-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dad81-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dad81-118">погода</span><span class="sxs-lookup"><span data-stu-id="dad81-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="dad81-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="dad81-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="dad81-120">Указывает погодные условия расположения.</span><span class="sxs-lookup"><span data-stu-id="dad81-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dad81-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dad81-121">Child elements</span></span>

<span data-ttu-id="dad81-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="dad81-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dad81-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dad81-123">Attributes</span></span>

|<span data-ttu-id="dad81-124">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="dad81-124">**Attribute**</span></span>|<span data-ttu-id="dad81-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="dad81-125">**Type**</span></span>|<span data-ttu-id="dad81-126">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="dad81-126">**Required**</span></span>|<span data-ttu-id="dad81-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dad81-127">**Description**</span></span>|<span data-ttu-id="dad81-128">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="dad81-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dad81-129">date</span><span class="sxs-lookup"><span data-stu-id="dad81-129">date</span></span>  <br/> |<span data-ttu-id="dad81-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="dad81-130">xs:date</span></span>  <br/> |<span data-ttu-id="dad81-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-131">required</span></span>  <br/> |<span data-ttu-id="dad81-132">Указывает дату прогноза.</span><span class="sxs-lookup"><span data-stu-id="dad81-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="dad81-133">Значение типа xs:date</span><span class="sxs-lookup"><span data-stu-id="dad81-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="dad81-134">день</span><span class="sxs-lookup"><span data-stu-id="dad81-134">day</span></span>  <br/> |<span data-ttu-id="dad81-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-135">xs:string</span></span>  <br/> |<span data-ttu-id="dad81-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-136">required</span></span>  <br/> |<span data-ttu-id="dad81-137">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="dad81-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="dad81-138">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dad81-139">высокая</span><span class="sxs-lookup"><span data-stu-id="dad81-139">high</span></span>  <br/> |<span data-ttu-id="dad81-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-140">xs:integer</span></span>  <br/> |<span data-ttu-id="dad81-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-141">required</span></span>  <br/> |<span data-ttu-id="dad81-142">Указывает прогнозируемую наивысшую температуру.</span><span class="sxs-lookup"><span data-stu-id="dad81-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="dad81-143">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dad81-144">низкий</span><span class="sxs-lookup"><span data-stu-id="dad81-144">low</span></span>  <br/> |<span data-ttu-id="dad81-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-145">xs:integer</span></span>  <br/> |<span data-ttu-id="dad81-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-146">required</span></span>  <br/> |<span data-ttu-id="dad81-147">Указывает прогнозируемую минимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="dad81-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="dad81-148">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dad81-149">precip</span><span class="sxs-lookup"><span data-stu-id="dad81-149">precip</span></span>  <br/> |<span data-ttu-id="dad81-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-150">xs:integer</span></span>  <br/> |<span data-ttu-id="dad81-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-151">required</span></span>  <br/> |<span data-ttu-id="dad81-152">Указывает процентную вероятность осадков.</span><span class="sxs-lookup"><span data-stu-id="dad81-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="dad81-153">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dad81-154">shortday</span><span class="sxs-lookup"><span data-stu-id="dad81-154">shortday</span></span>  <br/> |<span data-ttu-id="dad81-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-155">xs:string</span></span>  <br/> |<span data-ttu-id="dad81-156">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-156">required</span></span>  <br/> |<span data-ttu-id="dad81-157">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="dad81-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="dad81-158">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dad81-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="dad81-159">skycodeday</span></span>  <br/> |<span data-ttu-id="dad81-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-160">xs:integer</span></span>  <br/> |<span data-ttu-id="dad81-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-161">required</span></span>  <br/> |<span data-ttu-id="dad81-162">Указывает код для прогнозируемых условий.</span><span class="sxs-lookup"><span data-stu-id="dad81-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="dad81-163">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="dad81-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dad81-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="dad81-164">skytextday</span></span>  <br/> |<span data-ttu-id="dad81-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-165">xs:string</span></span>  <br/> |<span data-ttu-id="dad81-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dad81-166">required</span></span>  <br/> |<span data-ttu-id="dad81-167">Указывает от одного до двух слов, описывая прогнозируемые условия.</span><span class="sxs-lookup"><span data-stu-id="dad81-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="dad81-168">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="dad81-168">A value of the type xs:string</span></span>  <br/> |
   

