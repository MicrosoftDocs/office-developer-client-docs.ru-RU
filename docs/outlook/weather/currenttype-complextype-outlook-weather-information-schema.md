---
title: currentType complexType (Outlook схема сведений о погоде)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Определяет параметры текущих погодных условий расположения.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540989"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="94330-103">currentType complexType (Outlook схема сведений о погоде)</span><span class="sxs-lookup"><span data-stu-id="94330-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="94330-104">Определяет параметры текущих погодных условий расположения.</span><span class="sxs-lookup"><span data-stu-id="94330-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="94330-105">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="94330-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94330-106">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="94330-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="94330-107">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="94330-107">**Schema file**</span></span> <br/> |<span data-ttu-id="94330-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="94330-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="94330-109">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="94330-109">**Extension base**</span></span> <br/> |<span data-ttu-id="94330-110">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="94330-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94330-111">Определение</span><span class="sxs-lookup"><span data-stu-id="94330-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="94330-112">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="94330-112">Elements and attributes</span></span>

<span data-ttu-id="94330-113">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="94330-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="94330-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="94330-114">Child elements</span></span>

<span data-ttu-id="94330-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="94330-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94330-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="94330-116">Attributes</span></span>

|<span data-ttu-id="94330-117">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="94330-117">**Attribute**</span></span>|<span data-ttu-id="94330-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="94330-118">**Type**</span></span>|<span data-ttu-id="94330-119">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="94330-119">**Required**</span></span>|<span data-ttu-id="94330-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="94330-120">**Description**</span></span>|<span data-ttu-id="94330-121">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="94330-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94330-122">date</span><span class="sxs-lookup"><span data-stu-id="94330-122">date</span></span>  <br/> |<span data-ttu-id="94330-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="94330-123">xs:date</span></span>  <br/> |<span data-ttu-id="94330-124">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-124">required</span></span>  <br/> |<span data-ttu-id="94330-125">Указывает дату сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="94330-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="94330-126">Значение типа xs:date</span><span class="sxs-lookup"><span data-stu-id="94330-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="94330-127">день</span><span class="sxs-lookup"><span data-stu-id="94330-127">day</span></span>  <br/> |<span data-ttu-id="94330-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-128">xs:string</span></span>  <br/> |<span data-ttu-id="94330-129">необязательный</span><span class="sxs-lookup"><span data-stu-id="94330-129">optional</span></span>  <br/> |<span data-ttu-id="94330-130">Указывает день для прогноза.</span><span class="sxs-lookup"><span data-stu-id="94330-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="94330-131">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94330-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="94330-132">feelslike</span></span>  <br/> |<span data-ttu-id="94330-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-133">xs:integer</span></span>  <br/> |<span data-ttu-id="94330-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-134">required</span></span>  <br/> |<span data-ttu-id="94330-135">Указывает температуру текущего погодных условий.</span><span class="sxs-lookup"><span data-stu-id="94330-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="94330-136">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94330-137">влажность</span><span class="sxs-lookup"><span data-stu-id="94330-137">humidity</span></span>  <br/> |<span data-ttu-id="94330-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-138">xs:integer</span></span>  <br/> |<span data-ttu-id="94330-139">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-139">required</span></span>  <br/> |<span data-ttu-id="94330-140">Указывает текущее числовое значение влажности.</span><span class="sxs-lookup"><span data-stu-id="94330-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="94330-141">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94330-142">точка наблюдения</span><span class="sxs-lookup"><span data-stu-id="94330-142">observationpoint</span></span>  <br/> |<span data-ttu-id="94330-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-143">xs:string</span></span>  <br/> |<span data-ttu-id="94330-144">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-144">required</span></span>  <br/> |<span data-ttu-id="94330-145">Указывает, откуда наблюдается текущая информация о погоде.</span><span class="sxs-lookup"><span data-stu-id="94330-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="94330-146">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94330-147">время наблюдения</span><span class="sxs-lookup"><span data-stu-id="94330-147">observationtime</span></span>  <br/> |<span data-ttu-id="94330-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="94330-148">xs:time</span></span>  <br/> |<span data-ttu-id="94330-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-149">required</span></span>  <br/> |<span data-ttu-id="94330-150">Указывает, когда наблюдается текущая информация о погоде.</span><span class="sxs-lookup"><span data-stu-id="94330-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="94330-151">Значение типа xs:time</span><span class="sxs-lookup"><span data-stu-id="94330-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="94330-152">shortday</span><span class="sxs-lookup"><span data-stu-id="94330-152">shortday</span></span>  <br/> |<span data-ttu-id="94330-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-153">xs:string</span></span>  <br/> |<span data-ttu-id="94330-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="94330-154">optional</span></span>  <br/> |<span data-ttu-id="94330-155">Указывает день в сокращенной форме.</span><span class="sxs-lookup"><span data-stu-id="94330-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="94330-156">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94330-157">skycode</span><span class="sxs-lookup"><span data-stu-id="94330-157">skycode</span></span>  <br/> |<span data-ttu-id="94330-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-158">xs:integer</span></span>  <br/> |<span data-ttu-id="94330-159">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-159">required</span></span>  <br/> |<span data-ttu-id="94330-160">Указывает код для текущих погодных условий.</span><span class="sxs-lookup"><span data-stu-id="94330-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="94330-161">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94330-162">skytext</span><span class="sxs-lookup"><span data-stu-id="94330-162">skytext</span></span>  <br/> |<span data-ttu-id="94330-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-163">xs:string</span></span>  <br/> |<span data-ttu-id="94330-164">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-164">required</span></span>  <br/> |<span data-ttu-id="94330-165">Указывает от одного до двух слов, описывающих текущие погодные условия.</span><span class="sxs-lookup"><span data-stu-id="94330-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="94330-166">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94330-167">температура</span><span class="sxs-lookup"><span data-stu-id="94330-167">temperature</span></span>  <br/> |<span data-ttu-id="94330-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-168">xs:integer</span></span>  <br/> |<span data-ttu-id="94330-169">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-169">required</span></span>  <br/> |<span data-ttu-id="94330-170">Указывает текущую температуру расположения.</span><span class="sxs-lookup"><span data-stu-id="94330-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="94330-171">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="94330-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="94330-172">winddisplay</span></span>  <br/> |<span data-ttu-id="94330-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-173">xs:string</span></span>  <br/> |<span data-ttu-id="94330-174">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-174">required</span></span>  <br/> |<span data-ttu-id="94330-175">Строка, описывающая текущие условия ветра.</span><span class="sxs-lookup"><span data-stu-id="94330-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="94330-176">Значение типа xs:string</span><span class="sxs-lookup"><span data-stu-id="94330-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="94330-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="94330-177">windspeed</span></span>  <br/> |<span data-ttu-id="94330-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-178">xs:integer</span></span>  <br/> |<span data-ttu-id="94330-179">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94330-179">required</span></span>  <br/> |<span data-ttu-id="94330-180">Указывает текущее числовое значение скорости ветра.</span><span class="sxs-lookup"><span data-stu-id="94330-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="94330-181">Значение типа xs:integer</span><span class="sxs-lookup"><span data-stu-id="94330-181">A value of the type xs:integer</span></span>  <br/> |
   

