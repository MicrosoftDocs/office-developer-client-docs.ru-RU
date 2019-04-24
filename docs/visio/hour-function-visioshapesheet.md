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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329969"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="87a56-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="87a56-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="87a56-104">Возвращает целое число от 0 до 23, представляющее час суток даты и _времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="87a56-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="87a56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87a56-105">Syntax</span></span>

<span data-ttu-id="87a56-106">HOUR ("\* \* *DateTime* \* \*" | \* \* *выражение* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="87a56-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="87a56-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="87a56-107">Parameters</span></span>

|<span data-ttu-id="87a56-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="87a56-108">**Name**</span></span>|<span data-ttu-id="87a56-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="87a56-109">**Required/Optional**</span></span>|<span data-ttu-id="87a56-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="87a56-110">**Data Type**</span></span>|<span data-ttu-id="87a56-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="87a56-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87a56-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="87a56-112">_datetime_</span></span> <br/> |<span data-ttu-id="87a56-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="87a56-113">Required</span></span>  <br/> |<span data-ttu-id="87a56-114">**String**</span><span class="sxs-lookup"><span data-stu-id="87a56-114">**String**</span></span> <br/> | <span data-ttu-id="87a56-115">Строка, которая обычно распознается как Дата и время, или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="87a56-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="87a56-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="87a56-116">_expression_</span></span> <br/> |<span data-ttu-id="87a56-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="87a56-117">Required</span></span>  <br/> |<span data-ttu-id="87a56-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="87a56-118">**Varies**</span></span> <br/> |<span data-ttu-id="87a56-119">Выражение, которое возвращает дату и время.</span><span class="sxs-lookup"><span data-stu-id="87a56-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="87a56-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="87a56-120">_lcid_</span></span> <br/> |<span data-ttu-id="87a56-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="87a56-121">Optional</span></span>  <br/> |<span data-ttu-id="87a56-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="87a56-122">**Number**</span></span> <br/> | <span data-ttu-id="87a56-123">Идентификатор языкового стандарта, используемый для оценки нелокальной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="87a56-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="87a56-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="87a56-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87a56-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87a56-125">Remarks</span></span>

<span data-ttu-id="87a56-126">Компонент даты в *DateTime* и *выражении* отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="87a56-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="87a56-127">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87a56-127">No rounding is done.</span></span> <span data-ttu-id="87a56-128">Если *значение DateTime* отсутствует или не может быть преобразовано в допустимый результат, функция возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="87a56-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="87a56-129">Возвращаемое значение форматируется в соответствии со стилем времени, установленным текущими региональными параметрами системы.</span><span class="sxs-lookup"><span data-stu-id="87a56-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="87a56-130">Функция HOUR также принимает одно числовое значение для *выражения* , где дробная часть результата представляет часть дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="87a56-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="87a56-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87a56-131">Example 1</span></span>

<span data-ttu-id="87a56-132">ЧАС ("15:45")</span><span class="sxs-lookup"><span data-stu-id="87a56-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="87a56-133">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="87a56-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="87a56-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87a56-134">Example 2</span></span>

<span data-ttu-id="87a56-135">ЧАС ("30 мая, 1997 3:45:24 PM")</span><span class="sxs-lookup"><span data-stu-id="87a56-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="87a56-136">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="87a56-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="87a56-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="87a56-137">Example 3</span></span>

<span data-ttu-id="87a56-138">ЧАС (0,5)</span><span class="sxs-lookup"><span data-stu-id="87a56-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="87a56-139">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="87a56-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="87a56-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="87a56-140">Example 4</span></span>

<span data-ttu-id="87a56-141">ЧАС ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="87a56-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="87a56-142">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="87a56-142">Returns 0.</span></span>
  

