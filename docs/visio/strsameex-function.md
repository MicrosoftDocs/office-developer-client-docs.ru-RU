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
# <a name="strsameex-function"></a><span data-ttu-id="fe2a0-103">Функция STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="fe2a0-103">STRSAMEEX Function</span></span>

<span data-ttu-id="fe2a0-104">Определяет, одинаковы ли две строки.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fe2a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe2a0-105">Syntax</span></span>

<span data-ttu-id="fe2a0-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fe2a0-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe2a0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe2a0-107">Parameters</span></span>

|<span data-ttu-id="fe2a0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-108">**Name**</span></span>|<span data-ttu-id="fe2a0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-109">**Required/Optional**</span></span>|<span data-ttu-id="fe2a0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-110">**Data Type**</span></span>|<span data-ttu-id="fe2a0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe2a0-112">_строка1_</span><span class="sxs-lookup"><span data-stu-id="fe2a0-112">_string1_</span></span> <br/> |<span data-ttu-id="fe2a0-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fe2a0-113">Required</span></span>  <br/> |<span data-ttu-id="fe2a0-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-114">**String**</span></span> <br/> |<span data-ttu-id="fe2a0-115">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="fe2a0-116">_строка2_</span><span class="sxs-lookup"><span data-stu-id="fe2a0-116">_string2_</span></span> <br/> |<span data-ttu-id="fe2a0-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fe2a0-117">Required</span></span>  <br/> |<span data-ttu-id="fe2a0-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-118">**String**</span></span> <br/> | <span data-ttu-id="fe2a0-119">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="fe2a0-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="fe2a0-120">_localeID_</span></span> <br/> |<span data-ttu-id="fe2a0-121">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fe2a0-121">Required</span></span>  <br/> |<span data-ttu-id="fe2a0-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-122">**Numeric**</span></span> <br/> |<span data-ttu-id="fe2a0-123">Код кода кода локализованного кода.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="fe2a0-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="fe2a0-124">_flag_</span></span> <br/> |<span data-ttu-id="fe2a0-125">Обязательна</span><span class="sxs-lookup"><span data-stu-id="fe2a0-125">Required</span></span>  <br/> |<span data-ttu-id="fe2a0-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-126">**Numeric**</span></span> <br/> | <span data-ttu-id="fe2a0-127">Бит, который указывает тип сравнения.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fe2a0-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe2a0-128">Return value</span></span>

<span data-ttu-id="fe2a0-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="fe2a0-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe2a0-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe2a0-130">Remarks</span></span>

<span data-ttu-id="fe2a0-131">STRSAMEEX возвращает true, если обе входные строки одинаковы, и FALSE, если они не являются.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="fe2a0-132">Используйте эту функцию для сравнения многофайтных строк или сравнения, которые используют правила дела для определенного локаля.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="fe2a0-133">Можно использовать сочетание любого из следующих флагов с функцией STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="fe2a0-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-134">**Flag**</span></span>|<span data-ttu-id="fe2a0-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe2a0-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe2a0-136">1</span><span class="sxs-lookup"><span data-stu-id="fe2a0-136">1</span></span>  <br/> |<span data-ttu-id="fe2a0-137">Игнорируйте дело.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="fe2a0-138">2 </span><span class="sxs-lookup"><span data-stu-id="fe2a0-138">2</span></span>  <br/> |<span data-ttu-id="fe2a0-139">Игнорируйте символы без интервала.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="fe2a0-140">4 </span><span class="sxs-lookup"><span data-stu-id="fe2a0-140">4</span></span>  <br/> |<span data-ttu-id="fe2a0-141">Игнорируйте символы.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="fe2a0-142">4096</span><span class="sxs-lookup"><span data-stu-id="fe2a0-142">4096</span></span>  <br/> |<span data-ttu-id="fe2a0-143">Знаки препинания обрабатывают так же, как символы.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="fe2a0-144">65536</span><span class="sxs-lookup"><span data-stu-id="fe2a0-144">65536</span></span>  <br/> |<span data-ttu-id="fe2a0-145">Не различайте символы хираганы и Катаканы.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="fe2a0-146">131072</span><span class="sxs-lookup"><span data-stu-id="fe2a0-146">131072</span></span>  <br/> |<span data-ttu-id="fe2a0-147">Не различайте один и тот же символ, что и двухбайт.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

