---
title: Функция DAYOFYEAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Возвращает целое число от 1 до 366, представляющее собой порядковый день года в значении даты и времени или выражении. Функция DAYOFYEAR использует григорианский календарь.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439453"
---
# <a name="dayofyear-function"></a><span data-ttu-id="de0ab-104">Функция DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="de0ab-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="de0ab-105">Возвращает целое число от 1 до 366, представляющее собой порядковый день года в _значении даты и времени_ или _выражении_.</span><span class="sxs-lookup"><span data-stu-id="de0ab-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="de0ab-106">Функция DAYOFYEAR использует григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="de0ab-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="de0ab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de0ab-107">Syntax</span></span>

<span data-ttu-id="de0ab-108">DAYOFYEAR ("\* \* *DateTime* \* \*" | \* \* *выражение* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="de0ab-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de0ab-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="de0ab-109">Parameters</span></span>

|<span data-ttu-id="de0ab-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="de0ab-110">**Name**</span></span>|<span data-ttu-id="de0ab-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="de0ab-111">**Required/Optional**</span></span>|<span data-ttu-id="de0ab-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="de0ab-112">**Data Type**</span></span>|<span data-ttu-id="de0ab-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de0ab-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de0ab-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="de0ab-114">_datetime_</span></span> <br/> |<span data-ttu-id="de0ab-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="de0ab-115">Required</span></span>  <br/> |<span data-ttu-id="de0ab-116">**String**</span><span class="sxs-lookup"><span data-stu-id="de0ab-116">**String**</span></span> <br/> |<span data-ttu-id="de0ab-117">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="de0ab-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="de0ab-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="de0ab-118">_expression_</span></span> <br/> |<span data-ttu-id="de0ab-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="de0ab-119">Required</span></span>  <br/> |<span data-ttu-id="de0ab-120">**String**</span><span class="sxs-lookup"><span data-stu-id="de0ab-120">**String**</span></span> <br/> |<span data-ttu-id="de0ab-121">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="de0ab-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="de0ab-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="de0ab-122">_lcid_</span></span> <br/> |<span data-ttu-id="de0ab-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="de0ab-123">Optional</span></span>  <br/> |<span data-ttu-id="de0ab-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="de0ab-124">**Number**</span></span> <br/> |<span data-ttu-id="de0ab-125">Задает идентификатор языкового стандарта, который будет использоваться при оценке нелокальной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="de0ab-125">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="de0ab-126">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="de0ab-126">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="de0ab-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de0ab-127">Return value</span></span>

<span data-ttu-id="de0ab-128">Целое число</span><span class="sxs-lookup"><span data-stu-id="de0ab-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de0ab-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="de0ab-129">Remarks</span></span>

<span data-ttu-id="de0ab-130">Любой компонент времени в _DateTime_ или _выражении_ отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="de0ab-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="de0ab-131">Результат соответствует 1 января 31 декабря.</span><span class="sxs-lookup"><span data-stu-id="de0ab-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="de0ab-132">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de0ab-132">No rounding is done.</span></span> <span data-ttu-id="de0ab-133">Если _значение DateTime_ отсутствует или не может интерпретироваться как допустимое значение даты или времени, функция возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="de0ab-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="de0ab-134">Функция DAYOFYEAR также принимает одно числовое значение для _выражения_ , где целая часть результата представляет количество дней с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="de0ab-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="de0ab-135">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de0ab-135">Example 1</span></span>

<span data-ttu-id="de0ab-136">DAYOFYEAR ("30 мая, 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="de0ab-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="de0ab-137">Возвращает 150.</span><span class="sxs-lookup"><span data-stu-id="de0ab-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="de0ab-138">Пример 2</span><span class="sxs-lookup"><span data-stu-id="de0ab-138">Example 2</span></span>

<span data-ttu-id="de0ab-139">DAYOFYEAR ("ДАТАЗНАЧ" ("30 мая 1997") + 7 ED.)</span><span class="sxs-lookup"><span data-stu-id="de0ab-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="de0ab-140">Возвращает 157.</span><span class="sxs-lookup"><span data-stu-id="de0ab-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="de0ab-141">Пример 3</span><span class="sxs-lookup"><span data-stu-id="de0ab-141">Example 3</span></span>

<span data-ttu-id="de0ab-142">DAYOFYEAR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="de0ab-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="de0ab-143">Возвращает 150.</span><span class="sxs-lookup"><span data-stu-id="de0ab-143">Returns 150.</span></span>
  

