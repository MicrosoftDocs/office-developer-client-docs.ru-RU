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
description: Возвращает компоненты от 0 до 59, которые представляют собой компонент секунд даты или выражения.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404878"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="d1526-103">SECOND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d1526-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d1526-104">Возвращает компоненты от 0 до 59, которые представляют собой компонент секунд времени даты _или_ _выражения._</span><span class="sxs-lookup"><span data-stu-id="d1526-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d1526-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1526-105">Syntax</span></span>

<span data-ttu-id="d1526-106">SECOND(" \*\* *datetime* \*\* "| \*\* *выражение* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="d1526-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d1526-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1526-107">Parameters</span></span>

|<span data-ttu-id="d1526-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d1526-108">**Name**</span></span>|<span data-ttu-id="d1526-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d1526-109">**Required/Optional**</span></span>|<span data-ttu-id="d1526-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d1526-110">**Data Type**</span></span>|<span data-ttu-id="d1526-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1526-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1526-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="d1526-112">_datetime_</span></span> <br/> |<span data-ttu-id="d1526-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d1526-113">Required</span></span>  <br/> |<span data-ttu-id="d1526-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d1526-114">**String**</span></span> <br/> |<span data-ttu-id="d1526-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="d1526-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d1526-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d1526-116">_expression_</span></span> <br/> |<span data-ttu-id="d1526-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d1526-117">Required</span></span>  <br/> |<span data-ttu-id="d1526-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d1526-118">**String**</span></span> <br/> | <span data-ttu-id="d1526-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="d1526-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d1526-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d1526-120">_lcid_</span></span> <br/> |<span data-ttu-id="d1526-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d1526-121">Optional</span></span>  <br/> |<span data-ttu-id="d1526-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="d1526-122">**Numeric**</span></span> <br/> |<span data-ttu-id="d1526-123">Идентификатор locale, который будет использоваться для оценки нелокального _времени даты._</span><span class="sxs-lookup"><span data-stu-id="d1526-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="d1526-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="d1526-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d1526-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1526-125">Return value</span></span>

<span data-ttu-id="d1526-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="d1526-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1526-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1526-127">Remarks</span></span>

<span data-ttu-id="d1526-128">Компонент даты в  _дате_ или  _выражении_ удаляется.</span><span class="sxs-lookup"><span data-stu-id="d1526-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d1526-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1526-129">No rounding is done.</span></span> <span data-ttu-id="d1526-130">Если  _дата отсутствует_ или не может быть преобразована в допустимый результат, эта функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d1526-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="d1526-131">Функция SECOND также принимает одно значение  номера для выражения, где десятичная часть результата представляет долю дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="d1526-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d1526-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1526-132">Example 1</span></span>

<span data-ttu-id="d1526-133">SECOND ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="d1526-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="d1526-134">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="d1526-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d1526-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d1526-135">Example 2</span></span>

<span data-ttu-id="d1526-136">SECOND (TIMEVALUE("30 мая 1996 г. 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="d1526-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="d1526-137">Возвращает 52.</span><span class="sxs-lookup"><span data-stu-id="d1526-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d1526-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d1526-138">Example 3</span></span>

<span data-ttu-id="d1526-139">SECOND (0.6337)</span><span class="sxs-lookup"><span data-stu-id="d1526-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="d1526-140">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="d1526-140">Returns 32.</span></span>
  

