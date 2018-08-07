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
description: Возвращает целое число от 1-7, представляющее день недели в даты и времени или выражение.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815166"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="991fd-103">WEEKDAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="991fd-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="991fd-104">Возвращает целое число от 1-7, представляющее день недели в _даты и времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="991fd-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="991fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="991fd-105">Syntax</span></span>

<span data-ttu-id="991fd-106">День НЕДЕЛИ ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="991fd-106">WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="991fd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="991fd-107">Parameters</span></span>

|<span data-ttu-id="991fd-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="991fd-108">**Name**</span></span>|<span data-ttu-id="991fd-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="991fd-109">**Required/Optional**</span></span>|<span data-ttu-id="991fd-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="991fd-110">**Data Type**</span></span>|<span data-ttu-id="991fd-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="991fd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="991fd-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="991fd-112">_datetime_</span></span> <br/> |<span data-ttu-id="991fd-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="991fd-113">Required</span></span>  <br/> |<span data-ttu-id="991fd-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="991fd-114">**String**</span></span> <br/> | <span data-ttu-id="991fd-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="991fd-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="991fd-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="991fd-116">_expression_</span></span> <br/> |<span data-ttu-id="991fd-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="991fd-117">Required</span></span>  <br/> |<span data-ttu-id="991fd-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="991fd-118">**Varies**</span></span> <br/> |<span data-ttu-id="991fd-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="991fd-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="991fd-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="991fd-120">_lcid_</span></span> <br/> |<span data-ttu-id="991fd-121">Optional</span><span class="sxs-lookup"><span data-stu-id="991fd-121">Optional</span></span>  <br/> |<span data-ttu-id="991fd-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="991fd-122">**Numeric**</span></span> <br/> |<span data-ttu-id="991fd-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="991fd-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="991fd-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="991fd-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="991fd-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="991fd-125">Return value</span></span>

<span data-ttu-id="991fd-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="991fd-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="991fd-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="991fd-127">Remarks</span></span>

<span data-ttu-id="991fd-128">Компонент времени в _даты и времени_ или _выражение,_ удаляются.</span><span class="sxs-lookup"><span data-stu-id="991fd-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="991fd-129">Результат соответствует понедельника воскресенье (7) (1).</span><span class="sxs-lookup"><span data-stu-id="991fd-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="991fd-130">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="991fd-130">No rounding is done.</span></span> <span data-ttu-id="991fd-131">Если _даты и времени_ , отсутствует или не может использоваться как допустимая дата или время, функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="991fd-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="991fd-132">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="991fd-132">error.</span></span> 
  
<span data-ttu-id="991fd-133">Функция WEEKDAY также принимает одно значение номеров для _выражения_ , где целую часть результата представляет число дней, прошедших с 30 декабря 1899.</span><span class="sxs-lookup"><span data-stu-id="991fd-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="991fd-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="991fd-134">Example 1</span></span>

<span data-ttu-id="991fd-135">День НЕДЕЛИ ("30 мая 1999 г.")</span><span class="sxs-lookup"><span data-stu-id="991fd-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="991fd-136">Возвращает 7.</span><span class="sxs-lookup"><span data-stu-id="991fd-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="991fd-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="991fd-137">Example 2</span></span>

<span data-ttu-id="991fd-138">День НЕДЕЛИ (DATEVALUE ("30 мая 1999 г.") + 2 ed.)</span><span class="sxs-lookup"><span data-stu-id="991fd-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="991fd-139">Возвращает 2.</span><span class="sxs-lookup"><span data-stu-id="991fd-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="991fd-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="991fd-140">Example 3</span></span>

<span data-ttu-id="991fd-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="991fd-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="991fd-142">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="991fd-142">Returns 4.</span></span>
  

