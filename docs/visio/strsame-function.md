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
description: Определяет, одинаковы ли строки. Возвращает значение TRUE, если они совпадают с и значение FALSE, если они не.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814944"
---
# <a name="strsame-function"></a><span data-ttu-id="e8b51-104">Функция STRSAME</span><span class="sxs-lookup"><span data-stu-id="e8b51-104">STRSAME Function</span></span>

<span data-ttu-id="e8b51-105">Определяет, одинаковы ли строки.</span><span class="sxs-lookup"><span data-stu-id="e8b51-105">Determines whether strings are the same.</span></span> <span data-ttu-id="e8b51-106">Возвращает значение TRUE, если они совпадают с и значение FALSE, если они не.</span><span class="sxs-lookup"><span data-stu-id="e8b51-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8b51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8b51-107">Syntax</span></span>

<span data-ttu-id="e8b51-108">STRSAME (» ** *string1* ** «,» ** *string2* ** «, ** *ignoreCase* **)</span><span class="sxs-lookup"><span data-stu-id="e8b51-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e8b51-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8b51-109">Parameters</span></span>

|<span data-ttu-id="e8b51-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e8b51-110">**Name**</span></span>|<span data-ttu-id="e8b51-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="e8b51-111">**Required/Optional**</span></span>|<span data-ttu-id="e8b51-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e8b51-112">**Data Type**</span></span>|<span data-ttu-id="e8b51-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8b51-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e8b51-114">_string1_</span><span class="sxs-lookup"><span data-stu-id="e8b51-114">_string1_</span></span> <br/> |<span data-ttu-id="e8b51-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8b51-115">Required</span></span>  <br/> |<span data-ttu-id="e8b51-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="e8b51-116">**String**</span></span> <br/> |<span data-ttu-id="e8b51-117">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="e8b51-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="e8b51-118">_Строка string2_</span><span class="sxs-lookup"><span data-stu-id="e8b51-118">_string2_</span></span> <br/> |<span data-ttu-id="e8b51-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8b51-119">Required</span></span>  <br/> |<span data-ttu-id="e8b51-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="e8b51-120">**String**</span></span> <br/> |<span data-ttu-id="e8b51-121">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="e8b51-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="e8b51-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="e8b51-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="e8b51-123">Optional</span><span class="sxs-lookup"><span data-stu-id="e8b51-123">Optional</span></span>  <br/> |<span data-ttu-id="e8b51-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e8b51-124">**Boolean**</span></span> <br/> |<span data-ttu-id="e8b51-125">Значение TRUE, следует ли игнорировать регистр и значение FALSE для сравнения регистр.</span><span class="sxs-lookup"><span data-stu-id="e8b51-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="e8b51-126">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e8b51-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="e8b51-128">Логический</span><span class="sxs-lookup"><span data-stu-id="e8b51-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8b51-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8b51-129">Remarks</span></span>

<span data-ttu-id="e8b51-130">Для сравнения строк из нескольких байтов или сравнений с использованием правил регистра для определенного языкового стандарта, используйте функцию STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="e8b51-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="e8b51-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8b51-131">Example 1</span></span>

<span data-ttu-id="e8b51-132">STRSAME("CAT","dog")</span><span class="sxs-lookup"><span data-stu-id="e8b51-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="e8b51-133">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e8b51-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8b51-134">Example 2</span></span>

<span data-ttu-id="e8b51-135">STRSAME("CAT","CAT")</span><span class="sxs-lookup"><span data-stu-id="e8b51-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="e8b51-136">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e8b51-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e8b51-137">Example 3</span></span>

<span data-ttu-id="e8b51-138">STRSAME («cat», «cat», значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="e8b51-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="e8b51-139">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e8b51-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e8b51-140">Example 4</span></span>

<span data-ttu-id="e8b51-141">STRSAME("CAT","CAT")</span><span class="sxs-lookup"><span data-stu-id="e8b51-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="e8b51-142">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="e8b51-143">Пример 5</span><span class="sxs-lookup"><span data-stu-id="e8b51-143">Example 5</span></span>

<span data-ttu-id="e8b51-144">STRSAME (слово "кошка", "Кот", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="e8b51-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="e8b51-145">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="e8b51-146">В примере 6</span><span class="sxs-lookup"><span data-stu-id="e8b51-146">Example 6</span></span>

<span data-ttu-id="e8b51-147">STRSAME ("cät," кот", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="e8b51-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="e8b51-148">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="e8b51-149">Пример 7</span><span class="sxs-lookup"><span data-stu-id="e8b51-149">Example 7</span></span>

<span data-ttu-id="e8b51-150">STRSAME ("cät," CÄT", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="e8b51-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="e8b51-151">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e8b51-151">Returns TRUE.</span></span>
  

