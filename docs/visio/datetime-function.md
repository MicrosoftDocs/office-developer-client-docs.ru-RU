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
description: Возвращает значение даты и времени, представляемые датой или выражением.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360321"
---
# <a name="datetime-function"></a><span data-ttu-id="db015-103">Функция DATETIME</span><span class="sxs-lookup"><span data-stu-id="db015-103">DATETIME Function</span></span>

<span data-ttu-id="db015-104">Возвращает значение даты и времени, представляемые _датой или_ _выражением._</span><span class="sxs-lookup"><span data-stu-id="db015-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="db015-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db015-105">Syntax</span></span>

<span data-ttu-id="db015-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="db015-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="db015-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="db015-107">Parameters</span></span>

|<span data-ttu-id="db015-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="db015-108">**Name**</span></span>|<span data-ttu-id="db015-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="db015-109">**Required/Optional**</span></span>|<span data-ttu-id="db015-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="db015-110">**Data Type**</span></span>|<span data-ttu-id="db015-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db015-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db015-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="db015-112">_datetime_</span></span> <br/> |<span data-ttu-id="db015-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="db015-113">Required</span></span>  <br/> |<span data-ttu-id="db015-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="db015-114">**String**</span></span> <br/> |<span data-ttu-id="db015-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="db015-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="db015-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="db015-116">_expression_</span></span> <br/> |<span data-ttu-id="db015-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="db015-117">Required</span></span>  <br/> |<span data-ttu-id="db015-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="db015-118">**String**</span></span> <br/> |<span data-ttu-id="db015-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="db015-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="db015-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="db015-120">_lcid_</span></span> <br/> |<span data-ttu-id="db015-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="db015-121">Optional</span></span>  <br/> |<span data-ttu-id="db015-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="db015-122">**Number**</span></span> <br/> |<span data-ttu-id="db015-123">Указывает идентификатор региональных даты, используемый при оценке нелокализованного даты и времени.</span><span class="sxs-lookup"><span data-stu-id="db015-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="db015-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="db015-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="db015-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db015-125">Return value</span></span>

<span data-ttu-id="db015-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="db015-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db015-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="db015-127">Remarks</span></span>

<span data-ttu-id="db015-128">Если  *дата-время*  отсутствует или не может быть интерпретирована как допустимая дата или время, DATETIME возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="db015-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="db015-129">error.</span><span class="sxs-lookup"><span data-stu-id="db015-129">error.</span></span> 
  
<span data-ttu-id="db015-130">Возвращаемая величина форматирована в соответствии со стилем короткой даты и времени в текущих региональных параметрах системы.</span><span class="sxs-lookup"><span data-stu-id="db015-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="db015-131">Функция DATETIME также принимает одно число  для выражения, где значительная часть результата представляет количество дней с 30 декабря 1899 г., а десятичная часть представляет часть дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="db015-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="db015-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db015-132">Example 1</span></span>

<span data-ttu-id="db015-133">DATETIME ("30 мая 1997 г.")+5 ed.</span><span class="sxs-lookup"><span data-stu-id="db015-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="db015-134">Возвращает значение, представляющее 04.06.1997.</span><span class="sxs-lookup"><span data-stu-id="db015-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="db015-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db015-135">Example 2</span></span>

<span data-ttu-id="db015-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="db015-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="db015-137">Возвращает строку "Вторник, 20 мая 1997 г., 14:30:45".</span><span class="sxs-lookup"><span data-stu-id="db015-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="db015-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="db015-138">Example 3</span></span>

<span data-ttu-id="db015-139">DATETIME("13:30 19 июля")</span><span class="sxs-lookup"><span data-stu-id="db015-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="db015-140">Возвращает значение, представляющее 07.19.2001 13:30:00 (при условии, что текущий год — 2001).</span><span class="sxs-lookup"><span data-stu-id="db015-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="db015-141">Пример 4</span><span class="sxs-lookup"><span data-stu-id="db015-141">Example 4</span></span>

<span data-ttu-id="db015-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="db015-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="db015-143">Возвращает значение, представляющее 30.05.1997 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="db015-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

