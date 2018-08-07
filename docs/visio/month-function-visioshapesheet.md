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
description: Возвращает целое число от 1 до 12, представляющее месяц.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814285"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="cbdc1-103">MONTH Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="cbdc1-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="cbdc1-104">Возвращает целое число от 1 до 12, представляющее месяц.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cbdc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbdc1-105">Syntax</span></span>

<span data-ttu-id="cbdc1-106">МЕСЯЦ ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="cbdc1-106">MONTH(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cbdc1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbdc1-107">Parameters</span></span>

|<span data-ttu-id="cbdc1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-108">**Name**</span></span>|<span data-ttu-id="cbdc1-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-109">**Required/Optional**</span></span>|<span data-ttu-id="cbdc1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-110">**Data Type**</span></span>|<span data-ttu-id="cbdc1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cbdc1-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="cbdc1-112">_datetime_</span></span> <br/> |<span data-ttu-id="cbdc1-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cbdc1-113">Required</span></span>  <br/> |<span data-ttu-id="cbdc1-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-114">**String**</span></span> <br/> |<span data-ttu-id="cbdc1-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="cbdc1-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="cbdc1-116">_expression_</span></span> <br/> |<span data-ttu-id="cbdc1-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cbdc1-117">Required</span></span>  <br/> |<span data-ttu-id="cbdc1-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-118">**String**</span></span> <br/> | <span data-ttu-id="cbdc1-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="cbdc1-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="cbdc1-120">_lcid_</span></span> <br/> |<span data-ttu-id="cbdc1-121">Optional</span><span class="sxs-lookup"><span data-stu-id="cbdc1-121">Optional</span></span>  <br/> |<span data-ttu-id="cbdc1-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="cbdc1-122">**Number**</span></span> <br/> |<span data-ttu-id="cbdc1-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="cbdc1-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cbdc1-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="cbdc1-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="cbdc1-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cbdc1-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="cbdc1-127">Remarks</span></span>

<span data-ttu-id="cbdc1-128">Компонент времени, _даты и времени_ или _выражения,_ отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="cbdc1-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-129">No rounding is done.</span></span> <span data-ttu-id="cbdc1-130">Если входной строки отсутствует или не может быть преобразована допустимый результат, функция MONTH возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-130">If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="cbdc1-131">Возвращаемое значение форматируется в соответствии с краткий формат даты установки с текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="cbdc1-132">Функция MONTH также принимает одно значение номеров для _выражения_ , где целую часть результата представляет число дней, прошедших с 30 декабря 1899.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cbdc1-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbdc1-133">Example 1</span></span>

<span data-ttu-id="cbdc1-134">МЕСЯЦ ("30 мая 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="cbdc1-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="cbdc1-135">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cbdc1-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cbdc1-136">Example 2</span></span>

<span data-ttu-id="cbdc1-137">МЕСЯЦ (DATEVALUE ("30 мая 1999 г.") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="cbdc1-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="cbdc1-138">Возвращает 6.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cbdc1-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cbdc1-139">Example 3</span></span>

<span data-ttu-id="cbdc1-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="cbdc1-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="cbdc1-141">Возвращает 5.</span><span class="sxs-lookup"><span data-stu-id="cbdc1-141">Returns 5.</span></span>
  

