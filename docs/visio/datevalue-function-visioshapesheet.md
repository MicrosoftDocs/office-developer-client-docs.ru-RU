---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Возвращает значение типа date, представленное даты и времени или выражение.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813560"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="bc4d1-103">DATEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bc4d1-104">Возвращает значение типа date, представленное _даты и времени_ или _выражение_.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bc4d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc4d1-105">Syntax</span></span>

<span data-ttu-id="bc4d1-106">Функция DATEVALUE ("** *даты и времени* **" | ** *выражение* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="bc4d1-106">DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bc4d1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc4d1-107">Parameters</span></span>

|<span data-ttu-id="bc4d1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-108">**Name**</span></span>|<span data-ttu-id="bc4d1-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-109">**Required/Optional**</span></span>|<span data-ttu-id="bc4d1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-110">**Data Type**</span></span>|<span data-ttu-id="bc4d1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bc4d1-112">_даты и времени_</span><span class="sxs-lookup"><span data-stu-id="bc4d1-112">_datetime_</span></span> <br/> |<span data-ttu-id="bc4d1-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bc4d1-113">Required</span></span>  <br/> |<span data-ttu-id="bc4d1-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-114">**String**</span></span> <br/> |<span data-ttu-id="bc4d1-115">Любая строка, часто распознается как даты и времени или ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="bc4d1-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="bc4d1-116">_expression_</span></span> <br/> |<span data-ttu-id="bc4d1-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bc4d1-117">Required</span></span>  <br/> |<span data-ttu-id="bc4d1-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-118">**String**</span></span> <br/> |<span data-ttu-id="bc4d1-119">Любое выражение, возвращающее даты и времени.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="bc4d1-120">_код языка_</span><span class="sxs-lookup"><span data-stu-id="bc4d1-120">_lcid_</span></span> <br/> |<span data-ttu-id="bc4d1-121">Optional</span><span class="sxs-lookup"><span data-stu-id="bc4d1-121">Optional</span></span>  <br/> |<span data-ttu-id="bc4d1-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="bc4d1-122">**Number**</span></span> <br/> |<span data-ttu-id="bc4d1-123">Задает идентификатор языкового стандарта для использования при оценке нелокальных datetime.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="bc4d1-124">Идентификатор языкового стандарта — это число, описанных в файлы заголовков системы.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bc4d1-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bc4d1-125">Return value</span></span>

<span data-ttu-id="bc4d1-126">Даты и времени</span><span class="sxs-lookup"><span data-stu-id="bc4d1-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc4d1-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc4d1-127">Remarks</span></span>

<span data-ttu-id="bc4d1-128">Любой компонент времени в *даты и времени* или *выражение,* удаляются.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="bc4d1-129">Если *даты и времени* отсутствует или не может быть преобразована допустимый результат, DATEVALUE возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bc4d1-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="bc4d1-130">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-130">error.</span></span> 
  
<span data-ttu-id="bc4d1-131">Возвращаемое значение отображается с использованием стилей краткий формат даты, задание с текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="bc4d1-132">Функция DATEVALUE также принимает одно значение номеров для *выражения* , где целую часть результата представляет дней, прошедших с 30 декабря 1899.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bc4d1-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc4d1-133">Example 1</span></span>

<span data-ttu-id="bc4d1-134">Функция DATEVALUE (СЕЙЧАС ()) + 5 ed.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="bc4d1-135">Возвращает дату пять дней сейчас.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bc4d1-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc4d1-136">Example 2</span></span>

<span data-ttu-id="bc4d1-137">ФУНКЦИЯ DATEVALUE ("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="bc4d1-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="bc4d1-138">Возвращает дату.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bc4d1-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bc4d1-139">Example 3</span></span>

<span data-ttu-id="bc4d1-140">Функция DATEVALUE ("мая 33, 1997 г.")</span><span class="sxs-lookup"><span data-stu-id="bc4d1-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="bc4d1-141">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bc4d1-141">Returns a #VALUE!</span></span> <span data-ttu-id="bc4d1-142">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-142">error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="bc4d1-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="bc4d1-143">Example 4</span></span>

<span data-ttu-id="bc4d1-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="bc4d1-145">Возвращает 5/30/1997 г.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-145">Returns 5/30/1997.</span></span>
  

