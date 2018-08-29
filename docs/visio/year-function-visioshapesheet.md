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
description: Возвращает целое число, представляющее год по григорианскому календарю, в виде даты и времени или выражения, отформатированного в соответствии со стилем краткой даты из текущих системных параметров языка и региона.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815223"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="0cb50-103">Функция YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0cb50-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0cb50-104">Возвращает целое число, представляющее год по григорианскому календарю, в виде _даты и времени_ или _выражения_, отформатированного в соответствии со стилем краткой даты из текущих системных параметров языка и региона.</span><span class="sxs-lookup"><span data-stu-id="0cb50-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0cb50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cb50-105">Syntax</span></span>

<span data-ttu-id="0cb50-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span><span class="sxs-lookup"><span data-stu-id="0cb50-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0cb50-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cb50-107">Parameters</span></span>

|<span data-ttu-id="0cb50-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0cb50-108">**Name**</span></span>|<span data-ttu-id="0cb50-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0cb50-109">**Required/Optional**</span></span>|<span data-ttu-id="0cb50-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0cb50-110">**Data Type**</span></span>|<span data-ttu-id="0cb50-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cb50-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0cb50-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="0cb50-112">_DateTime_</span></span> <br/> |<span data-ttu-id="0cb50-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0cb50-113">Required</span></span>  <br/> |<span data-ttu-id="0cb50-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0cb50-114">**String**</span></span> <br/> | <span data-ttu-id="0cb50-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="0cb50-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="0cb50-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="0cb50-116">_expression_</span></span> <br/> |<span data-ttu-id="0cb50-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0cb50-117">Required</span></span>  <br/> |<span data-ttu-id="0cb50-118">**Разные**</span><span class="sxs-lookup"><span data-stu-id="0cb50-118">**Varies**</span></span> <br/> |<span data-ttu-id="0cb50-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="0cb50-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="0cb50-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="0cb50-120">_LCID_</span></span> <br/> |<span data-ttu-id="0cb50-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0cb50-121">Optional</span></span>  <br/> |<span data-ttu-id="0cb50-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="0cb50-122">**Numeric**</span></span> <br/> |<span data-ttu-id="0cb50-123">Идентификатор языкового стандарта, используемый при оценке нелокальных даты и времени.</span><span class="sxs-lookup"><span data-stu-id="0cb50-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="0cb50-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="0cb50-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0cb50-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cb50-125">Return value</span></span>

<span data-ttu-id="0cb50-126">Целое число</span><span class="sxs-lookup"><span data-stu-id="0cb50-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0cb50-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="0cb50-127">Remarks</span></span>

<span data-ttu-id="0cb50-128">Из параметров _datetime_ и _expression_ удаляется компонент времени.</span><span class="sxs-lookup"><span data-stu-id="0cb50-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="0cb50-129">Округление не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cb50-129">No rounding is done.</span></span> <span data-ttu-id="0cb50-130">Если параметр _datetime_ отсутствует или не может быть интерпретирован как допустимое значение даты и времени, функция YEAR возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0cb50-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="0cb50-131">Функция YEAR также принимает в качестве параметра _expression_ одно числовое значение, где целочисленная часть результата представляет количество дней, прошедших с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="0cb50-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0cb50-132">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0cb50-132">Example 1</span></span>

<span data-ttu-id="0cb50-133">YEAR("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="0cb50-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="0cb50-134">Возвращает значение 2007.</span><span class="sxs-lookup"><span data-stu-id="0cb50-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0cb50-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0cb50-135">Example 2</span></span>

<span data-ttu-id="0cb50-136">YEAR(DATEVALUE("25 Дек 2006") + 7 дн.)</span><span class="sxs-lookup"><span data-stu-id="0cb50-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="0cb50-137">Возвращает значение 2007.</span><span class="sxs-lookup"><span data-stu-id="0cb50-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0cb50-138">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0cb50-138">Example 3</span></span>

<span data-ttu-id="0cb50-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="0cb50-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="0cb50-140">Возвращает значение 1997.</span><span class="sxs-lookup"><span data-stu-id="0cb50-140">Returns 1997.</span></span>
  

