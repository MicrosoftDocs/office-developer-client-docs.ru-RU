---
title: weatherType complexType (Схема сведений о погоде в Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Указывает погоду расположения.
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542949"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="80755-103">weatherType complexType (Схема сведений о погоде в Outlook)</span><span class="sxs-lookup"><span data-stu-id="80755-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="80755-104">Указывает погоду расположения.</span><span class="sxs-lookup"><span data-stu-id="80755-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="80755-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="80755-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80755-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="80755-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="80755-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="80755-107">**Schema file**</span></span> <br/> |<span data-ttu-id="80755-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="80755-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="80755-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="80755-109">**Extension base**</span></span> <br/> |<span data-ttu-id="80755-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="80755-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80755-111">Определение</span><span class="sxs-lookup"><span data-stu-id="80755-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="80755-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="80755-112">Elements and attributes</span></span>

<span data-ttu-id="80755-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="80755-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="80755-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="80755-114">Child elements</span></span>

|<span data-ttu-id="80755-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="80755-115">**Element**</span></span>|<span data-ttu-id="80755-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="80755-116">**Type**</span></span>|<span data-ttu-id="80755-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="80755-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80755-118">current</span><span class="sxs-lookup"><span data-stu-id="80755-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="80755-119">currentType</span><span class="sxs-lookup"><span data-stu-id="80755-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="80755-120">Указывает текущие прогнозы погоды.</span><span class="sxs-lookup"><span data-stu-id="80755-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="80755-121">forecast</span><span class="sxs-lookup"><span data-stu-id="80755-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="80755-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="80755-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="80755-123">Указывает будущие прогнозы погоды по крайней мере на три дня вперед, включая сегодня: сегодня, завтра, день после завтра.</span><span class="sxs-lookup"><span data-stu-id="80755-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="80755-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="80755-124">Attributes</span></span>

|<span data-ttu-id="80755-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="80755-125">**Attribute**</span></span>|<span data-ttu-id="80755-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="80755-126">**Type**</span></span>|<span data-ttu-id="80755-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="80755-127">**Required**</span></span>|<span data-ttu-id="80755-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="80755-128">**Description**</span></span>|<span data-ttu-id="80755-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="80755-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80755-130">attribution</span><span class="sxs-lookup"><span data-stu-id="80755-130">attribution</span></span>  <br/> |<span data-ttu-id="80755-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-131">xs:string</span></span>  <br/> |<span data-ttu-id="80755-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-132">required</span></span>  <br/> |<span data-ttu-id="80755-133">Указывает источник сведений о погоде.</span><span class="sxs-lookup"><span data-stu-id="80755-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="80755-134">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="80755-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="80755-135">degreetype</span></span>  <br/> |<span data-ttu-id="80755-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-136">xs:string</span></span>  <br/> |<span data-ttu-id="80755-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-137">required</span></span>  <br/> |<span data-ttu-id="80755-138">Указывает единицу температуры расположения, например Цельсия.</span><span class="sxs-lookup"><span data-stu-id="80755-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="80755-139">C, F</span><span class="sxs-lookup"><span data-stu-id="80755-139">C, F</span></span>  <br/> |
|<span data-ttu-id="80755-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="80755-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="80755-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-141">xs:string</span></span>  <br/> |<span data-ttu-id="80755-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-142">required</span></span>  <br/> |<span data-ttu-id="80755-143">Указывает URL-адрес изображения для расположения.</span><span class="sxs-lookup"><span data-stu-id="80755-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="80755-144">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="80755-145">timezone</span><span class="sxs-lookup"><span data-stu-id="80755-145">timezone</span></span>  <br/> |<span data-ttu-id="80755-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="80755-146">xs:integer</span></span>  <br/> |<span data-ttu-id="80755-147">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-147">required</span></span>  <br/> |<span data-ttu-id="80755-148">Указывает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="80755-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="80755-149">Значение от -11 до 12 включительно</span><span class="sxs-lookup"><span data-stu-id="80755-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="80755-150">url</span><span class="sxs-lookup"><span data-stu-id="80755-150">url</span></span>  <br/> |<span data-ttu-id="80755-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-151">xs:string</span></span>  <br/> |<span data-ttu-id="80755-152">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-152">required</span></span>  <br/> |<span data-ttu-id="80755-153">Указывает URL-адрес веб-страницы службы прогноза погоды, которая содержит сведения о погоде для указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="80755-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="80755-154">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="80755-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="80755-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="80755-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-156">xs:string</span></span>  <br/> |<span data-ttu-id="80755-157">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-157">required</span></span>  <br/> |<span data-ttu-id="80755-158">Указывает код, связанный с расположением, используемым для различиации нескольких расположений с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="80755-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="80755-159">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="80755-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="80755-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="80755-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-161">xs:string</span></span>  <br/> |<span data-ttu-id="80755-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="80755-162">required</span></span>  <br/> |<span data-ttu-id="80755-163">Указывает имя расположения, которое отображается в выпадаемом оке.</span><span class="sxs-lookup"><span data-stu-id="80755-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="80755-164">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="80755-164">A value of the type xs:string</span></span>  <br/> |
   

