---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Возвращает ряд от 1 до 12, которое представляет месяц.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431976"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="19501-103">MONTH Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="19501-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="19501-104">Возвращает ряд от 1 до 12, которое представляет месяц.</span><span class="sxs-lookup"><span data-stu-id="19501-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="19501-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19501-105">Syntax</span></span>

<span data-ttu-id="19501-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="19501-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="19501-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="19501-107">Parameters</span></span>

|<span data-ttu-id="19501-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="19501-108">**Name**</span></span>|<span data-ttu-id="19501-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="19501-109">**Required/Optional**</span></span>|<span data-ttu-id="19501-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="19501-110">**Data Type**</span></span>|<span data-ttu-id="19501-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19501-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="19501-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="19501-112">_datetime_</span></span> <br/> |<span data-ttu-id="19501-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="19501-113">Required</span></span>  <br/> |<span data-ttu-id="19501-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="19501-114">**String**</span></span> <br/> |<span data-ttu-id="19501-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="19501-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="19501-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="19501-116">_expression_</span></span> <br/> |<span data-ttu-id="19501-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="19501-117">Required</span></span>  <br/> |<span data-ttu-id="19501-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="19501-118">**String**</span></span> <br/> | <span data-ttu-id="19501-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="19501-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="19501-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="19501-120">_lcid_</span></span> <br/> |<span data-ttu-id="19501-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="19501-121">Optional</span></span>  <br/> |<span data-ttu-id="19501-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="19501-122">**Number**</span></span> <br/> |<span data-ttu-id="19501-123">Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="19501-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="19501-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="19501-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="19501-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19501-125">Return value</span></span>

<span data-ttu-id="19501-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="19501-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19501-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="19501-127">Remarks</span></span>

<span data-ttu-id="19501-128">Компонент времени _даты и выражения_ _удаляется._</span><span class="sxs-lookup"><span data-stu-id="19501-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="19501-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19501-129">No rounding is done.</span></span> <span data-ttu-id="19501-130">Если входная строка отсутствует или не может быть преобразована в допустимый результат, функция MONTH возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19501-130">If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="19501-131">Возвращаемая величина форматирована в соответствии с кратким стилем даты, установленным текущими региональными настройками системы.</span><span class="sxs-lookup"><span data-stu-id="19501-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="19501-132">Функция MONTH также принимает одно число  для выражения, где значительная часть результата представляет количество дней с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="19501-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="19501-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19501-133">Example 1</span></span>

<span data-ttu-id="19501-134">MONTH ("30 мая 1999 г., 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="19501-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="19501-135">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="19501-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="19501-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="19501-136">Example 2</span></span>

<span data-ttu-id="19501-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="19501-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="19501-138">Возвращает 6.</span><span class="sxs-lookup"><span data-stu-id="19501-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="19501-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="19501-139">Example 3</span></span>

<span data-ttu-id="19501-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="19501-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="19501-141">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="19501-141">Returns 5.</span></span>
  

