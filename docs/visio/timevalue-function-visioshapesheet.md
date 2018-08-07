---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Возвращает значение времени, даты и времени или выражение, на основании системные язык и региональные параметры.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815030"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="c483f-103">TIMEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c483f-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c483f-104">Возвращает значение времени, представленного _даты и времени_ или _выражения_на основании системные язык и региональные параметры.</span><span class="sxs-lookup"><span data-stu-id="c483f-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c483f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c483f-105">Syntax</span></span>

<span data-ttu-id="c483f-106">Функция TIMEVALUE ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="c483f-106">TIMEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c483f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c483f-107">Parameters</span></span>

|<span data-ttu-id="c483f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c483f-108">**Name**</span></span>|<span data-ttu-id="c483f-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c483f-109">**Required/Optional**</span></span>|<span data-ttu-id="c483f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c483f-110">**Data Type**</span></span>|<span data-ttu-id="c483f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c483f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c483f-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="c483f-112">_datetime_</span></span> <br/> |<span data-ttu-id="c483f-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c483f-113">Required</span></span>  <br/> |<span data-ttu-id="c483f-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c483f-114">**String**</span></span> <br/> | <span data-ttu-id="c483f-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="c483f-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="c483f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="c483f-116">_expression_</span></span> <br/> |<span data-ttu-id="c483f-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c483f-117">Required</span></span>  <br/> |<span data-ttu-id="c483f-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="c483f-118">**Varies**</span></span> <br/> | <span data-ttu-id="c483f-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c483f-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="c483f-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="c483f-120">_lcid_</span></span> <br/> |<span data-ttu-id="c483f-121">Optional</span><span class="sxs-lookup"><span data-stu-id="c483f-121">Optional</span></span>  <br/> |<span data-ttu-id="c483f-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="c483f-122">**Number**</span></span> <br/> |<span data-ttu-id="c483f-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="c483f-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="c483f-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="c483f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c483f-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="c483f-125">Remarks</span></span>

<span data-ttu-id="c483f-126">Любой компонент даты в _даты и времени_ или _выражение,_ удаляются.</span><span class="sxs-lookup"><span data-stu-id="c483f-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="c483f-127">Если _даты и времени_ , отсутствует или не может быть преобразована допустимый результат, эта функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c483f-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="c483f-128">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="c483f-128">error.</span></span> 
  
<span data-ttu-id="c483f-129">Функция TIMEVALUE также принимает одно значение номеров для _выражения_ , где целой и дробной части результат представляет долю день после полночи.</span><span class="sxs-lookup"><span data-stu-id="c483f-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c483f-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c483f-130">Example 1</span></span>

<span data-ttu-id="c483f-131">ФУНКЦИЯ TIMEVALUE ("6:00:00")</span><span class="sxs-lookup"><span data-stu-id="c483f-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="c483f-132">Возвращает значение, представляющее 6:00:00.</span><span class="sxs-lookup"><span data-stu-id="c483f-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c483f-133">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c483f-133">Example 2</span></span>

<span data-ttu-id="c483f-134">Функция TIMEVALUE ("14:30") + 4 а. длинное + 30.</span><span class="sxs-lookup"><span data-stu-id="c483f-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="c483f-135">Возвращает значение, представляющее 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="c483f-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c483f-136">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c483f-136">Example 3</span></span>

<span data-ttu-id="c483f-137">Функция TIMEVALUE ("11: 00, 1 июля 1997 г.")</span><span class="sxs-lookup"><span data-stu-id="c483f-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="c483f-138">Возвращает значение, представляющее 11:00:00.</span><span class="sxs-lookup"><span data-stu-id="c483f-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="c483f-139">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c483f-139">Example 4</span></span>

<span data-ttu-id="c483f-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="c483f-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="c483f-141">Возвращает значение, представляющее 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="c483f-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="c483f-142">Пример 5</span><span class="sxs-lookup"><span data-stu-id="c483f-142">Example 5</span></span>

<span data-ttu-id="c483f-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="c483f-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="c483f-144">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c483f-144">Returns a #VALUE!</span></span> <span data-ttu-id="c483f-145">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="c483f-145">error.</span></span>
  

