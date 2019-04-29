---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Возвращает целое число от 0 до 23, представляющее час суток даты и времени или выражение.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429637"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="34515-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="34515-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="34515-104">Возвращает целое число от 0 до 23, представляющее час суток даты и _времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="34515-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="34515-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34515-105">Syntax</span></span>

<span data-ttu-id="34515-106">HOUR ("\* \* *DateTime* \* \*" | \* \* *выражение* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="34515-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="34515-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34515-107">Parameters</span></span>

|<span data-ttu-id="34515-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="34515-108">**Name**</span></span>|<span data-ttu-id="34515-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="34515-109">**Required/Optional**</span></span>|<span data-ttu-id="34515-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="34515-110">**Data Type**</span></span>|<span data-ttu-id="34515-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="34515-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="34515-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="34515-112">_datetime_</span></span> <br/> |<span data-ttu-id="34515-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="34515-113">Required</span></span>  <br/> |<span data-ttu-id="34515-114">**String**</span><span class="sxs-lookup"><span data-stu-id="34515-114">**String**</span></span> <br/> | <span data-ttu-id="34515-115">Строка, которая обычно распознается как Дата и время, или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="34515-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="34515-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="34515-116">_expression_</span></span> <br/> |<span data-ttu-id="34515-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="34515-117">Required</span></span>  <br/> |<span data-ttu-id="34515-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="34515-118">**Varies**</span></span> <br/> |<span data-ttu-id="34515-119">Выражение, которое возвращает дату и время.</span><span class="sxs-lookup"><span data-stu-id="34515-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="34515-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="34515-120">_lcid_</span></span> <br/> |<span data-ttu-id="34515-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="34515-121">Optional</span></span>  <br/> |<span data-ttu-id="34515-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="34515-122">**Number**</span></span> <br/> | <span data-ttu-id="34515-123">Идентификатор языкового стандарта, используемый для оценки нелокальной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="34515-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="34515-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="34515-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34515-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="34515-125">Remarks</span></span>

<span data-ttu-id="34515-126">Компонент даты в *DateTime* и *выражении* отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="34515-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="34515-127">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34515-127">No rounding is done.</span></span> <span data-ttu-id="34515-128">Если *значение DateTime* отсутствует или не может быть преобразовано в допустимый результат, функция возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="34515-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="34515-129">Возвращаемое значение форматируется в соответствии со стилем времени, установленным текущими региональными параметрами системы.</span><span class="sxs-lookup"><span data-stu-id="34515-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="34515-130">Функция HOUR также принимает одно числовое значение для *выражения* , где дробная часть результата представляет часть дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="34515-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="34515-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34515-131">Example 1</span></span>

<span data-ttu-id="34515-132">ЧАС ("15:45")</span><span class="sxs-lookup"><span data-stu-id="34515-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="34515-133">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="34515-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="34515-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="34515-134">Example 2</span></span>

<span data-ttu-id="34515-135">ЧАС ("30 мая, 1997 3:45:24 PM")</span><span class="sxs-lookup"><span data-stu-id="34515-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="34515-136">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="34515-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="34515-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="34515-137">Example 3</span></span>

<span data-ttu-id="34515-138">ЧАС (0,5)</span><span class="sxs-lookup"><span data-stu-id="34515-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="34515-139">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="34515-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="34515-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="34515-140">Example 4</span></span>

<span data-ttu-id="34515-141">ЧАС ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="34515-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="34515-142">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="34515-142">Returns 0.</span></span>
  

