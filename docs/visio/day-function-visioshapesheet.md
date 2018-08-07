---
title: DAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Возвращает целое число от 1 до 31, представляющее день в даты и времени или выражение. Функция DAY использует григорианский календарь.
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813575"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="fd308-104">DAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fd308-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fd308-105">Возвращает целое число от 1 до 31, представляющее день в _даты и времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="fd308-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="fd308-106">Функция DAY использует григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="fd308-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fd308-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd308-107">Syntax</span></span>

<span data-ttu-id="fd308-108">ДЕНЬ ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="fd308-108">DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fd308-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd308-109">Parameters</span></span>

|<span data-ttu-id="fd308-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fd308-110">**Name**</span></span>|<span data-ttu-id="fd308-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="fd308-111">**Required/Optional**</span></span>|<span data-ttu-id="fd308-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fd308-112">**Data Type**</span></span>|<span data-ttu-id="fd308-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fd308-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fd308-114">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="fd308-114">_datetime_</span></span> <br/> |<span data-ttu-id="fd308-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fd308-115">Required</span></span>  <br/> |<span data-ttu-id="fd308-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="fd308-116">**String**</span></span> <br/> |<span data-ttu-id="fd308-117">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="fd308-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="fd308-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="fd308-118">_expression_</span></span> <br/> |<span data-ttu-id="fd308-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fd308-119">Required</span></span>  <br/> |<span data-ttu-id="fd308-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="fd308-120">**String**</span></span> <br/> |<span data-ttu-id="fd308-121">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="fd308-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="fd308-122">_код языка_</span><span class="sxs-lookup"><span data-stu-id="fd308-122">_lcid_</span></span> <br/> |<span data-ttu-id="fd308-123">Optional</span><span class="sxs-lookup"><span data-stu-id="fd308-123">Optional</span></span>  <br/> |<span data-ttu-id="fd308-124">**Число**</span><span class="sxs-lookup"><span data-stu-id="fd308-124">**Number**</span></span> <br/> |<span data-ttu-id="fd308-125">Задает идентификатор языкового стандарта для использования при оценке нелокальных datetime.</span><span class="sxs-lookup"><span data-stu-id="fd308-125">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="fd308-126">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="fd308-126">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fd308-127">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="fd308-127">Return value</span></span>

<span data-ttu-id="fd308-128">Целое число</span><span class="sxs-lookup"><span data-stu-id="fd308-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd308-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="fd308-129">Remarks</span></span>

<span data-ttu-id="fd308-130">Любой компонент времени в _даты и времени_ или _выражение,_ удаляются.</span><span class="sxs-lookup"><span data-stu-id="fd308-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="fd308-131">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd308-131">No rounding is done.</span></span> <span data-ttu-id="fd308-132">Если _даты и времени_ , отсутствует или не может быть преобразована допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fd308-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="fd308-133">Функция DAY также принимает одно значение номеров для _выражения_ , где целую часть результата представляет число дней, прошедших с 30 декабря 1899.</span><span class="sxs-lookup"><span data-stu-id="fd308-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fd308-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd308-134">Example 1</span></span>

<span data-ttu-id="fd308-135">ДЕНЬ ("30 мая 1997 г., 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="fd308-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="fd308-136">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="fd308-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fd308-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fd308-137">Example 2</span></span>

<span data-ttu-id="fd308-138">ДЕНЬ (DATEVALUE ("30 мая 1997 г.") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="fd308-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="fd308-139">Возвращает 6.</span><span class="sxs-lookup"><span data-stu-id="fd308-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fd308-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fd308-140">Example 3</span></span>

<span data-ttu-id="fd308-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="fd308-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="fd308-142">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="fd308-142">Returns 30.</span></span>
  

