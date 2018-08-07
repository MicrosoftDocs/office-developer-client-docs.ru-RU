---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Возвращает целое число от 0 до 59, представляющее минуты в значении даты и времени или выражение.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814282"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="d054b-103">MINUTE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d054b-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d054b-104">Возвращает целое число от 0 до 59, представляющее минуты в значении *даты и времени* или *выражение* .</span><span class="sxs-lookup"><span data-stu-id="d054b-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d054b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d054b-105">Syntax</span></span>

<span data-ttu-id="d054b-106">МИНУТЫ (" *datetime* " |  *выражение*  [, *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="d054b-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d054b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d054b-107">Parameters</span></span>

|<span data-ttu-id="d054b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d054b-108">**Name**</span></span>|<span data-ttu-id="d054b-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="d054b-109">**Required/Optional**</span></span>|<span data-ttu-id="d054b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d054b-110">**Data Type**</span></span>|<span data-ttu-id="d054b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d054b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d054b-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="d054b-112">_datetime_</span></span> <br/> |<span data-ttu-id="d054b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d054b-113">Required</span></span>  <br/> |<span data-ttu-id="d054b-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d054b-114">**String**</span></span> <br/> |<span data-ttu-id="d054b-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="d054b-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d054b-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d054b-116">_expression_</span></span> <br/> |<span data-ttu-id="d054b-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d054b-117">Required</span></span>  <br/> |<span data-ttu-id="d054b-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d054b-118">**String**</span></span> <br/> | <span data-ttu-id="d054b-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="d054b-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d054b-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="d054b-120">_lcid_</span></span> <br/> |<span data-ttu-id="d054b-121">Optional</span><span class="sxs-lookup"><span data-stu-id="d054b-121">Optional</span></span>  <br/> |<span data-ttu-id="d054b-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="d054b-122">**Number**</span></span> <br/> |<span data-ttu-id="d054b-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="d054b-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="d054b-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="d054b-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d054b-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d054b-125">Return value</span></span>

<span data-ttu-id="d054b-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="d054b-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d054b-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="d054b-127">Remarks</span></span>

<span data-ttu-id="d054b-128">Удаляется компонент даты в _даты и времени_ и _выражение_ .</span><span class="sxs-lookup"><span data-stu-id="d054b-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d054b-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d054b-129">No rounding is done.</span></span> <span data-ttu-id="d054b-130">Если _даты и времени_ , отсутствует или не может быть преобразована допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d054b-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="d054b-131">Возвращаемое значение форматируется в соответствии с формат времени, задание с текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="d054b-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="d054b-132">Функция MINUTE также принимает одно значение номеров для _выражения_ , где дробная часть представляет долю день после полночи.</span><span class="sxs-lookup"><span data-stu-id="d054b-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d054b-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d054b-133">Example 1</span></span>

<span data-ttu-id="d054b-134">МИНУТЫ ("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="d054b-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="d054b-135">Возвращает 45.</span><span class="sxs-lookup"><span data-stu-id="d054b-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d054b-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d054b-136">Example 2</span></span>

<span data-ttu-id="d054b-137">МИНУТЫ (TIMEVALUE ("25 января 1999 12:07:45") + 6 длинное.)</span><span class="sxs-lookup"><span data-stu-id="d054b-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="d054b-138">Возвращает 13.</span><span class="sxs-lookup"><span data-stu-id="d054b-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d054b-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d054b-139">Example 3</span></span>

<span data-ttu-id="d054b-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="d054b-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="d054b-141">Возвращает 48.</span><span class="sxs-lookup"><span data-stu-id="d054b-141">Returns 48.</span></span>
  

