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
description: Возвращает integer, от 1 до 31, представляющее день в даты и времени или выражение. Функция DAY использует григорианский календарь.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360299"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="460d0-104">DAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="460d0-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="460d0-105">Возвращает integer, от 1 до 31, представляющее день в  _даты и времени_ или  _выражение_.</span><span class="sxs-lookup"><span data-stu-id="460d0-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="460d0-106">Функция DAY использует григорианский календарь.</span><span class="sxs-lookup"><span data-stu-id="460d0-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="460d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="460d0-107">Syntax</span></span>

<span data-ttu-id="460d0-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="460d0-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="460d0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="460d0-109">Parameters</span></span>

|<span data-ttu-id="460d0-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="460d0-110">**Name**</span></span>|<span data-ttu-id="460d0-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="460d0-111">**Required/Optional**</span></span>|<span data-ttu-id="460d0-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="460d0-112">**Data Type**</span></span>|<span data-ttu-id="460d0-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="460d0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="460d0-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="460d0-114">_datetime_</span></span> <br/> |<span data-ttu-id="460d0-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="460d0-115">Required</span></span>  <br/> |<span data-ttu-id="460d0-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="460d0-116">**String**</span></span> <br/> |<span data-ttu-id="460d0-117">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="460d0-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="460d0-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="460d0-118">_expression_</span></span> <br/> |<span data-ttu-id="460d0-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="460d0-119">Required</span></span>  <br/> |<span data-ttu-id="460d0-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="460d0-120">**String**</span></span> <br/> |<span data-ttu-id="460d0-121">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="460d0-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="460d0-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="460d0-122">_lcid_</span></span> <br/> |<span data-ttu-id="460d0-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="460d0-123">Optional</span></span>  <br/> |<span data-ttu-id="460d0-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="460d0-124">**Number**</span></span> <br/> |<span data-ttu-id="460d0-125">Указывает идентификатор региональных даты, используемый при оценке нелокализованного даты и времени.</span><span class="sxs-lookup"><span data-stu-id="460d0-125">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="460d0-126">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="460d0-126">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="460d0-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="460d0-127">Return value</span></span>

<span data-ttu-id="460d0-128">Целое число</span><span class="sxs-lookup"><span data-stu-id="460d0-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="460d0-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="460d0-129">Remarks</span></span>

<span data-ttu-id="460d0-130">Любой компонент времени в  _дате или_  _выражении_ удаляется.</span><span class="sxs-lookup"><span data-stu-id="460d0-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="460d0-131">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="460d0-131">No rounding is done.</span></span> <span data-ttu-id="460d0-132">Если  _дата-время_ отсутствует или не удается преобразовать в допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="460d0-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="460d0-133">Функция DAY также принимает одно число  для выражения, где значительная часть результата представляет количество дней с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="460d0-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="460d0-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="460d0-134">Example 1</span></span>

<span data-ttu-id="460d0-135">DAY("30 мая 1997 г. 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="460d0-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="460d0-136">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="460d0-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="460d0-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="460d0-137">Example 2</span></span>

<span data-ttu-id="460d0-138">DAY(DATEVALUE("30 мая 1997 г.")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="460d0-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="460d0-139">Возвращает 6.</span><span class="sxs-lookup"><span data-stu-id="460d0-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="460d0-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="460d0-140">Example 3</span></span>

<span data-ttu-id="460d0-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="460d0-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="460d0-142">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="460d0-142">Returns 30.</span></span>
  

