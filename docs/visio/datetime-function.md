---
title: Функция DATETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Возвращает значение даты и времени, представленное датой или выражением.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360321"
---
# <a name="datetime-function"></a><span data-ttu-id="59eb2-103">Функция DATETIME</span><span class="sxs-lookup"><span data-stu-id="59eb2-103">DATETIME Function</span></span>

<span data-ttu-id="59eb2-104">Возвращает значение даты и времени, представленное _датой или_ _выражением._</span><span class="sxs-lookup"><span data-stu-id="59eb2-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="59eb2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59eb2-105">Syntax</span></span>

<span data-ttu-id="59eb2-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *выражение* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="59eb2-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="59eb2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="59eb2-107">Parameters</span></span>

|<span data-ttu-id="59eb2-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="59eb2-108">**Name**</span></span>|<span data-ttu-id="59eb2-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="59eb2-109">**Required/Optional**</span></span>|<span data-ttu-id="59eb2-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="59eb2-110">**Data Type**</span></span>|<span data-ttu-id="59eb2-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59eb2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="59eb2-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="59eb2-112">_datetime_</span></span> <br/> |<span data-ttu-id="59eb2-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="59eb2-113">Required</span></span>  <br/> |<span data-ttu-id="59eb2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="59eb2-114">**String**</span></span> <br/> |<span data-ttu-id="59eb2-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="59eb2-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="59eb2-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="59eb2-116">_expression_</span></span> <br/> |<span data-ttu-id="59eb2-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="59eb2-117">Required</span></span>  <br/> |<span data-ttu-id="59eb2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="59eb2-118">**String**</span></span> <br/> |<span data-ttu-id="59eb2-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="59eb2-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="59eb2-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="59eb2-120">_lcid_</span></span> <br/> |<span data-ttu-id="59eb2-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="59eb2-121">Optional</span></span>  <br/> |<span data-ttu-id="59eb2-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="59eb2-122">**Number**</span></span> <br/> |<span data-ttu-id="59eb2-123">Указывает идентификатор локального адреса, который будет использоваться для оценки неместного времени даты.</span><span class="sxs-lookup"><span data-stu-id="59eb2-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="59eb2-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="59eb2-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="59eb2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59eb2-125">Return value</span></span>

<span data-ttu-id="59eb2-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="59eb2-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59eb2-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="59eb2-127">Remarks</span></span>

<span data-ttu-id="59eb2-128">Если  *дата отсутствует*  или не может быть истолкована как допустимая дата или время, DATETIME возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="59eb2-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="59eb2-129">ошибка.</span><span class="sxs-lookup"><span data-stu-id="59eb2-129">error.</span></span> 
  
<span data-ttu-id="59eb2-130">Возвращенное значение отформатировано в соответствии со стилем коротких дат и стилем времени в текущем региональном Параметры.</span><span class="sxs-lookup"><span data-stu-id="59eb2-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="59eb2-131">В функции DATETIME также принимается  одно значение числа для выражения, в котором вся часть результата представляет число дней с 30 декабря 1899 г., а десятичная часть представляет долю дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="59eb2-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="59eb2-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59eb2-132">Example 1</span></span>

<span data-ttu-id="59eb2-133">DATETIME ("30 мая 1997 г.") +5 ed.</span><span class="sxs-lookup"><span data-stu-id="59eb2-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="59eb2-134">Возвращает значение 6/4/1997.</span><span class="sxs-lookup"><span data-stu-id="59eb2-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="59eb2-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59eb2-135">Example 2</span></span>

<span data-ttu-id="59eb2-136">FORMAT (DATETIME ("5/20/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="59eb2-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="59eb2-137">Возвращает строку "Вторник, 20 мая 1997 г. 14:30:45".</span><span class="sxs-lookup"><span data-stu-id="59eb2-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="59eb2-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="59eb2-138">Example 3</span></span>

<span data-ttu-id="59eb2-139">DATETIME ("13:30 19 июля")</span><span class="sxs-lookup"><span data-stu-id="59eb2-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="59eb2-140">Возвращает значение 7/19/2001 по 13:30:00 (если предположить, что текущий год — 2001 г.).</span><span class="sxs-lookup"><span data-stu-id="59eb2-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="59eb2-141">Пример 4</span><span class="sxs-lookup"><span data-stu-id="59eb2-141">Example 4</span></span>

<span data-ttu-id="59eb2-142">DATETIME (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="59eb2-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="59eb2-143">Возвращает значение 5/30/1997 3:12:32 PM.</span><span class="sxs-lookup"><span data-stu-id="59eb2-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

