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
description: Возвращает значение даты, представленное датой или выражением.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360314"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="a09cd-103">DATEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a09cd-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a09cd-104">Возвращает значение даты, представленное _датой или_ _выражением._</span><span class="sxs-lookup"><span data-stu-id="a09cd-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a09cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a09cd-105">Syntax</span></span>

<span data-ttu-id="a09cd-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="a09cd-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a09cd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a09cd-107">Parameters</span></span>

|<span data-ttu-id="a09cd-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a09cd-108">**Name**</span></span>|<span data-ttu-id="a09cd-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a09cd-109">**Required/Optional**</span></span>|<span data-ttu-id="a09cd-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a09cd-110">**Data Type**</span></span>|<span data-ttu-id="a09cd-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a09cd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a09cd-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="a09cd-112">_datetime_</span></span> <br/> |<span data-ttu-id="a09cd-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a09cd-113">Required</span></span>  <br/> |<span data-ttu-id="a09cd-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a09cd-114">**String**</span></span> <br/> |<span data-ttu-id="a09cd-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="a09cd-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a09cd-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a09cd-116">_expression_</span></span> <br/> |<span data-ttu-id="a09cd-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a09cd-117">Required</span></span>  <br/> |<span data-ttu-id="a09cd-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a09cd-118">**String**</span></span> <br/> |<span data-ttu-id="a09cd-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="a09cd-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a09cd-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a09cd-120">_lcid_</span></span> <br/> |<span data-ttu-id="a09cd-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a09cd-121">Optional</span></span>  <br/> |<span data-ttu-id="a09cd-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="a09cd-122">**Number**</span></span> <br/> |<span data-ttu-id="a09cd-123">Указывает идентификатор региональных даты, используемый при оценке нелокализованного даты и времени.</span><span class="sxs-lookup"><span data-stu-id="a09cd-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="a09cd-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="a09cd-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a09cd-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a09cd-125">Return value</span></span>

<span data-ttu-id="a09cd-126">Дата и время</span><span class="sxs-lookup"><span data-stu-id="a09cd-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a09cd-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="a09cd-127">Remarks</span></span>

<span data-ttu-id="a09cd-128">Любой компонент времени в  *дате или*  *выражении*  удаляется.</span><span class="sxs-lookup"><span data-stu-id="a09cd-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="a09cd-129">Если  *дата-время*  отсутствует или не удается преобразовать в допустимый результат, DATEVALUE возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a09cd-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="a09cd-130">error.</span><span class="sxs-lookup"><span data-stu-id="a09cd-130">error.</span></span> 
  
<span data-ttu-id="a09cd-131">Возвращенное значение отображается с использованием краткого стиля даты, установленного текущими региональными настройками системы.</span><span class="sxs-lookup"><span data-stu-id="a09cd-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="a09cd-132">Функция DATEVALUE также принимает одно числовые значения для выражения, где значительная часть результата представляет дни с 30 декабря 1899 г. </span><span class="sxs-lookup"><span data-stu-id="a09cd-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a09cd-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a09cd-133">Example 1</span></span>

<span data-ttu-id="a09cd-134">DATEVALUE(NOW( )+5 ed.</span><span class="sxs-lookup"><span data-stu-id="a09cd-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="a09cd-135">Возвращает дату через пять дней.</span><span class="sxs-lookup"><span data-stu-id="a09cd-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a09cd-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a09cd-136">Example 2</span></span>

<span data-ttu-id="a09cd-137">DATEVALUE("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="a09cd-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="a09cd-138">Возвращает дату.</span><span class="sxs-lookup"><span data-stu-id="a09cd-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a09cd-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a09cd-139">Example 3</span></span>

<span data-ttu-id="a09cd-140">DATEVALUE ("33 мая 1997 г.")</span><span class="sxs-lookup"><span data-stu-id="a09cd-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="a09cd-141">Возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a09cd-141">Returns a #VALUE!</span></span> <span data-ttu-id="a09cd-142">error.</span><span class="sxs-lookup"><span data-stu-id="a09cd-142">error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="a09cd-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a09cd-143">Example 4</span></span>

<span data-ttu-id="a09cd-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a09cd-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="a09cd-145">Возвращается 30.05.1997.</span><span class="sxs-lookup"><span data-stu-id="a09cd-145">Returns 5/30/1997.</span></span>
  

