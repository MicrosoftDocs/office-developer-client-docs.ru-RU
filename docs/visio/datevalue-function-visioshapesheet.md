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
description: Возвращает значение даты, представленное в виде даты и времени или выражения.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360314"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="6e881-103">DATEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6e881-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6e881-104">Возвращает значение даты, представленное в виде даты и _времени_ или _выражения_.</span><span class="sxs-lookup"><span data-stu-id="6e881-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6e881-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e881-105">Syntax</span></span>

<span data-ttu-id="6e881-106">DATEVALUE ("\* \* *DateTime* \* \*" | \* \* *выражение* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="6e881-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e881-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e881-107">Parameters</span></span>

|<span data-ttu-id="6e881-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6e881-108">**Name**</span></span>|<span data-ttu-id="6e881-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6e881-109">**Required/Optional**</span></span>|<span data-ttu-id="6e881-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6e881-110">**Data Type**</span></span>|<span data-ttu-id="6e881-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e881-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e881-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="6e881-112">_datetime_</span></span> <br/> |<span data-ttu-id="6e881-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e881-113">Required</span></span>  <br/> |<span data-ttu-id="6e881-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6e881-114">**String**</span></span> <br/> |<span data-ttu-id="6e881-115">Любая строка, распознаваемая как дата и время либо ссылка на ячейку, содержащую дату и время.</span><span class="sxs-lookup"><span data-stu-id="6e881-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6e881-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6e881-116">_expression_</span></span> <br/> |<span data-ttu-id="6e881-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e881-117">Required</span></span>  <br/> |<span data-ttu-id="6e881-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6e881-118">**String**</span></span> <br/> |<span data-ttu-id="6e881-119">Любое выражение, возвращающее дату и время.</span><span class="sxs-lookup"><span data-stu-id="6e881-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6e881-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="6e881-120">_lcid_</span></span> <br/> |<span data-ttu-id="6e881-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="6e881-121">Optional</span></span>  <br/> |<span data-ttu-id="6e881-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="6e881-122">**Number**</span></span> <br/> |<span data-ttu-id="6e881-123">Задает идентификатор языкового стандарта, который будет использоваться при оценке нелокальной даты и времени.</span><span class="sxs-lookup"><span data-stu-id="6e881-123">Specifies the locale identifier to be used in evaluating a non-local datetime.</span></span> <span data-ttu-id="6e881-124">Идентификатор языкового стандарта — это число, представленной в файлах системных заголовков.</span><span class="sxs-lookup"><span data-stu-id="6e881-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6e881-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e881-125">Return value</span></span>

<span data-ttu-id="6e881-126">Отличным</span><span class="sxs-lookup"><span data-stu-id="6e881-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e881-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="6e881-127">Remarks</span></span>

<span data-ttu-id="6e881-128">Любой компонент времени в *DateTime* или *выражении* отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6e881-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="6e881-129">Если *DateTime* отсутствует или не может быть преобразован в допустимый результат, функция DATEVALUE возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6e881-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="6e881-130">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6e881-130">error.</span></span> 
  
<span data-ttu-id="6e881-131">Возвращаемое значение отображается с использованием краткого стиля даты, установленного текущими региональными параметрами системы.</span><span class="sxs-lookup"><span data-stu-id="6e881-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="6e881-132">Функция DATEVALUE также принимает одно числовое значение для *выражения* , где целая часть результата представляет дни с 30 декабря 1899 г.</span><span class="sxs-lookup"><span data-stu-id="6e881-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6e881-133">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e881-133">Example 1</span></span>

<span data-ttu-id="6e881-134">ДАТАЗНАЧ (NOW ()) + 5 ED.</span><span class="sxs-lookup"><span data-stu-id="6e881-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="6e881-135">Возвращает дату в пять дней от текущей даты.</span><span class="sxs-lookup"><span data-stu-id="6e881-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6e881-136">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e881-136">Example 2</span></span>

<span data-ttu-id="6e881-137">ДАТАЗНАЧ ("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="6e881-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="6e881-138">Возвращает дату.</span><span class="sxs-lookup"><span data-stu-id="6e881-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6e881-139">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6e881-139">Example 3</span></span>

<span data-ttu-id="6e881-140">ДАТАЗНАЧ ("Май 33, 1997")</span><span class="sxs-lookup"><span data-stu-id="6e881-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="6e881-141">Возвращает объект #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6e881-141">Returns a #VALUE!</span></span> <span data-ttu-id="6e881-142">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6e881-142">error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6e881-143">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6e881-143">Example 4</span></span>

<span data-ttu-id="6e881-144">ДАТАЗНАЧ (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="6e881-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="6e881-145">Возвращает 5/30/1997.</span><span class="sxs-lookup"><span data-stu-id="6e881-145">Returns 5/30/1997.</span></span>
  

