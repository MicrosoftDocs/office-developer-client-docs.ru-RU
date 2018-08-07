---
title: currentType complexType (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры о текущем погоды расположения.
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812850"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="29656-103">currentType complexType (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="29656-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="29656-104">Определяет параметры о текущем погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="29656-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="29656-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="29656-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29656-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="29656-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="29656-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="29656-107">**Schema file**</span></span> <br/> |<span data-ttu-id="29656-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="29656-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="29656-109">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="29656-109">**Extension base**</span></span> <br/> |<span data-ttu-id="29656-110">Нет</span><span class="sxs-lookup"><span data-stu-id="29656-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29656-111">Определение</span><span class="sxs-lookup"><span data-stu-id="29656-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="29656-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="29656-112">Elements and attributes</span></span>

<span data-ttu-id="29656-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="29656-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="29656-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="29656-114">Child elements</span></span>

<span data-ttu-id="29656-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="29656-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29656-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="29656-116">Attributes</span></span>

|<span data-ttu-id="29656-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="29656-117">**Attribute**</span></span>|<span data-ttu-id="29656-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29656-118">**Type**</span></span>|<span data-ttu-id="29656-119">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="29656-119">**Required**</span></span>|<span data-ttu-id="29656-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="29656-120">**Description**</span></span>|<span data-ttu-id="29656-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="29656-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29656-122">date</span><span class="sxs-lookup"><span data-stu-id="29656-122">date</span></span>  <br/> |<span data-ttu-id="29656-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="29656-123">xs:date</span></span>  <br/> |<span data-ttu-id="29656-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-124">required</span></span>  <br/> |<span data-ttu-id="29656-125">Задает текущую дату.</span><span class="sxs-lookup"><span data-stu-id="29656-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="29656-126">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="29656-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="29656-127">день</span><span class="sxs-lookup"><span data-stu-id="29656-127">day</span></span>  <br/> |<span data-ttu-id="29656-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="29656-128">xs:string</span></span>  <br/> |<span data-ttu-id="29656-129">необязательный</span><span class="sxs-lookup"><span data-stu-id="29656-129">optional</span></span>  <br/> |<span data-ttu-id="29656-130">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="29656-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="29656-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="29656-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="29656-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="29656-132">feelslike</span></span>  <br/> |<span data-ttu-id="29656-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29656-133">xs:integer</span></span>  <br/> |<span data-ttu-id="29656-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-134">required</span></span>  <br/> |<span data-ttu-id="29656-135">Указывает, как текущий прогноза погоды, в том числе как температуры.</span><span class="sxs-lookup"><span data-stu-id="29656-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="29656-136">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="29656-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="29656-137">влажность</span><span class="sxs-lookup"><span data-stu-id="29656-137">humidity</span></span>  <br/> |<span data-ttu-id="29656-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29656-138">xs:integer</span></span>  <br/> |<span data-ttu-id="29656-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-139">required</span></span>  <br/> |<span data-ttu-id="29656-140">Задает текущее значение числовых влажность.</span><span class="sxs-lookup"><span data-stu-id="29656-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="29656-141">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="29656-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="29656-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="29656-142">observationpoint</span></span>  <br/> |<span data-ttu-id="29656-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="29656-143">xs:string</span></span>  <br/> |<span data-ttu-id="29656-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-144">required</span></span>  <br/> |<span data-ttu-id="29656-145">Указывает, где наблюдается из текущей информации о погоде.</span><span class="sxs-lookup"><span data-stu-id="29656-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="29656-146">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="29656-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="29656-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="29656-147">observationtime</span></span>  <br/> |<span data-ttu-id="29656-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="29656-148">xs:time</span></span>  <br/> |<span data-ttu-id="29656-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-149">required</span></span>  <br/> |<span data-ttu-id="29656-150">Указывает, когда наблюдаемое текущей информации о погоде в.</span><span class="sxs-lookup"><span data-stu-id="29656-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="29656-151">Значения типа xs: Time</span><span class="sxs-lookup"><span data-stu-id="29656-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="29656-152">shortday</span><span class="sxs-lookup"><span data-stu-id="29656-152">shortday</span></span>  <br/> |<span data-ttu-id="29656-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="29656-153">xs:string</span></span>  <br/> |<span data-ttu-id="29656-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="29656-154">optional</span></span>  <br/> |<span data-ttu-id="29656-155">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="29656-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="29656-156">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="29656-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="29656-157">skycode</span><span class="sxs-lookup"><span data-stu-id="29656-157">skycode</span></span>  <br/> |<span data-ttu-id="29656-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29656-158">xs:integer</span></span>  <br/> |<span data-ttu-id="29656-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-159">required</span></span>  <br/> |<span data-ttu-id="29656-160">Указывает целочисленный код для текущей погоды.</span><span class="sxs-lookup"><span data-stu-id="29656-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="29656-161">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="29656-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="29656-162">skytext</span><span class="sxs-lookup"><span data-stu-id="29656-162">skytext</span></span>  <br/> |<span data-ttu-id="29656-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="29656-163">xs:string</span></span>  <br/> |<span data-ttu-id="29656-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-164">required</span></span>  <br/> |<span data-ttu-id="29656-165">Задает один или два слова, описывающие сводки погоды.</span><span class="sxs-lookup"><span data-stu-id="29656-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="29656-166">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="29656-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="29656-167">температура</span><span class="sxs-lookup"><span data-stu-id="29656-167">temperature</span></span>  <br/> |<span data-ttu-id="29656-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29656-168">xs:integer</span></span>  <br/> |<span data-ttu-id="29656-169">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-169">required</span></span>  <br/> |<span data-ttu-id="29656-170">Задает текущую температуру расположения.</span><span class="sxs-lookup"><span data-stu-id="29656-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="29656-171">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="29656-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="29656-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="29656-172">winddisplay</span></span>  <br/> |<span data-ttu-id="29656-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="29656-173">xs:string</span></span>  <br/> |<span data-ttu-id="29656-174">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-174">required</span></span>  <br/> |<span data-ttu-id="29656-175">Строка, описывающая текущие условия устройство.</span><span class="sxs-lookup"><span data-stu-id="29656-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="29656-176">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="29656-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="29656-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="29656-177">windspeed</span></span>  <br/> |<span data-ttu-id="29656-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="29656-178">xs:integer</span></span>  <br/> |<span data-ttu-id="29656-179">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29656-179">required</span></span>  <br/> |<span data-ttu-id="29656-180">Задает текущее значение скорости числовых устройство.</span><span class="sxs-lookup"><span data-stu-id="29656-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="29656-181">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="29656-181">A value of the type xs:integer</span></span>  <br/> |
   

