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
description: Возвращает целое число от 0 до 23, представляющее час дня даты и времени или выражения.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813916"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="6bd3b-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6bd3b-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6bd3b-104">Возвращает целое число от 0 до 23, представляющее час дня _даты и времени_ или _выражения_.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6bd3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bd3b-105">Syntax</span></span>

<span data-ttu-id="6bd3b-106">ЧАС ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="6bd3b-106">HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6bd3b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bd3b-107">Parameters</span></span>

|<span data-ttu-id="6bd3b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-108">**Name**</span></span>|<span data-ttu-id="6bd3b-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-109">**Required/Optional**</span></span>|<span data-ttu-id="6bd3b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-110">**Data Type**</span></span>|<span data-ttu-id="6bd3b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6bd3b-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="6bd3b-112">_datetime_</span></span> <br/> |<span data-ttu-id="6bd3b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6bd3b-113">Required</span></span>  <br/> |<span data-ttu-id="6bd3b-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-114">**String**</span></span> <br/> | <span data-ttu-id="6bd3b-115">Строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6bd3b-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6bd3b-116">_expression_</span></span> <br/> |<span data-ttu-id="6bd3b-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6bd3b-117">Required</span></span>  <br/> |<span data-ttu-id="6bd3b-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-118">**Varies**</span></span> <br/> |<span data-ttu-id="6bd3b-119">Выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6bd3b-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="6bd3b-120">_lcid_</span></span> <br/> |<span data-ttu-id="6bd3b-121">Optional</span><span class="sxs-lookup"><span data-stu-id="6bd3b-121">Optional</span></span>  <br/> |<span data-ttu-id="6bd3b-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="6bd3b-122">**Number**</span></span> <br/> | <span data-ttu-id="6bd3b-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="6bd3b-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bd3b-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="6bd3b-125">Remarks</span></span>

<span data-ttu-id="6bd3b-126">Удаляется компонент даты в *даты и времени* и *выражение* .</span><span class="sxs-lookup"><span data-stu-id="6bd3b-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="6bd3b-127">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-127">No rounding is done.</span></span> <span data-ttu-id="6bd3b-128">Если *даты и времени* , отсутствует или не может быть преобразована допустимый результат, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="6bd3b-129">Возвращаемое значение форматируется в соответствии с формат времени, задание с текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="6bd3b-130">Функция HOUR также принимает одно значение номеров для *выражения* , где целой и дробной части результат представляет долю день после полночи.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6bd3b-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bd3b-131">Example 1</span></span>

<span data-ttu-id="6bd3b-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="6bd3b-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="6bd3b-133">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6bd3b-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bd3b-134">Example 2</span></span>

<span data-ttu-id="6bd3b-135">ЧАС ("30 мая 1997 г., 15:45:24 часов")</span><span class="sxs-lookup"><span data-stu-id="6bd3b-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="6bd3b-136">Возвращает 15.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6bd3b-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6bd3b-137">Example 3</span></span>

<span data-ttu-id="6bd3b-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="6bd3b-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="6bd3b-139">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6bd3b-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6bd3b-140">Example 4</span></span>

<span data-ttu-id="6bd3b-141">HOUR("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="6bd3b-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="6bd3b-142">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="6bd3b-142">Returns 0.</span></span>
  

