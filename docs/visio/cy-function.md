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
# <a name="cy-function"></a><span data-ttu-id="ec115-103">Функция CY</span><span class="sxs-lookup"><span data-stu-id="ec115-103">CY Function</span></span>

<span data-ttu-id="ec115-104">Возвращает значение валюты.</span><span class="sxs-lookup"><span data-stu-id="ec115-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ec115-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec115-105">Syntax</span></span>

<span data-ttu-id="ec115-106">CY(\*\* *значение* \*\*, \*\* *cyID* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ec115-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ec115-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec115-107">Parameters</span></span>

|<span data-ttu-id="ec115-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ec115-108">**Name**</span></span>|<span data-ttu-id="ec115-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ec115-109">**Required/Optional**</span></span>|<span data-ttu-id="ec115-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ec115-110">**Data Type**</span></span>|<span data-ttu-id="ec115-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec115-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ec115-112">_value_</span><span class="sxs-lookup"><span data-stu-id="ec115-112">_value_</span></span> <br/> |<span data-ttu-id="ec115-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ec115-113">Optional</span></span>  <br/> |<span data-ttu-id="ec115-114">**Число или строка**</span><span class="sxs-lookup"><span data-stu-id="ec115-114">**Number or String**</span></span> <br/> |<span data-ttu-id="ec115-115">Номер или строка, которая включает форматирование с определенной валютой.</span><span class="sxs-lookup"><span data-stu-id="ec115-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="ec115-116">Если не указано, значение валюты отформатировано в соответствии со стилем валюты в параметрах регион и язык системы.</span><span class="sxs-lookup"><span data-stu-id="ec115-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="ec115-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="ec115-117">_cyID_</span></span> <br/> |<span data-ttu-id="ec115-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ec115-118">Optional</span></span>  <br/> |<span data-ttu-id="ec115-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="ec115-119">**Number**</span></span> <br/> |<span data-ttu-id="ec115-120">Цифровой ИД валюты или строка с тремя символами, закавычка для аббревиатуры ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="ec115-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec115-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec115-121">Remarks</span></span>

<span data-ttu-id="ec115-122">Чтобы указать другую валюту, необходимо включить допустимый _cyID._</span><span class="sxs-lookup"><span data-stu-id="ec115-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="ec115-123">Список см. в [рублях О константах валюты.](about-currency-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ec115-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="ec115-124">Если  _значение_ несовместимо с указанным типом валюты или если указан недействительный аргумент, например "не номер", #VALUE!</span><span class="sxs-lookup"><span data-stu-id="ec115-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="ec115-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ec115-125">error is returned.</span></span> <span data-ttu-id="ec115-126">Если  значение больше 922 337 203 685 477,5807 или меньше -922 337 203 685 477,5808, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="ec115-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="ec115-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ec115-127">error is returned.</span></span> 
  
<span data-ttu-id="ec115-128">Для улучшения точности с очень большими значениями валюты, которые включают фракции единицы, например 3,6 трлн, используйте аргументы строки для  _значения_.</span><span class="sxs-lookup"><span data-stu-id="ec115-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="ec115-129">Указание  _недействительных cyID_ возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ec115-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ec115-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec115-130">Example 1</span></span>

<span data-ttu-id="ec115-131">Если параметры региона и языка пользователя указывают доллары США:</span><span class="sxs-lookup"><span data-stu-id="ec115-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="ec115-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="ec115-132">CY(999998.993)</span></span>
  
<span data-ttu-id="ec115-133">Возвращает $999 998.99</span><span class="sxs-lookup"><span data-stu-id="ec115-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ec115-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec115-134">Example 2</span></span>

<span data-ttu-id="ec115-135">CY (12345678.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="ec115-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="ec115-136">Возвращает $12 345 678.99</span><span class="sxs-lookup"><span data-stu-id="ec115-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ec115-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ec115-137">Example 3</span></span>

<span data-ttu-id="ec115-138">CY (12345678.993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="ec115-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="ec115-139">Возвращает 12 345 678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="ec115-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ec115-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ec115-140">Example 4</span></span>

<span data-ttu-id="ec115-141">CY (12345678.7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="ec115-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="ec115-142">Возвращает 12 345 678,78</span><span class="sxs-lookup"><span data-stu-id="ec115-142">Returns 12,345,678.78</span></span>
  

