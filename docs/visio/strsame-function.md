---
title: Функция STRSAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Определяет, являются ли строки одинаковыми. Он возвращает TRUE, если они одинаковы и FALSE, если они не являются.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428685"
---
# <a name="strsame-function"></a><span data-ttu-id="59106-104">Функция STRSAME</span><span class="sxs-lookup"><span data-stu-id="59106-104">STRSAME Function</span></span>

<span data-ttu-id="59106-105">Определяет, являются ли строки одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="59106-105">Determines whether strings are the same.</span></span> <span data-ttu-id="59106-106">Он возвращает TRUE, если они одинаковы и FALSE, если они не являются.</span><span class="sxs-lookup"><span data-stu-id="59106-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="59106-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59106-107">Syntax</span></span>

<span data-ttu-id="59106-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span><span class="sxs-lookup"><span data-stu-id="59106-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="59106-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59106-109">Parameters</span></span>

|<span data-ttu-id="59106-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="59106-110">**Name**</span></span>|<span data-ttu-id="59106-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="59106-111">**Required/Optional**</span></span>|<span data-ttu-id="59106-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="59106-112">**Data Type**</span></span>|<span data-ttu-id="59106-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59106-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="59106-114">_строка1_</span><span class="sxs-lookup"><span data-stu-id="59106-114">_string1_</span></span> <br/> |<span data-ttu-id="59106-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="59106-115">Required</span></span>  <br/> |<span data-ttu-id="59106-116">**String**</span><span class="sxs-lookup"><span data-stu-id="59106-116">**String**</span></span> <br/> |<span data-ttu-id="59106-117">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="59106-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="59106-118">_строка2_</span><span class="sxs-lookup"><span data-stu-id="59106-118">_string2_</span></span> <br/> |<span data-ttu-id="59106-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="59106-119">Required</span></span>  <br/> |<span data-ttu-id="59106-120">**String**</span><span class="sxs-lookup"><span data-stu-id="59106-120">**String**</span></span> <br/> |<span data-ttu-id="59106-121">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="59106-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="59106-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="59106-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="59106-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="59106-123">Optional</span></span>  <br/> |<span data-ttu-id="59106-124">**Логический**</span><span class="sxs-lookup"><span data-stu-id="59106-124">**Boolean**</span></span> <br/> |<span data-ttu-id="59106-125">TRUE, чтобы игнорировать случай и FALSE, чтобы сравнить случай.</span><span class="sxs-lookup"><span data-stu-id="59106-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="59106-126">По умолчанию значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="59106-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="59106-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59106-127">Return value</span></span>

<span data-ttu-id="59106-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="59106-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59106-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="59106-129">Remarks</span></span>

<span data-ttu-id="59106-130">Чтобы сравнить строки с несколькими байтами или сделать сравнения с использованием правил дела для определенного локального, используйте функцию STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="59106-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="59106-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59106-131">Example 1</span></span>

<span data-ttu-id="59106-132">STRSAME ("cat", "dog")</span><span class="sxs-lookup"><span data-stu-id="59106-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="59106-133">Возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="59106-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="59106-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59106-134">Example 2</span></span>

<span data-ttu-id="59106-135">STRSAME ("cat", "cat")</span><span class="sxs-lookup"><span data-stu-id="59106-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="59106-136">Возвращает TRUE.</span><span class="sxs-lookup"><span data-stu-id="59106-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="59106-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="59106-137">Example 3</span></span>

<span data-ttu-id="59106-138">STRSAME ("cat", "cat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="59106-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="59106-139">Возвращает TRUE.</span><span class="sxs-lookup"><span data-stu-id="59106-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="59106-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="59106-140">Example 4</span></span>

<span data-ttu-id="59106-141">STRSAME ("cat", "CAT")</span><span class="sxs-lookup"><span data-stu-id="59106-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="59106-142">Возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="59106-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="59106-143">Пример 5</span><span class="sxs-lookup"><span data-stu-id="59106-143">Example 5</span></span>

<span data-ttu-id="59106-144">STRSAME ("cat", "CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="59106-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="59106-145">Возвращает TRUE.</span><span class="sxs-lookup"><span data-stu-id="59106-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="59106-146">Пример 6</span><span class="sxs-lookup"><span data-stu-id="59106-146">Example 6</span></span>

<span data-ttu-id="59106-147">STRSAME ("cät", "CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="59106-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="59106-148">Возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="59106-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="59106-149">Пример 7</span><span class="sxs-lookup"><span data-stu-id="59106-149">Example 7</span></span>

<span data-ttu-id="59106-150">STRSAME ("cät", "CÄT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="59106-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="59106-151">Возвращает TRUE.</span><span class="sxs-lookup"><span data-stu-id="59106-151">Returns TRUE.</span></span>
  

