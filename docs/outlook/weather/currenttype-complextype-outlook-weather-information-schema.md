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
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387036"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="5a337-103">currentType complexType (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="5a337-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="5a337-104">Определяет параметры о текущем погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="5a337-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="5a337-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5a337-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a337-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5a337-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="5a337-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5a337-107">**Schema file**</span></span> <br/> |<span data-ttu-id="5a337-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="5a337-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="5a337-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="5a337-109">**Extension base**</span></span> <br/> |<span data-ttu-id="5a337-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="5a337-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5a337-111">Определение</span><span class="sxs-lookup"><span data-stu-id="5a337-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5a337-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5a337-112">Elements and attributes</span></span>

<span data-ttu-id="5a337-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5a337-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5a337-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5a337-114">Child elements</span></span>

<span data-ttu-id="5a337-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="5a337-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a337-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5a337-116">Attributes</span></span>

|<span data-ttu-id="5a337-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5a337-117">**Attribute**</span></span>|<span data-ttu-id="5a337-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5a337-118">**Type**</span></span>|<span data-ttu-id="5a337-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5a337-119">**Required**</span></span>|<span data-ttu-id="5a337-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5a337-120">**Description**</span></span>|<span data-ttu-id="5a337-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5a337-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5a337-122">date</span><span class="sxs-lookup"><span data-stu-id="5a337-122">date</span></span>  <br/> |<span data-ttu-id="5a337-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="5a337-123">xs:date</span></span>  <br/> |<span data-ttu-id="5a337-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-124">required</span></span>  <br/> |<span data-ttu-id="5a337-125">Задает текущую дату.</span><span class="sxs-lookup"><span data-stu-id="5a337-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="5a337-126">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="5a337-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="5a337-127">день</span><span class="sxs-lookup"><span data-stu-id="5a337-127">day</span></span>  <br/> |<span data-ttu-id="5a337-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a337-128">xs:string</span></span>  <br/> |<span data-ttu-id="5a337-129">необязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-129">optional</span></span>  <br/> |<span data-ttu-id="5a337-130">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="5a337-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="5a337-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5a337-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5a337-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="5a337-132">feelslike</span></span>  <br/> |<span data-ttu-id="5a337-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a337-133">xs:integer</span></span>  <br/> |<span data-ttu-id="5a337-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-134">required</span></span>  <br/> |<span data-ttu-id="5a337-135">Указывает, как текущий прогноза погоды, в том числе как температуры.</span><span class="sxs-lookup"><span data-stu-id="5a337-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="5a337-136">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="5a337-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5a337-137">влажность</span><span class="sxs-lookup"><span data-stu-id="5a337-137">humidity</span></span>  <br/> |<span data-ttu-id="5a337-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a337-138">xs:integer</span></span>  <br/> |<span data-ttu-id="5a337-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-139">required</span></span>  <br/> |<span data-ttu-id="5a337-140">Задает текущее значение числовых влажность.</span><span class="sxs-lookup"><span data-stu-id="5a337-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="5a337-141">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="5a337-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5a337-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="5a337-142">observationpoint</span></span>  <br/> |<span data-ttu-id="5a337-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a337-143">xs:string</span></span>  <br/> |<span data-ttu-id="5a337-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-144">required</span></span>  <br/> |<span data-ttu-id="5a337-145">Указывает, где наблюдается из текущей информации о погоде.</span><span class="sxs-lookup"><span data-stu-id="5a337-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="5a337-146">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5a337-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5a337-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="5a337-147">observationtime</span></span>  <br/> |<span data-ttu-id="5a337-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="5a337-148">xs:time</span></span>  <br/> |<span data-ttu-id="5a337-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-149">required</span></span>  <br/> |<span data-ttu-id="5a337-150">Указывает, когда наблюдаемое текущей информации о погоде в.</span><span class="sxs-lookup"><span data-stu-id="5a337-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="5a337-151">Значения типа xs: Time</span><span class="sxs-lookup"><span data-stu-id="5a337-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="5a337-152">shortday</span><span class="sxs-lookup"><span data-stu-id="5a337-152">shortday</span></span>  <br/> |<span data-ttu-id="5a337-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a337-153">xs:string</span></span>  <br/> |<span data-ttu-id="5a337-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-154">optional</span></span>  <br/> |<span data-ttu-id="5a337-155">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="5a337-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="5a337-156">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5a337-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5a337-157">skycode</span><span class="sxs-lookup"><span data-stu-id="5a337-157">skycode</span></span>  <br/> |<span data-ttu-id="5a337-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a337-158">xs:integer</span></span>  <br/> |<span data-ttu-id="5a337-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-159">required</span></span>  <br/> |<span data-ttu-id="5a337-160">Указывает целочисленный код для текущей погоды.</span><span class="sxs-lookup"><span data-stu-id="5a337-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="5a337-161">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="5a337-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5a337-162">skytext</span><span class="sxs-lookup"><span data-stu-id="5a337-162">skytext</span></span>  <br/> |<span data-ttu-id="5a337-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a337-163">xs:string</span></span>  <br/> |<span data-ttu-id="5a337-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-164">required</span></span>  <br/> |<span data-ttu-id="5a337-165">Задает один или два слова, описывающие сводки погоды.</span><span class="sxs-lookup"><span data-stu-id="5a337-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="5a337-166">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5a337-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5a337-167">температура</span><span class="sxs-lookup"><span data-stu-id="5a337-167">temperature</span></span>  <br/> |<span data-ttu-id="5a337-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a337-168">xs:integer</span></span>  <br/> |<span data-ttu-id="5a337-169">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-169">required</span></span>  <br/> |<span data-ttu-id="5a337-170">Задает текущую температуру расположения.</span><span class="sxs-lookup"><span data-stu-id="5a337-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="5a337-171">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="5a337-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5a337-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="5a337-172">winddisplay</span></span>  <br/> |<span data-ttu-id="5a337-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="5a337-173">xs:string</span></span>  <br/> |<span data-ttu-id="5a337-174">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-174">required</span></span>  <br/> |<span data-ttu-id="5a337-175">Строка, описывающая текущие условия устройство.</span><span class="sxs-lookup"><span data-stu-id="5a337-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="5a337-176">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="5a337-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5a337-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="5a337-177">windspeed</span></span>  <br/> |<span data-ttu-id="5a337-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a337-178">xs:integer</span></span>  <br/> |<span data-ttu-id="5a337-179">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5a337-179">required</span></span>  <br/> |<span data-ttu-id="5a337-180">Задает текущее значение скорости числовых устройство.</span><span class="sxs-lookup"><span data-stu-id="5a337-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="5a337-181">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="5a337-181">A value of the type xs:integer</span></span>  <br/> |
   

