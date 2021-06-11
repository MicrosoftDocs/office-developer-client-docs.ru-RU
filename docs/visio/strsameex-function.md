---
title: Функция STRSAMEEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Определяет, одинаковы ли две строки.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413866"
---
# <a name="strsameex-function"></a><span data-ttu-id="8ec0e-103">Функция STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="8ec0e-103">STRSAMEEX Function</span></span>

<span data-ttu-id="8ec0e-104">Определяет, одинаковы ли две строки.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8ec0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec0e-105">Syntax</span></span>

<span data-ttu-id="8ec0e-106">STRSAMEEX (" \*\* *string1* \*\* ", "\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8ec0e-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8ec0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ec0e-107">Parameters</span></span>

|<span data-ttu-id="8ec0e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-108">**Name**</span></span>|<span data-ttu-id="8ec0e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-109">**Required/Optional**</span></span>|<span data-ttu-id="8ec0e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-110">**Data Type**</span></span>|<span data-ttu-id="8ec0e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8ec0e-112">_строка1_</span><span class="sxs-lookup"><span data-stu-id="8ec0e-112">_string1_</span></span> <br/> |<span data-ttu-id="8ec0e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8ec0e-113">Required</span></span>  <br/> |<span data-ttu-id="8ec0e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-114">**String**</span></span> <br/> |<span data-ttu-id="8ec0e-115">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="8ec0e-116">_строка2_</span><span class="sxs-lookup"><span data-stu-id="8ec0e-116">_string2_</span></span> <br/> |<span data-ttu-id="8ec0e-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8ec0e-117">Required</span></span>  <br/> |<span data-ttu-id="8ec0e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-118">**String**</span></span> <br/> | <span data-ttu-id="8ec0e-119">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="8ec0e-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="8ec0e-120">_localeID_</span></span> <br/> |<span data-ttu-id="8ec0e-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8ec0e-121">Required</span></span>  <br/> |<span data-ttu-id="8ec0e-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-122">**Numeric**</span></span> <br/> |<span data-ttu-id="8ec0e-123">Код кода локального кода.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="8ec0e-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="8ec0e-124">_flag_</span></span> <br/> |<span data-ttu-id="8ec0e-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8ec0e-125">Required</span></span>  <br/> |<span data-ttu-id="8ec0e-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-126">**Numeric**</span></span> <br/> | <span data-ttu-id="8ec0e-127">Немного, который указывает тип сравнения.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8ec0e-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ec0e-128">Return value</span></span>

<span data-ttu-id="8ec0e-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec0e-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ec0e-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ec0e-130">Remarks</span></span>

<span data-ttu-id="8ec0e-131">STRSAMEEX возвращает TRUE, если обе строки ввода одинаковы, а FALSE — нет.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="8ec0e-132">Используйте эту функцию для сравнения строк с несколькими byte или сравнения, которые используют правила дела для определенного локального.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="8ec0e-133">Вы можете использовать сочетание любого из следующих флагов с функцией STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="8ec0e-134">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-134">**Flag**</span></span>|<span data-ttu-id="8ec0e-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ec0e-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ec0e-136">1</span><span class="sxs-lookup"><span data-stu-id="8ec0e-136">1</span></span>  <br/> |<span data-ttu-id="8ec0e-137">Игнорируйте случай.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="8ec0e-138">2</span><span class="sxs-lookup"><span data-stu-id="8ec0e-138">2</span></span>  <br/> |<span data-ttu-id="8ec0e-139">Игнорируйте не интервальные символы.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="8ec0e-140">4 </span><span class="sxs-lookup"><span data-stu-id="8ec0e-140">4</span></span>  <br/> |<span data-ttu-id="8ec0e-141">Игнорировать символы.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="8ec0e-142">4096</span><span class="sxs-lookup"><span data-stu-id="8ec0e-142">4096</span></span>  <br/> |<span data-ttu-id="8ec0e-143">Относитесь к пунктуации так же, как к символам.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="8ec0e-144">65536</span><span class="sxs-lookup"><span data-stu-id="8ec0e-144">65536</span></span>  <br/> |<span data-ttu-id="8ec0e-145">Не различайте символы Hiragana и Katakana.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="8ec0e-146">131072</span><span class="sxs-lookup"><span data-stu-id="8ec0e-146">131072</span></span>  <br/> |<span data-ttu-id="8ec0e-147">Не дифференцируйте один и тот же символ, что и двухбайт.</span><span class="sxs-lookup"><span data-stu-id="8ec0e-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

