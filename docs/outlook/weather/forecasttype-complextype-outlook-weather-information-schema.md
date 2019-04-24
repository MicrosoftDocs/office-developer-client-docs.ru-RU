---
title: Форекасттипе complexType (схема сведений о погоде Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Определяет параметры прогноза погоды для местоположения.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361147"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="f9cea-103">Форекасттипе complexType (схема сведений о погоде Outlook)</span><span class="sxs-lookup"><span data-stu-id="f9cea-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f9cea-104">Определяет параметры прогноза погоды для местоположения.</span><span class="sxs-lookup"><span data-stu-id="f9cea-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="f9cea-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f9cea-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9cea-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f9cea-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f9cea-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f9cea-107">**Schema file**</span></span> <br/> |<span data-ttu-id="f9cea-108">жетвеасеринфо. xsd</span><span class="sxs-lookup"><span data-stu-id="f9cea-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="f9cea-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f9cea-109">**Extension base**</span></span> <br/> |<span data-ttu-id="f9cea-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f9cea-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9cea-111">Определение</span><span class="sxs-lookup"><span data-stu-id="f9cea-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f9cea-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f9cea-112">Elements and attributes</span></span>

<span data-ttu-id="f9cea-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f9cea-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f9cea-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f9cea-114">Child elements</span></span>

<span data-ttu-id="f9cea-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="f9cea-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9cea-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f9cea-116">Attributes</span></span>

|<span data-ttu-id="f9cea-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f9cea-117">**Attribute**</span></span>|<span data-ttu-id="f9cea-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f9cea-118">**Type**</span></span>|<span data-ttu-id="f9cea-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f9cea-119">**Required**</span></span>|<span data-ttu-id="f9cea-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f9cea-120">**Description**</span></span>|<span data-ttu-id="f9cea-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f9cea-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f9cea-122">дата</span><span class="sxs-lookup"><span data-stu-id="f9cea-122">date</span></span>  <br/> |<span data-ttu-id="f9cea-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="f9cea-123">xs:date</span></span>  <br/> |<span data-ttu-id="f9cea-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-124">required</span></span>  <br/> |<span data-ttu-id="f9cea-125">Указывает дату для прогноза.</span><span class="sxs-lookup"><span data-stu-id="f9cea-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="f9cea-126">Значение типа xs: Date</span><span class="sxs-lookup"><span data-stu-id="f9cea-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="f9cea-127">открыт</span><span class="sxs-lookup"><span data-stu-id="f9cea-127">day</span></span>  <br/> |<span data-ttu-id="f9cea-128">xs: String</span><span class="sxs-lookup"><span data-stu-id="f9cea-128">xs:string</span></span>  <br/> |<span data-ttu-id="f9cea-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-129">required</span></span>  <br/> |<span data-ttu-id="f9cea-130">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="f9cea-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="f9cea-131">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f9cea-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f9cea-132">высокоуровневых</span><span class="sxs-lookup"><span data-stu-id="f9cea-132">high</span></span>  <br/> |<span data-ttu-id="f9cea-133">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-133">xs:integer</span></span>  <br/> |<span data-ttu-id="f9cea-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-134">required</span></span>  <br/> |<span data-ttu-id="f9cea-135">Указывает прогнозируемую максимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="f9cea-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="f9cea-136">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f9cea-137">потребление</span><span class="sxs-lookup"><span data-stu-id="f9cea-137">low</span></span>  <br/> |<span data-ttu-id="f9cea-138">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-138">xs:integer</span></span>  <br/> |<span data-ttu-id="f9cea-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-139">required</span></span>  <br/> |<span data-ttu-id="f9cea-140">Указывает прогнозируемую минимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="f9cea-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="f9cea-141">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f9cea-142">преЦип</span><span class="sxs-lookup"><span data-stu-id="f9cea-142">precip</span></span>  <br/> |<span data-ttu-id="f9cea-143">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-143">xs:integer</span></span>  <br/> |<span data-ttu-id="f9cea-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-144">required</span></span>  <br/> |<span data-ttu-id="f9cea-145">Указывает процентное отношение возможности преЦипитатион.</span><span class="sxs-lookup"><span data-stu-id="f9cea-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="f9cea-146">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f9cea-147">шортдай</span><span class="sxs-lookup"><span data-stu-id="f9cea-147">shortday</span></span>  <br/> |<span data-ttu-id="f9cea-148">xs: String</span><span class="sxs-lookup"><span data-stu-id="f9cea-148">xs:string</span></span>  <br/> |<span data-ttu-id="f9cea-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-149">required</span></span>  <br/> |<span data-ttu-id="f9cea-150">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="f9cea-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="f9cea-151">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f9cea-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f9cea-152">скикодедай</span><span class="sxs-lookup"><span data-stu-id="f9cea-152">skycodeday</span></span>  <br/> |<span data-ttu-id="f9cea-153">xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-153">xs:integer</span></span>  <br/> |<span data-ttu-id="f9cea-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-154">required</span></span>  <br/> |<span data-ttu-id="f9cea-155">Указывает код для прогнозируемых условий.</span><span class="sxs-lookup"><span data-stu-id="f9cea-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f9cea-156">Значение типа xs: integer</span><span class="sxs-lookup"><span data-stu-id="f9cea-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f9cea-157">скитекстдай</span><span class="sxs-lookup"><span data-stu-id="f9cea-157">skytextday</span></span>  <br/> |<span data-ttu-id="f9cea-158">xs: String</span><span class="sxs-lookup"><span data-stu-id="f9cea-158">xs:string</span></span>  <br/> |<span data-ttu-id="f9cea-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9cea-159">required</span></span>  <br/> |<span data-ttu-id="f9cea-160">Указывает одно на два слова, описывающих прогнозируемые условия.</span><span class="sxs-lookup"><span data-stu-id="f9cea-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f9cea-161">Значение типа xs: String.</span><span class="sxs-lookup"><span data-stu-id="f9cea-161">A value of the type xs:string</span></span>  <br/> |
   

