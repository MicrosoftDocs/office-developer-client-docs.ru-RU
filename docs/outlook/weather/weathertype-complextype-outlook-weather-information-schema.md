---
title: weatherType complexType (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Задает погоды расположения.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398768"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="7f037-103">weatherType complexType (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="7f037-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="7f037-104">Задает погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="7f037-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="7f037-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7f037-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f037-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7f037-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="7f037-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7f037-107">**Schema file**</span></span> <br/> |<span data-ttu-id="7f037-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="7f037-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="7f037-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7f037-109">**Extension base**</span></span> <br/> |<span data-ttu-id="7f037-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7f037-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f037-111">Определение</span><span class="sxs-lookup"><span data-stu-id="7f037-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="7f037-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7f037-112">Elements and attributes</span></span>

<span data-ttu-id="7f037-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7f037-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f037-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7f037-114">Child elements</span></span>

|<span data-ttu-id="7f037-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7f037-115">**Element**</span></span>|<span data-ttu-id="7f037-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7f037-116">**Type**</span></span>|<span data-ttu-id="7f037-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f037-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7f037-118">current</span><span class="sxs-lookup"><span data-stu-id="7f037-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="7f037-119">currentType</span><span class="sxs-lookup"><span data-stu-id="7f037-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="7f037-120">Указывает текущий погоды.</span><span class="sxs-lookup"><span data-stu-id="7f037-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="7f037-121">Прогноз</span><span class="sxs-lookup"><span data-stu-id="7f037-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="7f037-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="7f037-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="7f037-123">Указывает будущих погоды по крайней мере три дня издержек, включая сегодня: сегодня, завтра, послезавтра.</span><span class="sxs-lookup"><span data-stu-id="7f037-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7f037-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7f037-124">Attributes</span></span>

|<span data-ttu-id="7f037-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7f037-125">**Attribute**</span></span>|<span data-ttu-id="7f037-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7f037-126">**Type**</span></span>|<span data-ttu-id="7f037-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7f037-127">**Required**</span></span>|<span data-ttu-id="7f037-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f037-128">**Description**</span></span>|<span data-ttu-id="7f037-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7f037-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f037-130">атрибуты</span><span class="sxs-lookup"><span data-stu-id="7f037-130">attribution</span></span>  <br/> |<span data-ttu-id="7f037-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-131">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-132">required</span></span>  <br/> |<span data-ttu-id="7f037-133">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="7f037-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="7f037-134">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7f037-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f037-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="7f037-135">degreetype</span></span>  <br/> |<span data-ttu-id="7f037-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-136">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-137">required</span></span>  <br/> |<span data-ttu-id="7f037-138">Определяет единицу измерения для температуры расположения, например градусы Цельсия.</span><span class="sxs-lookup"><span data-stu-id="7f037-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="7f037-139">C, F</span><span class="sxs-lookup"><span data-stu-id="7f037-139">C, F</span></span>  <br/> |
|<span data-ttu-id="7f037-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="7f037-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="7f037-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-141">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-142">required</span></span>  <br/> |<span data-ttu-id="7f037-143">URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="7f037-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="7f037-144">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7f037-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f037-145">часовой пояс</span><span class="sxs-lookup"><span data-stu-id="7f037-145">timezone</span></span>  <br/> |<span data-ttu-id="7f037-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7f037-146">xs:integer</span></span>  <br/> |<span data-ttu-id="7f037-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-147">required</span></span>  <br/> |<span data-ttu-id="7f037-148">Задает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="7f037-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="7f037-149">Значение в диапазоне от -11 и 12 включительно</span><span class="sxs-lookup"><span data-stu-id="7f037-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="7f037-150">url</span><span class="sxs-lookup"><span data-stu-id="7f037-150">url</span></span>  <br/> |<span data-ttu-id="7f037-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-151">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-152">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-152">required</span></span>  <br/> |<span data-ttu-id="7f037-153">Задает URL-адрес для веб-страницы, которая содержит информацию о погоде для заданного расположения службы прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="7f037-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="7f037-154">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7f037-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f037-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="7f037-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="7f037-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-156">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-157">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-157">required</span></span>  <br/> |<span data-ttu-id="7f037-158">Указывает код, который связан с расположением, используемых для различения нескольких расположения, с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="7f037-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="7f037-159">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7f037-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f037-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="7f037-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="7f037-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="7f037-161">xs:string</span></span>  <br/> |<span data-ttu-id="7f037-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7f037-162">required</span></span>  <br/> |<span data-ttu-id="7f037-163">Указывает имя расположения, которое отображается в элементе управления раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="7f037-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="7f037-164">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="7f037-164">A value of the type xs:string</span></span>  <br/> |
   

