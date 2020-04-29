---
title: Курренттипе complexType (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры для текущего положения прогноза погоды.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540989"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="f5b69-103">Курренттипе complexType (схема сведений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="f5b69-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f5b69-104">Определяет параметры для текущего положения прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="f5b69-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="f5b69-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f5b69-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5b69-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f5b69-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f5b69-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f5b69-107">**Schema file**</span></span> <br/> |<span data-ttu-id="f5b69-108">жетвеасеринфо. xsd</span><span class="sxs-lookup"><span data-stu-id="f5b69-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="f5b69-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f5b69-109">**Extension base**</span></span> <br/> |<span data-ttu-id="f5b69-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f5b69-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5b69-111">Определение</span><span class="sxs-lookup"><span data-stu-id="f5b69-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f5b69-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5b69-112">Elements and attributes</span></span>

<span data-ttu-id="f5b69-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f5b69-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f5b69-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f5b69-114">Child elements</span></span>

<span data-ttu-id="f5b69-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="f5b69-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5b69-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5b69-116">Attributes</span></span>

|<span data-ttu-id="f5b69-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f5b69-117">**Attribute**</span></span>|<span data-ttu-id="f5b69-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f5b69-118">**Type**</span></span>|<span data-ttu-id="f5b69-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f5b69-119">**Required**</span></span>|<span data-ttu-id="f5b69-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5b69-120">**Description**</span></span>|<span data-ttu-id="f5b69-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f5b69-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f5b69-122">date</span><span class="sxs-lookup"><span data-stu-id="f5b69-122">date</span></span>  <br/> |<span data-ttu-id="f5b69-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="f5b69-123">xs:date</span></span>  <br/> |<span data-ttu-id="f5b69-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-124">required</span></span>  <br/> |<span data-ttu-id="f5b69-125">Указывает сегодняшнюю дату.</span><span class="sxs-lookup"><span data-stu-id="f5b69-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="f5b69-126">Значение типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="f5b69-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="f5b69-127">открыт</span><span class="sxs-lookup"><span data-stu-id="f5b69-127">day</span></span>  <br/> |<span data-ttu-id="f5b69-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="f5b69-128">xs:string</span></span>  <br/> |<span data-ttu-id="f5b69-129">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-129">optional</span></span>  <br/> |<span data-ttu-id="f5b69-130">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="f5b69-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="f5b69-131">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f5b69-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f5b69-132">филслике</span><span class="sxs-lookup"><span data-stu-id="f5b69-132">feelslike</span></span>  <br/> |<span data-ttu-id="f5b69-133">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-133">xs:integer</span></span>  <br/> |<span data-ttu-id="f5b69-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-134">required</span></span>  <br/> |<span data-ttu-id="f5b69-135">Указывает температуру, с которой понравится Текущая погода.</span><span class="sxs-lookup"><span data-stu-id="f5b69-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="f5b69-136">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f5b69-137">хранени</span><span class="sxs-lookup"><span data-stu-id="f5b69-137">humidity</span></span>  <br/> |<span data-ttu-id="f5b69-138">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-138">xs:integer</span></span>  <br/> |<span data-ttu-id="f5b69-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-139">required</span></span>  <br/> |<span data-ttu-id="f5b69-140">Задает текущее числовое значение влажности.</span><span class="sxs-lookup"><span data-stu-id="f5b69-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="f5b69-141">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f5b69-142">обсерватионпоинт</span><span class="sxs-lookup"><span data-stu-id="f5b69-142">observationpoint</span></span>  <br/> |<span data-ttu-id="f5b69-143">xs: String</span><span class="sxs-lookup"><span data-stu-id="f5b69-143">xs:string</span></span>  <br/> |<span data-ttu-id="f5b69-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-144">required</span></span>  <br/> |<span data-ttu-id="f5b69-145">Указывает, с каких сведений отражается текущая информация о погоде.</span><span class="sxs-lookup"><span data-stu-id="f5b69-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="f5b69-146">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f5b69-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f5b69-147">обсерватионтиме</span><span class="sxs-lookup"><span data-stu-id="f5b69-147">observationtime</span></span>  <br/> |<span data-ttu-id="f5b69-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="f5b69-148">xs:time</span></span>  <br/> |<span data-ttu-id="f5b69-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-149">required</span></span>  <br/> |<span data-ttu-id="f5b69-150">Указывает, когда отражается текущая информация о погоде.</span><span class="sxs-lookup"><span data-stu-id="f5b69-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="f5b69-151">Значение типа xs: Time</span><span class="sxs-lookup"><span data-stu-id="f5b69-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="f5b69-152">шортдай</span><span class="sxs-lookup"><span data-stu-id="f5b69-152">shortday</span></span>  <br/> |<span data-ttu-id="f5b69-153">xs: String</span><span class="sxs-lookup"><span data-stu-id="f5b69-153">xs:string</span></span>  <br/> |<span data-ttu-id="f5b69-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-154">optional</span></span>  <br/> |<span data-ttu-id="f5b69-155">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="f5b69-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="f5b69-156">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f5b69-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f5b69-157">скикоде</span><span class="sxs-lookup"><span data-stu-id="f5b69-157">skycode</span></span>  <br/> |<span data-ttu-id="f5b69-158">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-158">xs:integer</span></span>  <br/> |<span data-ttu-id="f5b69-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-159">required</span></span>  <br/> |<span data-ttu-id="f5b69-160">Задает целочисленный код для текущих условий погоды.</span><span class="sxs-lookup"><span data-stu-id="f5b69-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="f5b69-161">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f5b69-162">скитекст</span><span class="sxs-lookup"><span data-stu-id="f5b69-162">skytext</span></span>  <br/> |<span data-ttu-id="f5b69-163">xs: String</span><span class="sxs-lookup"><span data-stu-id="f5b69-163">xs:string</span></span>  <br/> |<span data-ttu-id="f5b69-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-164">required</span></span>  <br/> |<span data-ttu-id="f5b69-165">Указывает одно на два слова, описывающих текущие условия погоды.</span><span class="sxs-lookup"><span data-stu-id="f5b69-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="f5b69-166">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f5b69-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f5b69-167">Рабочая</span><span class="sxs-lookup"><span data-stu-id="f5b69-167">temperature</span></span>  <br/> |<span data-ttu-id="f5b69-168">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-168">xs:integer</span></span>  <br/> |<span data-ttu-id="f5b69-169">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-169">required</span></span>  <br/> |<span data-ttu-id="f5b69-170">Задает текущую температуру расположения.</span><span class="sxs-lookup"><span data-stu-id="f5b69-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="f5b69-171">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f5b69-172">винддисплай</span><span class="sxs-lookup"><span data-stu-id="f5b69-172">winddisplay</span></span>  <br/> |<span data-ttu-id="f5b69-173">xs: String</span><span class="sxs-lookup"><span data-stu-id="f5b69-173">xs:string</span></span>  <br/> |<span data-ttu-id="f5b69-174">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-174">required</span></span>  <br/> |<span data-ttu-id="f5b69-175">Строка, описывающая текущие условия обмотки.</span><span class="sxs-lookup"><span data-stu-id="f5b69-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="f5b69-176">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f5b69-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f5b69-177">виндспид</span><span class="sxs-lookup"><span data-stu-id="f5b69-177">windspeed</span></span>  <br/> |<span data-ttu-id="f5b69-178">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-178">xs:integer</span></span>  <br/> |<span data-ttu-id="f5b69-179">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5b69-179">required</span></span>  <br/> |<span data-ttu-id="f5b69-180">Задает текущее числовое значение скорости обмотки.</span><span class="sxs-lookup"><span data-stu-id="f5b69-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="f5b69-181">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f5b69-181">A value of the type xs:integer</span></span>  <br/> |
   

