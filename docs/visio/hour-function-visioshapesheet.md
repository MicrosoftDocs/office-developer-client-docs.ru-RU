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
description: Возвращается в несколько часов от 0 до 23, представляющее час дня даты или выражения.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429637"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="536a5-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="536a5-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="536a5-104">Возвращает в нее несколько часов от 0 до 23, представляющее час дня даты _или_ _выражения._</span><span class="sxs-lookup"><span data-stu-id="536a5-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="536a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="536a5-105">Syntax</span></span>

<span data-ttu-id="536a5-106">HOUR(" \*\* *datetime* \*\* "| \*\* *выражение* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="536a5-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="536a5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="536a5-107">Parameters</span></span>

|<span data-ttu-id="536a5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="536a5-108">**Name**</span></span>|<span data-ttu-id="536a5-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="536a5-109">**Required/Optional**</span></span>|<span data-ttu-id="536a5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="536a5-110">**Data Type**</span></span>|<span data-ttu-id="536a5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="536a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="536a5-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="536a5-112">_datetime_</span></span> <br/> |<span data-ttu-id="536a5-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="536a5-113">Required</span></span>  <br/> |<span data-ttu-id="536a5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="536a5-114">**String**</span></span> <br/> | <span data-ttu-id="536a5-115">Строка, обычно распознаемая как дата и время или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="536a5-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="536a5-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="536a5-116">_expression_</span></span> <br/> |<span data-ttu-id="536a5-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="536a5-117">Required</span></span>  <br/> |<span data-ttu-id="536a5-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="536a5-118">**Varies**</span></span> <br/> |<span data-ttu-id="536a5-119">Выражение, которое дает дату и время.</span><span class="sxs-lookup"><span data-stu-id="536a5-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="536a5-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="536a5-120">_lcid_</span></span> <br/> |<span data-ttu-id="536a5-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="536a5-121">Optional</span></span>  <br/> |<span data-ttu-id="536a5-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="536a5-122">**Number**</span></span> <br/> | <span data-ttu-id="536a5-123">Идентификатор locale, который будет использоваться для оценки нелокального времени даты.</span><span class="sxs-lookup"><span data-stu-id="536a5-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="536a5-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="536a5-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="536a5-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="536a5-125">Remarks</span></span>

<span data-ttu-id="536a5-126">Компонент даты в  *дате*  и  *выражении*  удаляется.</span><span class="sxs-lookup"><span data-stu-id="536a5-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="536a5-127">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="536a5-127">No rounding is done.</span></span> <span data-ttu-id="536a5-128">Если время  *даты*  отсутствует или не может быть преобразовано в допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="536a5-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="536a5-129">Возвращенное значение отформатировано в соответствии со стилем времени, установленным текущим региональным Параметры.</span><span class="sxs-lookup"><span data-stu-id="536a5-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="536a5-130">Функция HOUR также принимает одно значение  номера для выражения, где десятичная часть результата представляет долю дня с полуночи.</span><span class="sxs-lookup"><span data-stu-id="536a5-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="536a5-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="536a5-131">Example 1</span></span>

<span data-ttu-id="536a5-132">HOUR ("15:45")</span><span class="sxs-lookup"><span data-stu-id="536a5-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="536a5-133">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="536a5-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="536a5-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="536a5-134">Example 2</span></span>

<span data-ttu-id="536a5-135">HOUR ("30 мая 1997 г. 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="536a5-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="536a5-136">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="536a5-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="536a5-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="536a5-137">Example 3</span></span>

<span data-ttu-id="536a5-138">HOUR (0.5)</span><span class="sxs-lookup"><span data-stu-id="536a5-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="536a5-139">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="536a5-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="536a5-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="536a5-140">Example 4</span></span>

<span data-ttu-id="536a5-141">HOUR ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="536a5-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="536a5-142">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="536a5-142">Returns 0.</span></span>
  

