---
title: forecastType complexType (Схема сведений о погоде в Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Определяет параметры прогноза погоды расположения.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540954"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="94e31-103">forecastType complexType (Схема сведений о погоде в Outlook)</span><span class="sxs-lookup"><span data-stu-id="94e31-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="94e31-104">Определяет параметры прогноза погоды расположения.</span><span class="sxs-lookup"><span data-stu-id="94e31-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="94e31-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="94e31-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94e31-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="94e31-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="94e31-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="94e31-107">**Schema file**</span></span> <br/> |<span data-ttu-id="94e31-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="94e31-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="94e31-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="94e31-109">**Extension base**</span></span> <br/> |<span data-ttu-id="94e31-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="94e31-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94e31-111">Определение</span><span class="sxs-lookup"><span data-stu-id="94e31-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="94e31-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="94e31-112">Elements and attributes</span></span>

<span data-ttu-id="94e31-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="94e31-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="94e31-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="94e31-114">Child elements</span></span>

<span data-ttu-id="94e31-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="94e31-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94e31-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="94e31-116">Attributes</span></span>

|<span data-ttu-id="94e31-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="94e31-117">**Attribute**</span></span>|<span data-ttu-id="94e31-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="94e31-118">**Type**</span></span>|<span data-ttu-id="94e31-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="94e31-119">**Required**</span></span>|<span data-ttu-id="94e31-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="94e31-120">**Description**</span></span>|<span data-ttu-id="94e31-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="94e31-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94e31-122">date</span><span class="sxs-lookup"><span data-stu-id="94e31-122">date</span></span>  <br/> |<span data-ttu-id="94e31-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="94e31-123">xs:date</span></span>  <br/> |<span data-ttu-id="94e31-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-124">required</span></span>  <br/> |<span data-ttu-id="94e31-125">Указывает дату прогноза.</span><span class="sxs-lookup"><span data-stu-id="94e31-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="94e31-126">Значение типа xs:date</span><span class="sxs-lookup"><span data-stu-id="94e31-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="94e31-127">day</span><span class="sxs-lookup"><span data-stu-id="94e31-127">day</span></span>  <br/> |<span data-ttu-id="94e31-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-128">xs:string</span></span>  <br/> |<span data-ttu-id="94e31-129">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-129">required</span></span>  <br/> |<span data-ttu-id="94e31-130">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="94e31-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="94e31-131">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94e31-132">high</span><span class="sxs-lookup"><span data-stu-id="94e31-132">high</span></span>  <br/> |<span data-ttu-id="94e31-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-133">xs:integer</span></span>  <br/> |<span data-ttu-id="94e31-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-134">required</span></span>  <br/> |<span data-ttu-id="94e31-135">Указывает прогнозируемую наивысшую температуру.</span><span class="sxs-lookup"><span data-stu-id="94e31-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="94e31-136">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94e31-137">low</span><span class="sxs-lookup"><span data-stu-id="94e31-137">low</span></span>  <br/> |<span data-ttu-id="94e31-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-138">xs:integer</span></span>  <br/> |<span data-ttu-id="94e31-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-139">required</span></span>  <br/> |<span data-ttu-id="94e31-140">Указывает прогнозируемую минимальную температуру.</span><span class="sxs-lookup"><span data-stu-id="94e31-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="94e31-141">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94e31-142">precip</span><span class="sxs-lookup"><span data-stu-id="94e31-142">precip</span></span>  <br/> |<span data-ttu-id="94e31-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-143">xs:integer</span></span>  <br/> |<span data-ttu-id="94e31-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-144">required</span></span>  <br/> |<span data-ttu-id="94e31-145">Указывает процентную вероятность хлама.</span><span class="sxs-lookup"><span data-stu-id="94e31-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="94e31-146">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94e31-147">shortday</span><span class="sxs-lookup"><span data-stu-id="94e31-147">shortday</span></span>  <br/> |<span data-ttu-id="94e31-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-148">xs:string</span></span>  <br/> |<span data-ttu-id="94e31-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-149">required</span></span>  <br/> |<span data-ttu-id="94e31-150">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="94e31-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="94e31-151">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94e31-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="94e31-152">skycodeday</span></span>  <br/> |<span data-ttu-id="94e31-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-153">xs:integer</span></span>  <br/> |<span data-ttu-id="94e31-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-154">required</span></span>  <br/> |<span data-ttu-id="94e31-155">Указывает код для прогнозируемых условий.</span><span class="sxs-lookup"><span data-stu-id="94e31-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="94e31-156">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94e31-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94e31-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="94e31-157">skytextday</span></span>  <br/> |<span data-ttu-id="94e31-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-158">xs:string</span></span>  <br/> |<span data-ttu-id="94e31-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94e31-159">required</span></span>  <br/> |<span data-ttu-id="94e31-160">Указывает от одного до двух слов, которые описывают прогнозируемые условия.</span><span class="sxs-lookup"><span data-stu-id="94e31-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="94e31-161">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94e31-161">A value of the type xs:string</span></span>  <br/> |
   

