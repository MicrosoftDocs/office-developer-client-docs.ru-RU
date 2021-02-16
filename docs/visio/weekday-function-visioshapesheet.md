---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Возвращает integer, от 1 до 7, представляющее день недели в дате или выражении.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404808"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="dbfd3-103">WEEKDAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="dbfd3-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="dbfd3-104">Возвращает integer, от 1 до 7, представляющее день недели в  _даты и времени_ или  _выражение_.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dbfd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbfd3-105">Syntax</span></span>

<span data-ttu-id="dbfd3-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="dbfd3-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dbfd3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbfd3-107">Parameters</span></span>

|<span data-ttu-id="dbfd3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-108">**Name**</span></span>|<span data-ttu-id="dbfd3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-109">**Required/Optional**</span></span>|<span data-ttu-id="dbfd3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-110">**Data Type**</span></span>|<span data-ttu-id="dbfd3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dbfd3-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="dbfd3-112">_datetime_</span></span> <br/> |<span data-ttu-id="dbfd3-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dbfd3-113">Required</span></span>  <br/> |<span data-ttu-id="dbfd3-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-114">**String**</span></span> <br/> | <span data-ttu-id="dbfd3-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="dbfd3-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="dbfd3-116">_expression_</span></span> <br/> |<span data-ttu-id="dbfd3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dbfd3-117">Required</span></span>  <br/> |<span data-ttu-id="dbfd3-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-118">**Varies**</span></span> <br/> |<span data-ttu-id="dbfd3-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="dbfd3-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="dbfd3-120">_lcid_</span></span> <br/> |<span data-ttu-id="dbfd3-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="dbfd3-121">Optional</span></span>  <br/> |<span data-ttu-id="dbfd3-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="dbfd3-122">**Numeric**</span></span> <br/> |<span data-ttu-id="dbfd3-123">Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="dbfd3-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dbfd3-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbfd3-125">Return value</span></span>

<span data-ttu-id="dbfd3-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="dbfd3-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dbfd3-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="dbfd3-127">Remarks</span></span>

<span data-ttu-id="dbfd3-128">Из параметров _datetime_ и _expression_ удаляется компонент времени.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="dbfd3-129">Результат соответствует понедельнику (1) по воскресенье (7).</span><span class="sxs-lookup"><span data-stu-id="dbfd3-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="dbfd3-130">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-130">No rounding is done.</span></span> <span data-ttu-id="dbfd3-131">Если  _дата-время_ отсутствует или не может быть интерпретирована как допустимая дата или время, функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="dbfd3-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="dbfd3-132">error.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-132">error.</span></span> 
  
<span data-ttu-id="dbfd3-133">Функция WEEKDAY также принимает одно число  для выражения, где значительная часть результата представляет количество дней с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dbfd3-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbfd3-134">Example 1</span></span>

<span data-ttu-id="dbfd3-135">WEEKDAY ("30 мая 1999 г.")</span><span class="sxs-lookup"><span data-stu-id="dbfd3-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="dbfd3-136">Возвращает 7.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dbfd3-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dbfd3-137">Example 2</span></span>

<span data-ttu-id="dbfd3-138">WEEKDAY(DATEVALUE("30 мая 1999 г.")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="dbfd3-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="dbfd3-139">Возвращает 2.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dbfd3-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dbfd3-140">Example 3</span></span>

<span data-ttu-id="dbfd3-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="dbfd3-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="dbfd3-142">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="dbfd3-142">Returns 4.</span></span>
  

