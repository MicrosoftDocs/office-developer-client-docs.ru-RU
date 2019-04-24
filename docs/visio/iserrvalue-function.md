---
title: Функция ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Возвращает значение TRUE, если значение целлреференце имеет тип ошибки #VALUE, где аргумент формулы имеет неправильный тип. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317888"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="66e37-104">Функция ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="66e37-104">ISERRVALUE Function</span></span>

<span data-ttu-id="66e37-105">Возвращает значение TRUE, если значение _целлреференце_ имеет тип ошибки #VALUE, где аргумент формулы имеет неправильный тип.</span><span class="sxs-lookup"><span data-stu-id="66e37-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="66e37-106">Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="66e37-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="66e37-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66e37-107">Syntax</span></span>

<span data-ttu-id="66e37-108">ISERRVALUE (\* \* *целлреференце* \* \*)</span><span class="sxs-lookup"><span data-stu-id="66e37-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66e37-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="66e37-109">Parameters</span></span>

|<span data-ttu-id="66e37-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="66e37-110">**Name**</span></span>|<span data-ttu-id="66e37-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="66e37-111">**Required/Optional**</span></span>|<span data-ttu-id="66e37-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="66e37-112">**Data Type**</span></span>|<span data-ttu-id="66e37-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66e37-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66e37-114">_целлреференце_</span><span class="sxs-lookup"><span data-stu-id="66e37-114">_cellreference_</span></span> <br/> |<span data-ttu-id="66e37-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="66e37-115">Required</span></span>  <br/> |<span data-ttu-id="66e37-116">**String**</span><span class="sxs-lookup"><span data-stu-id="66e37-116">**String**</span></span> <br/> |<span data-ttu-id="66e37-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="66e37-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66e37-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="66e37-118">Remarks</span></span>

<span data-ttu-id="66e37-119">НеРабочие ячейки С A по D не возвращают #VALUE!</span><span class="sxs-lookup"><span data-stu-id="66e37-119">Scratch cells A through D won't return a #VALUE!</span></span> <span data-ttu-id="66e37-120">ошибка, так как формула может содержать числа и буквы в одной строке.</span><span class="sxs-lookup"><span data-stu-id="66e37-120">error because the formula can contain numbers and letters in the same string.</span></span> <span data-ttu-id="66e37-121">Ячейки X и Y должны содержать только цифры.</span><span class="sxs-lookup"><span data-stu-id="66e37-121">Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="66e37-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="66e37-122">Example 1</span></span>

|<span data-ttu-id="66e37-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="66e37-123">**Cell**</span></span>|<span data-ttu-id="66e37-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="66e37-124">**Formula**</span></span>|<span data-ttu-id="66e37-125">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="66e37-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66e37-126">"С начала. x1"</span><span class="sxs-lookup"><span data-stu-id="66e37-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="66e37-127">= "Дом"</span><span class="sxs-lookup"><span data-stu-id="66e37-127">= "House"</span></span>  <br/> |<span data-ttu-id="66e37-128">#ЗНАЧ!</span><span class="sxs-lookup"><span data-stu-id="66e37-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="66e37-129">". A1"</span><span class="sxs-lookup"><span data-stu-id="66e37-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="66e37-130">= If (ISERRVALUE ("", ",", 2, "")</span><span class="sxs-lookup"><span data-stu-id="66e37-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="66e37-131">2</span><span class="sxs-lookup"><span data-stu-id="66e37-131">2</span></span>  <br/> |
   
<span data-ttu-id="66e37-132">Возвращает 2, так как возвращаемое значение является #VALUE!</span><span class="sxs-lookup"><span data-stu-id="66e37-132">Returns 2 because the value returned is a #VALUE!</span></span> <span data-ttu-id="66e37-133">, а выражение указывает, что Microsoft Visio возвращает 2 вместо ошибки.</span><span class="sxs-lookup"><span data-stu-id="66e37-133">error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="66e37-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="66e37-134">Example 2</span></span>

|<span data-ttu-id="66e37-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="66e37-135">**Cell**</span></span>|<span data-ttu-id="66e37-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="66e37-136">**Formula**</span></span>|<span data-ttu-id="66e37-137">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="66e37-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66e37-138">". A1"</span><span class="sxs-lookup"><span data-stu-id="66e37-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="66e37-139">= "5 + 7"</span><span class="sxs-lookup"><span data-stu-id="66e37-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="66e37-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="66e37-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="66e37-141">"С нуля".</span><span class="sxs-lookup"><span data-stu-id="66e37-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="66e37-142">= If (ISERRVALUE ("с нуля. a1), 2," нуля. a1 ")</span><span class="sxs-lookup"><span data-stu-id="66e37-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="66e37-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="66e37-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="66e37-144">Возвращает 12, так как возвращаемое значение не является #VALUE!</span><span class="sxs-lookup"><span data-stu-id="66e37-144">Returns 12 because the value returned is not a #VALUE!</span></span> <span data-ttu-id="66e37-145">, а выражение указывает Visio вернуть значение исходной ячейки.</span><span class="sxs-lookup"><span data-stu-id="66e37-145">error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

