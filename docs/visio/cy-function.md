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
description: Возвращает значение денежной единицы.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433558"
---
# <a name="cy-function"></a><span data-ttu-id="d9c92-103">Функция CY</span><span class="sxs-lookup"><span data-stu-id="d9c92-103">CY Function</span></span>

<span data-ttu-id="d9c92-104">Возвращает значение денежной единицы.</span><span class="sxs-lookup"><span data-stu-id="d9c92-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d9c92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9c92-105">Syntax</span></span>

<span data-ttu-id="d9c92-106">CY (\* \* *значение* \* \*, \* \* *циид* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d9c92-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d9c92-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9c92-107">Parameters</span></span>

|<span data-ttu-id="d9c92-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d9c92-108">**Name**</span></span>|<span data-ttu-id="d9c92-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d9c92-109">**Required/Optional**</span></span>|<span data-ttu-id="d9c92-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d9c92-110">**Data Type**</span></span>|<span data-ttu-id="d9c92-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9c92-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d9c92-112">_value_</span><span class="sxs-lookup"><span data-stu-id="d9c92-112">_value_</span></span> <br/> |<span data-ttu-id="d9c92-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="d9c92-113">Optional</span></span>  <br/> |<span data-ttu-id="d9c92-114">**Число или строка**</span><span class="sxs-lookup"><span data-stu-id="d9c92-114">**Number or String**</span></span> <br/> |<span data-ttu-id="d9c92-115">Число или строка, включающая в себя форматирование для конкретной валюты.</span><span class="sxs-lookup"><span data-stu-id="d9c92-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="d9c92-116">Если значение не указано, значение валюты форматируется в соответствии со стилем валюты в региональных параметрах системы и языковых параметрах.</span><span class="sxs-lookup"><span data-stu-id="d9c92-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="d9c92-117">_циид_</span><span class="sxs-lookup"><span data-stu-id="d9c92-117">_cyID_</span></span> <br/> |<span data-ttu-id="d9c92-118">Необязательна</span><span class="sxs-lookup"><span data-stu-id="d9c92-118">Optional</span></span>  <br/> |<span data-ttu-id="d9c92-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="d9c92-119">**Number**</span></span> <br/> |<span data-ttu-id="d9c92-120">Числовой идентификатор валюты или строка в кавычках из трех символов для аббревиатуры ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="d9c92-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9c92-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9c92-121">Remarks</span></span>

<span data-ttu-id="d9c92-122">Чтобы указать другую валюту, необходимо включить допустимый _циид_.</span><span class="sxs-lookup"><span data-stu-id="d9c92-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="d9c92-123">Список приведен в разделе [о константах Currency](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d9c92-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="d9c92-124">Если _значение_ несовместимо с определенным типом валюты или указан недопустимый аргумент (например, "не является числом"), то #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d9c92-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="d9c92-125">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d9c92-125">error is returned.</span></span> <span data-ttu-id="d9c92-126">Если _значение_ больше 922 337 203 685 477,5807 или меньше-922 337 203 685 477,5808, то #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d9c92-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="d9c92-127">возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d9c92-127">error is returned.</span></span> 
  
<span data-ttu-id="d9c92-128">Для лучшей точности с очень крупными денежными значениями, включающими дроби единиц измерения, например 3 600 000 000 000, используйте строковые аргументы для _value_.</span><span class="sxs-lookup"><span data-stu-id="d9c92-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="d9c92-129">При указании недопустимого _циид_ возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="d9c92-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d9c92-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9c92-130">Example 1</span></span>

<span data-ttu-id="d9c92-131">Если региональные и языковые параметры пользователя задают доллар США:</span><span class="sxs-lookup"><span data-stu-id="d9c92-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="d9c92-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="d9c92-132">CY(999998.993)</span></span>
  
<span data-ttu-id="d9c92-133">Возвращает $999 998,99</span><span class="sxs-lookup"><span data-stu-id="d9c92-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d9c92-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d9c92-134">Example 2</span></span>

<span data-ttu-id="d9c92-135">CY (12345678.993, "USD")</span><span class="sxs-lookup"><span data-stu-id="d9c92-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="d9c92-136">Возвращает $12 345 678,99</span><span class="sxs-lookup"><span data-stu-id="d9c92-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d9c92-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d9c92-137">Example 3</span></span>

<span data-ttu-id="d9c92-138">CY (12345678.993, "DEM")</span><span class="sxs-lookup"><span data-stu-id="d9c92-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="d9c92-139">Возвращает 12 345 678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="d9c92-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="d9c92-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d9c92-140">Example 4</span></span>

<span data-ttu-id="d9c92-141">CY (12345678.7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="d9c92-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="d9c92-142">Возвращает 12 345 678,78</span><span class="sxs-lookup"><span data-stu-id="d9c92-142">Returns 12,345,678.78</span></span>
  

