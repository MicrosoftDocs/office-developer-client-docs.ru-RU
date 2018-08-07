---
title: forecastType complexType (схема сведения о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Определяет параметры о прогноза погоды расположения.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812845"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="3393e-103">forecastType complexType (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="3393e-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="3393e-104">Определяет параметры о прогноза погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="3393e-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="3393e-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3393e-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3393e-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3393e-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="3393e-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3393e-107">**Schema file**</span></span> <br/> |<span data-ttu-id="3393e-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="3393e-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="3393e-109">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="3393e-109">**Extension base**</span></span> <br/> |<span data-ttu-id="3393e-110">Нет</span><span class="sxs-lookup"><span data-stu-id="3393e-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3393e-111">Определение</span><span class="sxs-lookup"><span data-stu-id="3393e-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="3393e-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3393e-112">Elements and attributes</span></span>

<span data-ttu-id="3393e-113">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="3393e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3393e-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3393e-114">Child elements</span></span>

<span data-ttu-id="3393e-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="3393e-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3393e-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3393e-116">Attributes</span></span>

|<span data-ttu-id="3393e-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3393e-117">**Attribute**</span></span>|<span data-ttu-id="3393e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3393e-118">**Type**</span></span>|<span data-ttu-id="3393e-119">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="3393e-119">**Required**</span></span>|<span data-ttu-id="3393e-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3393e-120">**Description**</span></span>|<span data-ttu-id="3393e-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3393e-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3393e-122">date</span><span class="sxs-lookup"><span data-stu-id="3393e-122">date</span></span>  <br/> |<span data-ttu-id="3393e-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="3393e-123">xs:date</span></span>  <br/> |<span data-ttu-id="3393e-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-124">required</span></span>  <br/> |<span data-ttu-id="3393e-125">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="3393e-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="3393e-126">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="3393e-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="3393e-127">день</span><span class="sxs-lookup"><span data-stu-id="3393e-127">day</span></span>  <br/> |<span data-ttu-id="3393e-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="3393e-128">xs:string</span></span>  <br/> |<span data-ttu-id="3393e-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-129">required</span></span>  <br/> |<span data-ttu-id="3393e-130">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="3393e-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="3393e-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="3393e-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3393e-132">Высокая</span><span class="sxs-lookup"><span data-stu-id="3393e-132">high</span></span>  <br/> |<span data-ttu-id="3393e-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3393e-133">xs:integer</span></span>  <br/> |<span data-ttu-id="3393e-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-134">required</span></span>  <br/> |<span data-ttu-id="3393e-135">Задает прогнозируемому количеству наибольший температуры.</span><span class="sxs-lookup"><span data-stu-id="3393e-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="3393e-136">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="3393e-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="3393e-137">Низкая</span><span class="sxs-lookup"><span data-stu-id="3393e-137">low</span></span>  <br/> |<span data-ttu-id="3393e-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3393e-138">xs:integer</span></span>  <br/> |<span data-ttu-id="3393e-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-139">required</span></span>  <br/> |<span data-ttu-id="3393e-140">Задает прогнозируемому количеству низшего температуры.</span><span class="sxs-lookup"><span data-stu-id="3393e-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="3393e-141">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="3393e-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="3393e-142">precip</span><span class="sxs-lookup"><span data-stu-id="3393e-142">precip</span></span>  <br/> |<span data-ttu-id="3393e-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3393e-143">xs:integer</span></span>  <br/> |<span data-ttu-id="3393e-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-144">required</span></span>  <br/> |<span data-ttu-id="3393e-145">Указывает процент возможность precipitation.</span><span class="sxs-lookup"><span data-stu-id="3393e-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="3393e-146">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="3393e-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="3393e-147">shortday</span><span class="sxs-lookup"><span data-stu-id="3393e-147">shortday</span></span>  <br/> |<span data-ttu-id="3393e-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="3393e-148">xs:string</span></span>  <br/> |<span data-ttu-id="3393e-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-149">required</span></span>  <br/> |<span data-ttu-id="3393e-150">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="3393e-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="3393e-151">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="3393e-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="3393e-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="3393e-152">skycodeday</span></span>  <br/> |<span data-ttu-id="3393e-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3393e-153">xs:integer</span></span>  <br/> |<span data-ttu-id="3393e-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-154">required</span></span>  <br/> |<span data-ttu-id="3393e-155">Указывает код прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="3393e-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="3393e-156">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="3393e-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="3393e-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="3393e-157">skytextday</span></span>  <br/> |<span data-ttu-id="3393e-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="3393e-158">xs:string</span></span>  <br/> |<span data-ttu-id="3393e-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3393e-159">required</span></span>  <br/> |<span data-ttu-id="3393e-160">Указывает один или два слова, которые описывают прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="3393e-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="3393e-161">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="3393e-161">A value of the type xs:string</span></span>  <br/> |
   

