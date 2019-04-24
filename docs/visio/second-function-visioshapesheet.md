---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Возвращает целое число от 0 до 59, которое представляет компонент секунд в значении даты и времени или выражении.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332790"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="043e3-103">SECOND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="043e3-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="043e3-104">Возвращает целое число от 0 до 59, которое представляет компонент секунд в _значении даты и времени_ или _выражении_.</span><span class="sxs-lookup"><span data-stu-id="043e3-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="043e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="043e3-105">Syntax</span></span>

<span data-ttu-id="043e3-106">SECOND ("\* \* *DateTime* \* \*" | \* \* *выражение* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="043e3-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="043e3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="043e3-107">Parameters</span></span>

|<span data-ttu-id="043e3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="043e3-108">**Name**</span></span>|<span data-ttu-id="043e3-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="043e3-109">**Required/Optional**</span></span>|<span data-ttu-id="043e3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="043e3-110">**Data Type**</span></span>|<span data-ttu-id="043e3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043e3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="043e3-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="043e3-112">_datetime_</span></span> <br/> |<span data-ttu-id="043e3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="043e3-113">Required</span></span>  <br/> |<span data-ttu-id="043e3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="043e3-114">**String**</span></span> <br/> |<span data-ttu-id="043e3-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="043e3-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="043e3-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="043e3-116">_expression_</span></span> <br/> |<span data-ttu-id="043e3-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="043e3-117">Required</span></span>  <br/> |<span data-ttu-id="043e3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="043e3-118">**String**</span></span> <br/> | <span data-ttu-id="043e3-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="043e3-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="043e3-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="043e3-120">_lcid_</span></span> <br/> |<span data-ttu-id="043e3-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="043e3-121">Optional</span></span>  <br/> |<span data-ttu-id="043e3-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="043e3-122">**Numeric**</span></span> <br/> |<span data-ttu-id="043e3-123">Идентификатор языкового стандарта, который будет использоваться при оценке нелокальной _даты и времени_.</span><span class="sxs-lookup"><span data-stu-id="043e3-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="043e3-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="043e3-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="043e3-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="043e3-125">Return value</span></span>

<span data-ttu-id="043e3-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="043e3-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="043e3-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="043e3-127">Remarks</span></span>

<span data-ttu-id="043e3-128">Компонент даты в _DateTime_ или _выражении_ отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="043e3-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="043e3-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="043e3-129">No rounding is done.</span></span> <span data-ttu-id="043e3-130">Если _DateTime_ отсутствует или не может быть преобразован в допустимый результат, эта функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="043e3-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="043e3-131">Вторая функция также принимает одно числовое значение для _выражения_ , где дробная часть результата представляет часть дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="043e3-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="043e3-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="043e3-132">Example 1</span></span>

<span data-ttu-id="043e3-133">СЕКУНДА ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="043e3-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="043e3-134">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="043e3-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="043e3-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="043e3-135">Example 2</span></span>

<span data-ttu-id="043e3-136">SECOND (TIMEVALUE ("30 мая, 1996 12:07:45") + 7 ES.)</span><span class="sxs-lookup"><span data-stu-id="043e3-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="043e3-137">Возвращает 52.</span><span class="sxs-lookup"><span data-stu-id="043e3-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="043e3-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="043e3-138">Example 3</span></span>

<span data-ttu-id="043e3-139">СЕКУНДА (0.6337)</span><span class="sxs-lookup"><span data-stu-id="043e3-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="043e3-140">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="043e3-140">Returns 32.</span></span>
  

