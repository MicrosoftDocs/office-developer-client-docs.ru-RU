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
description: Возвращает значение валюты.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433558"
---
# <a name="cy-function"></a><span data-ttu-id="a7f5a-103">Функция CY</span><span class="sxs-lookup"><span data-stu-id="a7f5a-103">CY Function</span></span>

<span data-ttu-id="a7f5a-104">Возвращает значение валюты.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a7f5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7f5a-105">Syntax</span></span>

<span data-ttu-id="a7f5a-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a7f5a-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7f5a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7f5a-107">Parameters</span></span>

|<span data-ttu-id="a7f5a-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-108">**Name**</span></span>|<span data-ttu-id="a7f5a-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-109">**Required/Optional**</span></span>|<span data-ttu-id="a7f5a-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-110">**Data Type**</span></span>|<span data-ttu-id="a7f5a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7f5a-112">_value_</span><span class="sxs-lookup"><span data-stu-id="a7f5a-112">_value_</span></span> <br/> |<span data-ttu-id="a7f5a-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="a7f5a-113">Optional</span></span>  <br/> |<span data-ttu-id="a7f5a-114">**Число или строка**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-114">**Number or String**</span></span> <br/> |<span data-ttu-id="a7f5a-115">Число или строка, включаемая форматирование для определенной валюты.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="a7f5a-116">Если значение не указано, значение валюты отформатировано в соответствии со стилем валюты в параметрах языка и региона системы.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="a7f5a-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="a7f5a-117">_cyID_</span></span> <br/> |<span data-ttu-id="a7f5a-118">Необязательна</span><span class="sxs-lookup"><span data-stu-id="a7f5a-118">Optional</span></span>  <br/> |<span data-ttu-id="a7f5a-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-119">**Number**</span></span> <br/> |<span data-ttu-id="a7f5a-120">Числовая валюта или трех символьная строка в кавычках для аббревиатуры ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f5a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7f5a-121">Remarks</span></span>

<span data-ttu-id="a7f5a-122">Чтобы указать другую валюту, необходимо указать допустимый _cyID._</span><span class="sxs-lookup"><span data-stu-id="a7f5a-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="a7f5a-123">Список см. в [списке "О константах валюты".](about-currency-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a7f5a-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="a7f5a-124">Если  _значение_ несовместимо с указанным типом валюты или указан недопустимый аргумент, например "не число", #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a7f5a-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="a7f5a-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-125">error is returned.</span></span> <span data-ttu-id="a7f5a-126">Если  значение больше 922 337 203 685 477,5807 или меньше -922 337 203 685 477,5808, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a7f5a-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="a7f5a-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-127">error is returned.</span></span> 
  
<span data-ttu-id="a7f5a-128">Для более точной точности с очень большими значениями валюты, которые включают дробные части единицы, например 3,6- и 3,6-</span><span class="sxs-lookup"><span data-stu-id="a7f5a-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="a7f5a-129">При указании  _недопустимого cyID_ возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a7f5a-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a7f5a-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7f5a-130">Example 1</span></span>

<span data-ttu-id="a7f5a-131">Если в параметрах языка и региона пользователя указаны доллара США:</span><span class="sxs-lookup"><span data-stu-id="a7f5a-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="a7f5a-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="a7f5a-132">CY(999998.993)</span></span>
  
<span data-ttu-id="a7f5a-133">Возвращает 999 998,99 долларов США</span><span class="sxs-lookup"><span data-stu-id="a7f5a-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a7f5a-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a7f5a-134">Example 2</span></span>

<span data-ttu-id="a7f5a-135">CY(12345678.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="a7f5a-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="a7f5a-136">Возвращает 12 345 678,99 долларов США</span><span class="sxs-lookup"><span data-stu-id="a7f5a-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a7f5a-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a7f5a-137">Example 3</span></span>

<span data-ttu-id="a7f5a-138">CY(12345678.993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="a7f5a-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="a7f5a-139">Возвращает 12 345 678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="a7f5a-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="a7f5a-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a7f5a-140">Example 4</span></span>

<span data-ttu-id="a7f5a-141">CY(12345678.7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="a7f5a-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="a7f5a-142">Возвращает 12 345 678,78</span><span class="sxs-lookup"><span data-stu-id="a7f5a-142">Returns 12,345,678.78</span></span>
  

