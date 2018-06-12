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
# <a name="strsame-function"></a><span data-ttu-id="162c6-104">Функция STRSAME</span><span class="sxs-lookup"><span data-stu-id="162c6-104">STRSAME Function</span></span>

<span data-ttu-id="162c6-105">Определяет, одинаковы ли строки.</span><span class="sxs-lookup"><span data-stu-id="162c6-105">Determines whether strings are the same.</span></span> <span data-ttu-id="162c6-106">Возвращает значение TRUE, если они совпадают с и значение FALSE, если они не.</span><span class="sxs-lookup"><span data-stu-id="162c6-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="162c6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="162c6-107">Syntax</span></span>

<span data-ttu-id="162c6-108">STRSAME (» ** *string1* ** «,» ** *string2* ** «, ** *ignoreCase* **)</span><span class="sxs-lookup"><span data-stu-id="162c6-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="162c6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="162c6-109">Parameters</span></span>

|<span data-ttu-id="162c6-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="162c6-110">**Name**</span></span>|<span data-ttu-id="162c6-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="162c6-111">**Required/Optional**</span></span>|<span data-ttu-id="162c6-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="162c6-112">**Data Type**</span></span>|<span data-ttu-id="162c6-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="162c6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="162c6-114">_string1_</span><span class="sxs-lookup"><span data-stu-id="162c6-114">_string1_</span></span> <br/> |<span data-ttu-id="162c6-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="162c6-115">Required</span></span>  <br/> |<span data-ttu-id="162c6-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="162c6-116">**String**</span></span> <br/> |<span data-ttu-id="162c6-117">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="162c6-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="162c6-118">_Строка string2_</span><span class="sxs-lookup"><span data-stu-id="162c6-118">_string2_</span></span> <br/> |<span data-ttu-id="162c6-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="162c6-119">Required</span></span>  <br/> |<span data-ttu-id="162c6-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="162c6-120">**String**</span></span> <br/> |<span data-ttu-id="162c6-121">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="162c6-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="162c6-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="162c6-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="162c6-123">Optional</span><span class="sxs-lookup"><span data-stu-id="162c6-123">Optional</span></span>  <br/> |<span data-ttu-id="162c6-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="162c6-124">**Boolean**</span></span> <br/> |<span data-ttu-id="162c6-125">Значение TRUE, следует ли игнорировать регистр и значение FALSE для сравнения регистр.</span><span class="sxs-lookup"><span data-stu-id="162c6-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="162c6-126">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="162c6-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="162c6-127">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="162c6-127">Return value</span></span>

<span data-ttu-id="162c6-128">Логический</span><span class="sxs-lookup"><span data-stu-id="162c6-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="162c6-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="162c6-129">Remarks</span></span>

<span data-ttu-id="162c6-130">Для сравнения строк из нескольких байтов или сравнений с использованием правил регистра для определенного языкового стандарта, используйте функцию STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="162c6-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="162c6-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="162c6-131">Example 1</span></span>

<span data-ttu-id="162c6-132">STRSAME("CAT","dog")</span><span class="sxs-lookup"><span data-stu-id="162c6-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="162c6-133">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="162c6-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="162c6-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="162c6-134">Example 2</span></span>

<span data-ttu-id="162c6-135">STRSAME("CAT","CAT")</span><span class="sxs-lookup"><span data-stu-id="162c6-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="162c6-136">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="162c6-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="162c6-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="162c6-137">Example 3</span></span>

<span data-ttu-id="162c6-138">STRSAME («cat», «cat», значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="162c6-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="162c6-139">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="162c6-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="162c6-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="162c6-140">Example 4</span></span>

<span data-ttu-id="162c6-141">STRSAME("CAT","CAT")</span><span class="sxs-lookup"><span data-stu-id="162c6-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="162c6-142">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="162c6-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="162c6-143">Пример 5</span><span class="sxs-lookup"><span data-stu-id="162c6-143">Example 5</span></span>

<span data-ttu-id="162c6-144">STRSAME (слово "кошка", "Кот", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="162c6-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="162c6-145">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="162c6-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="162c6-146">В примере 6</span><span class="sxs-lookup"><span data-stu-id="162c6-146">Example 6</span></span>

<span data-ttu-id="162c6-147">STRSAME ("cät," кот", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="162c6-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="162c6-148">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="162c6-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="162c6-149">Пример 7</span><span class="sxs-lookup"><span data-stu-id="162c6-149">Example 7</span></span>

<span data-ttu-id="162c6-150">STRSAME ("cät," CÄT", значение TRUE)</span><span class="sxs-lookup"><span data-stu-id="162c6-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="162c6-151">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="162c6-151">Returns TRUE.</span></span>
  

