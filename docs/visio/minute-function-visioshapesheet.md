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
description: Возвращает количество от 0 до 59, которое представляет собой компонент минут даты и времени или выражения.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436568"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="3d947-103">MINUTE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3d947-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3d947-104">Возвращает количество от 0 до 59, которое представляет собой компонент минут *даты и времени* *или выражения.*</span><span class="sxs-lookup"><span data-stu-id="3d947-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3d947-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d947-105">Syntax</span></span>

<span data-ttu-id="3d947-106">MINUTE(" *datetime*  "|  *выражение*  [,  *lcid*  ])</span><span class="sxs-lookup"><span data-stu-id="3d947-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3d947-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d947-107">Parameters</span></span>

|<span data-ttu-id="3d947-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3d947-108">**Name**</span></span>|<span data-ttu-id="3d947-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3d947-109">**Required/Optional**</span></span>|<span data-ttu-id="3d947-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3d947-110">**Data Type**</span></span>|<span data-ttu-id="3d947-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d947-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3d947-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="3d947-112">_datetime_</span></span> <br/> |<span data-ttu-id="3d947-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3d947-113">Required</span></span>  <br/> |<span data-ttu-id="3d947-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3d947-114">**String**</span></span> <br/> |<span data-ttu-id="3d947-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="3d947-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d947-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="3d947-116">_expression_</span></span> <br/> |<span data-ttu-id="3d947-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3d947-117">Required</span></span>  <br/> |<span data-ttu-id="3d947-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3d947-118">**String**</span></span> <br/> | <span data-ttu-id="3d947-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="3d947-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d947-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="3d947-120">_lcid_</span></span> <br/> |<span data-ttu-id="3d947-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3d947-121">Optional</span></span>  <br/> |<span data-ttu-id="3d947-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="3d947-122">**Number**</span></span> <br/> |<span data-ttu-id="3d947-123">Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="3d947-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="3d947-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="3d947-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3d947-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d947-125">Return value</span></span>

<span data-ttu-id="3d947-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="3d947-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d947-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d947-127">Remarks</span></span>

<span data-ttu-id="3d947-128">Компонент даты в  _дате и_  _выражении_ удаляется.</span><span class="sxs-lookup"><span data-stu-id="3d947-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="3d947-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d947-129">No rounding is done.</span></span> <span data-ttu-id="3d947-130">Если  _дата-время_ отсутствует или не удается преобразовать в допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3d947-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="3d947-131">Возвращаемая величина форматирована в соответствии со стилем времени, установленным текущими региональными настройками системы.</span><span class="sxs-lookup"><span data-stu-id="3d947-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="3d947-132">Функция MINUTE также принимает одно число  для выражения, где десятичная часть представляет часть дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="3d947-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3d947-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d947-133">Example 1</span></span>

<span data-ttu-id="3d947-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="3d947-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="3d947-135">Возвращает 45.</span><span class="sxs-lookup"><span data-stu-id="3d947-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3d947-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d947-136">Example 2</span></span>

<span data-ttu-id="3d947-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="3d947-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="3d947-138">Возвращает 13.</span><span class="sxs-lookup"><span data-stu-id="3d947-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3d947-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3d947-139">Example 3</span></span>

<span data-ttu-id="3d947-140">MINUTE(0,575)</span><span class="sxs-lookup"><span data-stu-id="3d947-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="3d947-141">Возвращает 48.</span><span class="sxs-lookup"><span data-stu-id="3d947-141">Returns 48.</span></span>
  

