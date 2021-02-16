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
description: Возвращает значение времени, представляемого датой или выражением, на основе параметров языка и региона системы.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432326"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="b26a4-103">TIMEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b26a4-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b26a4-104">Возвращает значение времени, представляемого  _датой или_  _выражением,_ на основе параметров языка и региона системы.</span><span class="sxs-lookup"><span data-stu-id="b26a4-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b26a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b26a4-105">Syntax</span></span>

<span data-ttu-id="b26a4-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="b26a4-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b26a4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b26a4-107">Parameters</span></span>

|<span data-ttu-id="b26a4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b26a4-108">**Name**</span></span>|<span data-ttu-id="b26a4-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b26a4-109">**Required/Optional**</span></span>|<span data-ttu-id="b26a4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b26a4-110">**Data Type**</span></span>|<span data-ttu-id="b26a4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b26a4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b26a4-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="b26a4-112">_datetime_</span></span> <br/> |<span data-ttu-id="b26a4-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="b26a4-113">Required</span></span>  <br/> |<span data-ttu-id="b26a4-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="b26a4-114">**String**</span></span> <br/> | <span data-ttu-id="b26a4-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="b26a4-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="b26a4-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="b26a4-116">_expression_</span></span> <br/> |<span data-ttu-id="b26a4-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b26a4-117">Required</span></span>  <br/> |<span data-ttu-id="b26a4-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="b26a4-118">**Varies**</span></span> <br/> | <span data-ttu-id="b26a4-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="b26a4-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="b26a4-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="b26a4-120">_lcid_</span></span> <br/> |<span data-ttu-id="b26a4-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b26a4-121">Optional</span></span>  <br/> |<span data-ttu-id="b26a4-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="b26a4-122">**Number**</span></span> <br/> |<span data-ttu-id="b26a4-123">Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="b26a4-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="b26a4-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="b26a4-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b26a4-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="b26a4-125">Remarks</span></span>

<span data-ttu-id="b26a4-126">Любой компонент даты  _в дате или_  _выражении_ удаляется.</span><span class="sxs-lookup"><span data-stu-id="b26a4-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="b26a4-127">Если  _дата-время_ отсутствует или не удается преобразовать в допустимый результат, эта функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b26a4-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="b26a4-128">error.</span><span class="sxs-lookup"><span data-stu-id="b26a4-128">error.</span></span> 
  
<span data-ttu-id="b26a4-129">Функция TIMEVALUE также принимает одно числовые значения для выражения, где десятичная часть результата представляет часть дня с полуночи. </span><span class="sxs-lookup"><span data-stu-id="b26a4-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b26a4-130">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b26a4-130">Example 1</span></span>

<span data-ttu-id="b26a4-131">TIMEVALUE("6:00 AM")</span><span class="sxs-lookup"><span data-stu-id="b26a4-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="b26a4-132">Возвращает значение, представляющее 6:00.</span><span class="sxs-lookup"><span data-stu-id="b26a4-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b26a4-133">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b26a4-133">Example 2</span></span>

<span data-ttu-id="b26a4-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="b26a4-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="b26a4-135">Возвращает значение, представляющее 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="b26a4-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b26a4-136">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b26a4-136">Example 3</span></span>

<span data-ttu-id="b26a4-137">TIMEVALUE("11:00, 1 июля 1997 г.")</span><span class="sxs-lookup"><span data-stu-id="b26a4-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="b26a4-138">Возвращает значение, представляющее 11:00.</span><span class="sxs-lookup"><span data-stu-id="b26a4-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="b26a4-139">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b26a4-139">Example 4</span></span>

<span data-ttu-id="b26a4-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="b26a4-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="b26a4-141">Возвращает значение, представляющее 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="b26a4-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="b26a4-142">Пример 5</span><span class="sxs-lookup"><span data-stu-id="b26a4-142">Example 5</span></span>

<span data-ttu-id="b26a4-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="b26a4-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="b26a4-144">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b26a4-144">Returns a #VALUE!</span></span> <span data-ttu-id="b26a4-145">error.</span><span class="sxs-lookup"><span data-stu-id="b26a4-145">error.</span></span>
  

