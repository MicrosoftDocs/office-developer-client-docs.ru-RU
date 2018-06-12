---
title: ВТОРАЯ функция (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Возвращает целое число 0 до 59, который представляет секунды в значении даты и времени или выражение.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814731"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="6017d-103">ВТОРАЯ функция (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6017d-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6017d-104">Возвращает целое число 0 до 59, который представляет секунды в значении _даты и времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="6017d-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6017d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6017d-105">Syntax</span></span>

<span data-ttu-id="6017d-106">ВТОРОЙ ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="6017d-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6017d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6017d-107">Parameters</span></span>

|<span data-ttu-id="6017d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6017d-108">**Name**</span></span>|<span data-ttu-id="6017d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6017d-109">**Required/Optional**</span></span>|<span data-ttu-id="6017d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6017d-110">**Data Type**</span></span>|<span data-ttu-id="6017d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6017d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6017d-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="6017d-112">_datetime_</span></span> <br/> |<span data-ttu-id="6017d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6017d-113">Required</span></span>  <br/> |<span data-ttu-id="6017d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6017d-114">**String**</span></span> <br/> |<span data-ttu-id="6017d-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="6017d-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6017d-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6017d-116">_expression_</span></span> <br/> |<span data-ttu-id="6017d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6017d-117">Required</span></span>  <br/> |<span data-ttu-id="6017d-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6017d-118">**String**</span></span> <br/> | <span data-ttu-id="6017d-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="6017d-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6017d-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="6017d-120">_lcid_</span></span> <br/> |<span data-ttu-id="6017d-121">Optional</span><span class="sxs-lookup"><span data-stu-id="6017d-121">Optional</span></span>  <br/> |<span data-ttu-id="6017d-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6017d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="6017d-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные _даты и времени_.</span><span class="sxs-lookup"><span data-stu-id="6017d-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="6017d-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="6017d-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6017d-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6017d-125">Return value</span></span>

<span data-ttu-id="6017d-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="6017d-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6017d-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="6017d-127">Remarks</span></span>

<span data-ttu-id="6017d-128">Компонент даты в _даты и времени_ или _выражение,_ удаляются.</span><span class="sxs-lookup"><span data-stu-id="6017d-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="6017d-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6017d-129">No rounding is done.</span></span> <span data-ttu-id="6017d-130">Если _даты и времени_ , отсутствует или не может быть преобразована допустимый результат, эта функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6017d-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="6017d-131">ВТОРАЯ функция также принимает одно значение номеров для _выражения_ , где целой и дробной части результат представляет долю день после полночи.</span><span class="sxs-lookup"><span data-stu-id="6017d-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6017d-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6017d-132">Example 1</span></span>

<span data-ttu-id="6017d-133">ВТОРОЙ ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="6017d-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="6017d-134">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="6017d-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6017d-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6017d-135">Example 2</span></span>

<span data-ttu-id="6017d-136">ВТОРОЙ (TIMEVALUE ("30 мая 1996 г., 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="6017d-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="6017d-137">Возвращает 52.</span><span class="sxs-lookup"><span data-stu-id="6017d-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6017d-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6017d-138">Example 3</span></span>

<span data-ttu-id="6017d-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="6017d-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="6017d-140">Возвращает 32.</span><span class="sxs-lookup"><span data-stu-id="6017d-140">Returns 32.</span></span>
  

