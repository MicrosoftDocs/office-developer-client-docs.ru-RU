---
title: Функция CY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Возвращает значение типа currency.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813513"
---
# <a name="cy-function"></a><span data-ttu-id="5a1b2-103">Функция CY</span><span class="sxs-lookup"><span data-stu-id="5a1b2-103">CY Function</span></span>

<span data-ttu-id="5a1b2-104">Возвращает значение типа currency.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5a1b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a1b2-105">Syntax</span></span>

<span data-ttu-id="5a1b2-106">КГ (** *значение* **, ** *cyID* **)</span><span class="sxs-lookup"><span data-stu-id="5a1b2-106">CY(** *value* **, ** *cyID* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5a1b2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a1b2-107">Parameters</span></span>

|<span data-ttu-id="5a1b2-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-108">**Name**</span></span>|<span data-ttu-id="5a1b2-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-109">**Required/Optional**</span></span>|<span data-ttu-id="5a1b2-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-110">**Data Type**</span></span>|<span data-ttu-id="5a1b2-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5a1b2-112">_value_</span><span class="sxs-lookup"><span data-stu-id="5a1b2-112">_value_</span></span> <br/> |<span data-ttu-id="5a1b2-113">Optional</span><span class="sxs-lookup"><span data-stu-id="5a1b2-113">Optional</span></span>  <br/> |<span data-ttu-id="5a1b2-114">**Число или строка**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-114">**Number or String**</span></span> <br/> |<span data-ttu-id="5a1b2-115">Номер или строку, которая включает в себя форматирование конкретной валюте.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="5a1b2-116">Если не указан, к денежному значению отформатированное в соответствии с денежный в язык и региональные параметры системы.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="5a1b2-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="5a1b2-117">_cyID_</span></span> <br/> |<span data-ttu-id="5a1b2-118">Optional</span><span class="sxs-lookup"><span data-stu-id="5a1b2-118">Optional</span></span>  <br/> |<span data-ttu-id="5a1b2-119">**Число**</span><span class="sxs-lookup"><span data-stu-id="5a1b2-119">**Number**</span></span> <br/> |<span data-ttu-id="5a1b2-120">Идентификатор числовое валюты или трехзначный строка в кавычках для аббревиатура ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a1b2-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="5a1b2-121">Remarks</span></span>

<span data-ttu-id="5a1b2-122">Чтобы указать другую валюту, необходимо включить действительный _cyID_.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="5a1b2-123">Полный список представлен [о константы валюты](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5a1b2-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="5a1b2-124">Если _значение_ несовместимо с типом назначенного валюты, или если указан недопустимый аргумент, например «не число» будет указано, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5a1b2-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="5a1b2-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-125">error is returned.</span></span> <span data-ttu-id="5a1b2-126">Если _значение_ больше, чем 922337203685477,5807 или меньше, чем -922,337,203,685,477.5808, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5a1b2-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="5a1b2-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-127">error is returned.</span></span> 
  
<span data-ttu-id="5a1b2-128">Для улучшения точности при работе с очень большой денежными значениями, включая долей единиц, таких как триллион 3.6 используйте строковые аргументы для _значения_.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="5a1b2-129">Указание недопустимый _cyID_ возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5a1b2-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a1b2-130">Example 1</span></span>

<span data-ttu-id="5a1b2-131">Если язык и региональные параметры пользователя укажите долларов США.</span><span class="sxs-lookup"><span data-stu-id="5a1b2-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="5a1b2-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="5a1b2-132">CY(999998.993)</span></span>
  
<span data-ttu-id="5a1b2-133">Возвращает $999,998.99</span><span class="sxs-lookup"><span data-stu-id="5a1b2-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5a1b2-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a1b2-134">Example 2</span></span>

<span data-ttu-id="5a1b2-135">КГ (12345678.993 "ДОЛЛАРОВ США")</span><span class="sxs-lookup"><span data-stu-id="5a1b2-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="5a1b2-136">Возвращает $12,345,678.99</span><span class="sxs-lookup"><span data-stu-id="5a1b2-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5a1b2-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5a1b2-137">Example 3</span></span>

<span data-ttu-id="5a1b2-138">КГ (12345678.993 "ДЕМОКРАТИЧЕСКАЯ")</span><span class="sxs-lookup"><span data-stu-id="5a1b2-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="5a1b2-139">Возвращает 12,345,678.99 Демократическая</span><span class="sxs-lookup"><span data-stu-id="5a1b2-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="5a1b2-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5a1b2-140">Example 4</span></span>

<span data-ttu-id="5a1b2-141">КГ (12345678.7832 "XXX")</span><span class="sxs-lookup"><span data-stu-id="5a1b2-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="5a1b2-142">Возвращает 12,345,678.78</span><span class="sxs-lookup"><span data-stu-id="5a1b2-142">Returns 12,345,678.78</span></span>
  

