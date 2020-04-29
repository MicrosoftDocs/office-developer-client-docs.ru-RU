---
title: элемент ПРЕДСКАЗ (Веасертипе complexType) (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540982"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="f8199-103">элемент ПРЕДСКАЗ (Веасертипе complexType) (схема сведений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="f8199-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f8199-104">Указывает будущие условия прогноза по крайней мере за три дня вперед, включая сегодняшние, завтра, завтра, после завтрашнего дня.</span><span class="sxs-lookup"><span data-stu-id="f8199-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8199-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f8199-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8199-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f8199-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f8199-107">форекасттипе</span><span class="sxs-lookup"><span data-stu-id="f8199-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="f8199-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f8199-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f8199-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f8199-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f8199-110">жетвеасеринфо. xsd</span><span class="sxs-lookup"><span data-stu-id="f8199-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8199-111">Определение</span><span class="sxs-lookup"><span data-stu-id="f8199-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="f8199-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8199-112">Elements and attributes</span></span>

<span data-ttu-id="f8199-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f8199-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f8199-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f8199-114">Parent elements</span></span>

|<span data-ttu-id="f8199-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f8199-115">**Element**</span></span>|<span data-ttu-id="f8199-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f8199-116">**Type**</span></span>|<span data-ttu-id="f8199-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8199-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f8199-118">Погода</span><span class="sxs-lookup"><span data-stu-id="f8199-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="f8199-119">веасертипе</span><span class="sxs-lookup"><span data-stu-id="f8199-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="f8199-120">Задает условия для расположения в прогнозе погоды.</span><span class="sxs-lookup"><span data-stu-id="f8199-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8199-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f8199-121">Child elements</span></span>

<span data-ttu-id="f8199-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="f8199-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8199-123">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f8199-123">Attributes</span></span>

|<span data-ttu-id="f8199-124">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f8199-124">**Attribute**</span></span>|<span data-ttu-id="f8199-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f8199-125">**Type**</span></span>|<span data-ttu-id="f8199-126">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f8199-126">**Required**</span></span>|<span data-ttu-id="f8199-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8199-127">**Description**</span></span>|<span data-ttu-id="f8199-128">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f8199-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8199-129">date</span><span class="sxs-lookup"><span data-stu-id="f8199-129">date</span></span>  <br/> |<span data-ttu-id="f8199-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="f8199-130">xs:date</span></span>  <br/> |<span data-ttu-id="f8199-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-131">required</span></span>  <br/> |<span data-ttu-id="f8199-132">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="f8199-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="f8199-133">Значение типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="f8199-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="f8199-134">открыт</span><span class="sxs-lookup"><span data-stu-id="f8199-134">day</span></span>  <br/> |<span data-ttu-id="f8199-135">xs: String</span><span class="sxs-lookup"><span data-stu-id="f8199-135">xs:string</span></span>  <br/> |<span data-ttu-id="f8199-136">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-136">required</span></span>  <br/> |<span data-ttu-id="f8199-137">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="f8199-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="f8199-138">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f8199-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f8199-139">высокоуровневых</span><span class="sxs-lookup"><span data-stu-id="f8199-139">high</span></span>  <br/> |<span data-ttu-id="f8199-140">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-140">xs:integer</span></span>  <br/> |<span data-ttu-id="f8199-141">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-141">required</span></span>  <br/> |<span data-ttu-id="f8199-142">Указывает прогнозируемую максимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="f8199-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="f8199-143">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f8199-144">потребление</span><span class="sxs-lookup"><span data-stu-id="f8199-144">low</span></span>  <br/> |<span data-ttu-id="f8199-145">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-145">xs:integer</span></span>  <br/> |<span data-ttu-id="f8199-146">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-146">required</span></span>  <br/> |<span data-ttu-id="f8199-147">Указывает прогнозируемую минимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="f8199-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="f8199-148">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f8199-149">преЦип</span><span class="sxs-lookup"><span data-stu-id="f8199-149">precip</span></span>  <br/> |<span data-ttu-id="f8199-150">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-150">xs:integer</span></span>  <br/> |<span data-ttu-id="f8199-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-151">required</span></span>  <br/> |<span data-ttu-id="f8199-152">Указывает процентное отношение возможности преЦипитатион.</span><span class="sxs-lookup"><span data-stu-id="f8199-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="f8199-153">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f8199-154">шортдай</span><span class="sxs-lookup"><span data-stu-id="f8199-154">shortday</span></span>  <br/> |<span data-ttu-id="f8199-155">xs: String</span><span class="sxs-lookup"><span data-stu-id="f8199-155">xs:string</span></span>  <br/> |<span data-ttu-id="f8199-156">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-156">required</span></span>  <br/> |<span data-ttu-id="f8199-157">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="f8199-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="f8199-158">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f8199-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f8199-159">скикодедай</span><span class="sxs-lookup"><span data-stu-id="f8199-159">skycodeday</span></span>  <br/> |<span data-ttu-id="f8199-160">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-160">xs:integer</span></span>  <br/> |<span data-ttu-id="f8199-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-161">required</span></span>  <br/> |<span data-ttu-id="f8199-162">Указывает код для прогнозируемых условий.</span><span class="sxs-lookup"><span data-stu-id="f8199-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f8199-163">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f8199-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f8199-164">скитекстдай</span><span class="sxs-lookup"><span data-stu-id="f8199-164">skytextday</span></span>  <br/> |<span data-ttu-id="f8199-165">xs: String</span><span class="sxs-lookup"><span data-stu-id="f8199-165">xs:string</span></span>  <br/> |<span data-ttu-id="f8199-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f8199-166">required</span></span>  <br/> |<span data-ttu-id="f8199-167">Указывает одно на два слова, описывающих прогнозируемые условия.</span><span class="sxs-lookup"><span data-stu-id="f8199-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f8199-168">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f8199-168">A value of the type xs:string</span></span>  <br/> |
   

