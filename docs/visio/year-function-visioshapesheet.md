---
title: Функция YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Возвращает целое число, представляющее григорианский год в даты и времени или выражение, отформатированное в соответствии с краткий формат даты задается текущий язык и региональные параметры системы.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815223"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="a9a4d-103">Функция YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a9a4d-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a9a4d-104">Возвращает целое число, представляющее григорианский год в _даты и времени_ или _выражение_, отформатированное в соответствии с краткий формат даты задается текущий язык и региональные параметры системы.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a9a4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9a4d-105">Syntax</span></span>

<span data-ttu-id="a9a4d-106">ГОДА ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="a9a4d-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9a4d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9a4d-107">Parameters</span></span>

|<span data-ttu-id="a9a4d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-108">**Name**</span></span>|<span data-ttu-id="a9a4d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-109">**Required/Optional**</span></span>|<span data-ttu-id="a9a4d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-110">**Data Type**</span></span>|<span data-ttu-id="a9a4d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9a4d-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="a9a4d-112">_datetime_</span></span> <br/> |<span data-ttu-id="a9a4d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a9a4d-113">Required</span></span>  <br/> |<span data-ttu-id="a9a4d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-114">**String**</span></span> <br/> | <span data-ttu-id="a9a4d-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a9a4d-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a9a4d-116">_expression_</span></span> <br/> |<span data-ttu-id="a9a4d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a9a4d-117">Required</span></span>  <br/> |<span data-ttu-id="a9a4d-118">**Может отличаться**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-118">**Varies**</span></span> <br/> |<span data-ttu-id="a9a4d-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a9a4d-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="a9a4d-120">_lcid_</span></span> <br/> |<span data-ttu-id="a9a4d-121">Optional</span><span class="sxs-lookup"><span data-stu-id="a9a4d-121">Optional</span></span>  <br/> |<span data-ttu-id="a9a4d-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="a9a4d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a9a4d-123">Идентификатор языкового стандарта, который следует использовать для определения нелокальные datetime.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="a9a4d-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a9a4d-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a9a4d-125">Return value</span></span>

<span data-ttu-id="a9a4d-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="a9a4d-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9a4d-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9a4d-127">Remarks</span></span>

<span data-ttu-id="a9a4d-128">Компонент времени в _даты и времени_ или _выражение,_ удаляются.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a9a4d-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-129">No rounding is done.</span></span> <span data-ttu-id="a9a4d-130">Если _даты и времени_ , отсутствует или не может использоваться как допустимая дата или время, года возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="a9a4d-131">Функция YEAR также принимает одно значение номеров для _выражения_ , где целую часть результата представляет число дней, прошедших с 30 декабря 1899.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a9a4d-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a9a4d-132">Example 1</span></span>

<span data-ttu-id="a9a4d-133">ГОДА ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="a9a4d-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="a9a4d-134">Возвращает 2007.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a9a4d-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a9a4d-135">Example 2</span></span>

<span data-ttu-id="a9a4d-136">ГОД (DATEVALUE ("25 декабря 2006 г.") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="a9a4d-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="a9a4d-137">Возвращает 2007.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a9a4d-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a9a4d-138">Example 3</span></span>

<span data-ttu-id="a9a4d-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a9a4d-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="a9a4d-140">Возвращает 1997 г.</span><span class="sxs-lookup"><span data-stu-id="a9a4d-140">Returns 1997.</span></span>
  

