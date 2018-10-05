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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390627"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="4854f-103">forecastType complexType (схема сведения о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="4854f-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4854f-104">Определяет параметры о прогноза погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="4854f-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="4854f-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4854f-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4854f-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4854f-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4854f-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4854f-107">**Schema file**</span></span> <br/> |<span data-ttu-id="4854f-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4854f-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="4854f-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4854f-109">**Extension base**</span></span> <br/> |<span data-ttu-id="4854f-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4854f-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4854f-111">Определение</span><span class="sxs-lookup"><span data-stu-id="4854f-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4854f-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4854f-112">Elements and attributes</span></span>

<span data-ttu-id="4854f-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4854f-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4854f-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4854f-114">Child elements</span></span>

<span data-ttu-id="4854f-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="4854f-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4854f-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4854f-116">Attributes</span></span>

|<span data-ttu-id="4854f-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4854f-117">**Attribute**</span></span>|<span data-ttu-id="4854f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4854f-118">**Type**</span></span>|<span data-ttu-id="4854f-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4854f-119">**Required**</span></span>|<span data-ttu-id="4854f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4854f-120">**Description**</span></span>|<span data-ttu-id="4854f-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4854f-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4854f-122">date</span><span class="sxs-lookup"><span data-stu-id="4854f-122">date</span></span>  <br/> |<span data-ttu-id="4854f-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="4854f-123">xs:date</span></span>  <br/> |<span data-ttu-id="4854f-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-124">required</span></span>  <br/> |<span data-ttu-id="4854f-125">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="4854f-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="4854f-126">Значения типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="4854f-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="4854f-127">день</span><span class="sxs-lookup"><span data-stu-id="4854f-127">day</span></span>  <br/> |<span data-ttu-id="4854f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4854f-128">xs:string</span></span>  <br/> |<span data-ttu-id="4854f-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-129">required</span></span>  <br/> |<span data-ttu-id="4854f-130">Задает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="4854f-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="4854f-131">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="4854f-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4854f-132">Высокая</span><span class="sxs-lookup"><span data-stu-id="4854f-132">high</span></span>  <br/> |<span data-ttu-id="4854f-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4854f-133">xs:integer</span></span>  <br/> |<span data-ttu-id="4854f-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-134">required</span></span>  <br/> |<span data-ttu-id="4854f-135">Задает прогнозируемому количеству наибольший температуры.</span><span class="sxs-lookup"><span data-stu-id="4854f-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="4854f-136">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4854f-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4854f-137">Низкая</span><span class="sxs-lookup"><span data-stu-id="4854f-137">low</span></span>  <br/> |<span data-ttu-id="4854f-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4854f-138">xs:integer</span></span>  <br/> |<span data-ttu-id="4854f-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-139">required</span></span>  <br/> |<span data-ttu-id="4854f-140">Задает прогнозируемому количеству низшего температуры.</span><span class="sxs-lookup"><span data-stu-id="4854f-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="4854f-141">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4854f-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4854f-142">precip</span><span class="sxs-lookup"><span data-stu-id="4854f-142">precip</span></span>  <br/> |<span data-ttu-id="4854f-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4854f-143">xs:integer</span></span>  <br/> |<span data-ttu-id="4854f-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-144">required</span></span>  <br/> |<span data-ttu-id="4854f-145">Указывает процент возможность precipitation.</span><span class="sxs-lookup"><span data-stu-id="4854f-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="4854f-146">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4854f-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4854f-147">shortday</span><span class="sxs-lookup"><span data-stu-id="4854f-147">shortday</span></span>  <br/> |<span data-ttu-id="4854f-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="4854f-148">xs:string</span></span>  <br/> |<span data-ttu-id="4854f-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-149">required</span></span>  <br/> |<span data-ttu-id="4854f-150">Задает день сокращенную форму.</span><span class="sxs-lookup"><span data-stu-id="4854f-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="4854f-151">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="4854f-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4854f-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="4854f-152">skycodeday</span></span>  <br/> |<span data-ttu-id="4854f-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4854f-153">xs:integer</span></span>  <br/> |<span data-ttu-id="4854f-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-154">required</span></span>  <br/> |<span data-ttu-id="4854f-155">Указывает код прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="4854f-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4854f-156">Значения типа xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4854f-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4854f-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="4854f-157">skytextday</span></span>  <br/> |<span data-ttu-id="4854f-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="4854f-158">xs:string</span></span>  <br/> |<span data-ttu-id="4854f-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4854f-159">required</span></span>  <br/> |<span data-ttu-id="4854f-160">Указывает один или два слова, которые описывают прогнозируемому количеству условий.</span><span class="sxs-lookup"><span data-stu-id="4854f-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4854f-161">Значения типа xs: String</span><span class="sxs-lookup"><span data-stu-id="4854f-161">A value of the type xs:string</span></span>  <br/> |
   

