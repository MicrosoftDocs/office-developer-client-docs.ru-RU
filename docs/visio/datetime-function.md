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
description: Возвращает значение даты и времени, даты и времени или выражения.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813562"
---
# <a name="datetime-function"></a><span data-ttu-id="7283e-103">Функция DATETIME</span><span class="sxs-lookup"><span data-stu-id="7283e-103">DATETIME Function</span></span>

<span data-ttu-id="7283e-104">Возвращает значение даты и времени, _даты и времени_ или _выражения_.</span><span class="sxs-lookup"><span data-stu-id="7283e-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7283e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7283e-105">Syntax</span></span>

<span data-ttu-id="7283e-106">Даты и времени ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="7283e-106">DATETIME(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7283e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7283e-107">Parameters</span></span>

|<span data-ttu-id="7283e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7283e-108">**Name**</span></span>|<span data-ttu-id="7283e-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7283e-109">**Required/Optional**</span></span>|<span data-ttu-id="7283e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7283e-110">**Data Type**</span></span>|<span data-ttu-id="7283e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7283e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7283e-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="7283e-112">_datetime_</span></span> <br/> |<span data-ttu-id="7283e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7283e-113">Required</span></span>  <br/> |<span data-ttu-id="7283e-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7283e-114">**String**</span></span> <br/> |<span data-ttu-id="7283e-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="7283e-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="7283e-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="7283e-116">_expression_</span></span> <br/> |<span data-ttu-id="7283e-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7283e-117">Required</span></span>  <br/> |<span data-ttu-id="7283e-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7283e-118">**String**</span></span> <br/> |<span data-ttu-id="7283e-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="7283e-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="7283e-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="7283e-120">_lcid_</span></span> <br/> |<span data-ttu-id="7283e-121">Optional</span><span class="sxs-lookup"><span data-stu-id="7283e-121">Optional</span></span>  <br/> |<span data-ttu-id="7283e-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="7283e-122">**Number**</span></span> <br/> |<span data-ttu-id="7283e-123">Задает идентификатор языкового стандарта для использования при оценке нелокальных datetime.</span><span class="sxs-lookup"><span data-stu-id="7283e-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="7283e-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="7283e-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7283e-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7283e-125">Return value</span></span>

<span data-ttu-id="7283e-126">Даты и времени</span><span class="sxs-lookup"><span data-stu-id="7283e-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7283e-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="7283e-127">Remarks</span></span>

<span data-ttu-id="7283e-128">Если *даты и времени* отсутствует или не может использоваться как даты или времени, даты и времени возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="7283e-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="7283e-129">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="7283e-129">error.</span></span> 
  
<span data-ttu-id="7283e-130">Возвращаемое значение форматируется в соответствии с краткий формат даты и времени стиль в текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="7283e-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="7283e-131">Функции даты и времени также принимает одно значение номеров для *выражения* , где целую часть результата представляет число дней, прошедших с 30 декабря 1899, а дробная часть представляет долю день после полночи.</span><span class="sxs-lookup"><span data-stu-id="7283e-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7283e-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7283e-132">Example 1</span></span>

<span data-ttu-id="7283e-133">Даты и времени ("30 мая 1997 г.") + 5 ed.</span><span class="sxs-lookup"><span data-stu-id="7283e-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="7283e-134">Возвращает значение, представляющее 6/4/1997 г.</span><span class="sxs-lookup"><span data-stu-id="7283e-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7283e-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7283e-135">Example 2</span></span>

<span data-ttu-id="7283e-136">ФОРМАТ (ДАТЫ И ВРЕМЕНИ ("5/20/1997 14:30:45"), «C»)</span><span class="sxs-lookup"><span data-stu-id="7283e-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="7283e-137">Возвращает строку «Вторник 20 мая, 1997 г. 2:30:45 PM.»</span><span class="sxs-lookup"><span data-stu-id="7283e-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7283e-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7283e-138">Example 3</span></span>

<span data-ttu-id="7283e-139">Даты и времени ("1:30 PM 19 июля")</span><span class="sxs-lookup"><span data-stu-id="7283e-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="7283e-140">Возвращает значение, представляющее 7/19/2001 1:30:00 PM (при условии текущего года 2001 г.).</span><span class="sxs-lookup"><span data-stu-id="7283e-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="7283e-141">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7283e-141">Example 4</span></span>

<span data-ttu-id="7283e-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="7283e-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="7283e-143">Возвращает значение, представляющее 5/30/1997 г., 15:12:32 по.</span><span class="sxs-lookup"><span data-stu-id="7283e-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

