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
description: Определяет, совпадают ли строки. Он возвращает значение TRUE, если они одинаковы, и значение FALSE в противном случае.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428685"
---
# <a name="strsame-function"></a><span data-ttu-id="5d4bc-104">Функция STRSAME</span><span class="sxs-lookup"><span data-stu-id="5d4bc-104">STRSAME Function</span></span>

<span data-ttu-id="5d4bc-105">Определяет, совпадают ли строки.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-105">Determines whether strings are the same.</span></span> <span data-ttu-id="5d4bc-106">Он возвращает значение TRUE, если они одинаковы, и значение FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5d4bc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d4bc-107">Syntax</span></span>

<span data-ttu-id="5d4bc-108">STRSAME ("\* \* *строка_поиска* \* *", "* \* *строка2* \* \*", \* \* *ignoreCase* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5d4bc-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d4bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d4bc-109">Parameters</span></span>

|<span data-ttu-id="5d4bc-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-110">**Name**</span></span>|<span data-ttu-id="5d4bc-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-111">**Required/Optional**</span></span>|<span data-ttu-id="5d4bc-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-112">**Data Type**</span></span>|<span data-ttu-id="5d4bc-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d4bc-114">_строка1_</span><span class="sxs-lookup"><span data-stu-id="5d4bc-114">_string1_</span></span> <br/> |<span data-ttu-id="5d4bc-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5d4bc-115">Required</span></span>  <br/> |<span data-ttu-id="5d4bc-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-116">**String**</span></span> <br/> |<span data-ttu-id="5d4bc-117">Первая сравниваемая строка.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="5d4bc-118">_строка2_</span><span class="sxs-lookup"><span data-stu-id="5d4bc-118">_string2_</span></span> <br/> |<span data-ttu-id="5d4bc-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5d4bc-119">Required</span></span>  <br/> |<span data-ttu-id="5d4bc-120">**String**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-120">**String**</span></span> <br/> |<span data-ttu-id="5d4bc-121">Вторая сравниваемая строка.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="5d4bc-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="5d4bc-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="5d4bc-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="5d4bc-123">Optional</span></span>  <br/> |<span data-ttu-id="5d4bc-124">**Логический**</span><span class="sxs-lookup"><span data-stu-id="5d4bc-124">**Boolean**</span></span> <br/> |<span data-ttu-id="5d4bc-125">Значение TRUE, чтобы игнорировать регистр и значение FALSE, чтобы сравнить регистр.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="5d4bc-126">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5d4bc-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d4bc-127">Return value</span></span>

<span data-ttu-id="5d4bc-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="5d4bc-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d4bc-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d4bc-129">Remarks</span></span>

<span data-ttu-id="5d4bc-130">Чтобы сравнить многобайтовые строки или выполнить сравнения с использованием правил для определенного языкового стандарта, используйте функцию STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="5d4bc-131">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d4bc-131">Example 1</span></span>

<span data-ttu-id="5d4bc-132">STRSAME ("Cat", "собака")</span><span class="sxs-lookup"><span data-stu-id="5d4bc-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="5d4bc-133">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5d4bc-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d4bc-134">Example 2</span></span>

<span data-ttu-id="5d4bc-135">STRSAME ("Cat", "Cat")</span><span class="sxs-lookup"><span data-stu-id="5d4bc-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="5d4bc-136">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5d4bc-137">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5d4bc-137">Example 3</span></span>

<span data-ttu-id="5d4bc-138">STRSAME ("Cat", "Cat", TRUE)</span><span class="sxs-lookup"><span data-stu-id="5d4bc-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="5d4bc-139">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="5d4bc-140">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5d4bc-140">Example 4</span></span>

<span data-ttu-id="5d4bc-141">STRSAME ("Cat", "CAT")</span><span class="sxs-lookup"><span data-stu-id="5d4bc-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="5d4bc-142">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="5d4bc-143">Пример 5</span><span class="sxs-lookup"><span data-stu-id="5d4bc-143">Example 5</span></span>

<span data-ttu-id="5d4bc-144">STRSAME ("Cat", "CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="5d4bc-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="5d4bc-145">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="5d4bc-146">Пример 6</span><span class="sxs-lookup"><span data-stu-id="5d4bc-146">Example 6</span></span>

<span data-ttu-id="5d4bc-147">STRSAME ("кäт", "CAT", TRUE)</span><span class="sxs-lookup"><span data-stu-id="5d4bc-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="5d4bc-148">Возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="5d4bc-149">Пример 7</span><span class="sxs-lookup"><span data-stu-id="5d4bc-149">Example 7</span></span>

<span data-ttu-id="5d4bc-150">STRSAME ("кäт", "КÄТ", TRUE)</span><span class="sxs-lookup"><span data-stu-id="5d4bc-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="5d4bc-151">Возвращает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5d4bc-151">Returns TRUE.</span></span>
  

