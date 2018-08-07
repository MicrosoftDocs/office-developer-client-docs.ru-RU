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
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814966"
---
# <a name="strsameex-function"></a><span data-ttu-id="45eb9-103">Функция STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="45eb9-103">STRSAMEEX Function</span></span>

<span data-ttu-id="45eb9-104">Определяет, одинаковы ли две строки.</span><span class="sxs-lookup"><span data-stu-id="45eb9-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="45eb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45eb9-105">Syntax</span></span>

<span data-ttu-id="45eb9-106">STRSAMEEX (» ** *string1* ** «,» ** *string2* ** «, ** *localeID* **, ** *флаг* **)</span><span class="sxs-lookup"><span data-stu-id="45eb9-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="45eb9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="45eb9-107">Parameters</span></span>

|<span data-ttu-id="45eb9-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="45eb9-108">**Name**</span></span>|<span data-ttu-id="45eb9-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="45eb9-109">**Required/Optional**</span></span>|<span data-ttu-id="45eb9-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="45eb9-110">**Data Type**</span></span>|<span data-ttu-id="45eb9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45eb9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="45eb9-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="45eb9-112">_string1_</span></span> <br/> |<span data-ttu-id="45eb9-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45eb9-113">Required</span></span>  <br/> |<span data-ttu-id="45eb9-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="45eb9-114">**String**</span></span> <br/> |<span data-ttu-id="45eb9-115">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="45eb9-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="45eb9-116">_Строка string2_</span><span class="sxs-lookup"><span data-stu-id="45eb9-116">_string2_</span></span> <br/> |<span data-ttu-id="45eb9-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45eb9-117">Required</span></span>  <br/> |<span data-ttu-id="45eb9-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="45eb9-118">**String**</span></span> <br/> | <span data-ttu-id="45eb9-119">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="45eb9-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="45eb9-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="45eb9-120">_localeID_</span></span> <br/> |<span data-ttu-id="45eb9-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45eb9-121">Required</span></span>  <br/> |<span data-ttu-id="45eb9-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="45eb9-122">**Numeric**</span></span> <br/> |<span data-ttu-id="45eb9-123">Код идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="45eb9-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="45eb9-124">_флаг_</span><span class="sxs-lookup"><span data-stu-id="45eb9-124">_flag_</span></span> <br/> |<span data-ttu-id="45eb9-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="45eb9-125">Required</span></span>  <br/> |<span data-ttu-id="45eb9-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="45eb9-126">**Numeric**</span></span> <br/> | <span data-ttu-id="45eb9-127">Бит, указывающий тип сравнения.</span><span class="sxs-lookup"><span data-stu-id="45eb9-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="45eb9-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="45eb9-129">Логический</span><span class="sxs-lookup"><span data-stu-id="45eb9-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45eb9-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="45eb9-130">Remarks</span></span>

<span data-ttu-id="45eb9-131">STRSAMEEX возвращает значение TRUE, если оба входных строк совпадают с и значение FALSE, если они не.</span><span class="sxs-lookup"><span data-stu-id="45eb9-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="45eb9-132">Эта функция используется для сравнения строк из нескольких байтов или для выполнения сравнения, использующие делами правил для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="45eb9-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="45eb9-133">Сочетание любых из следующих флагов можно использовать с помощью функции STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="45eb9-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="45eb9-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="45eb9-134">**Flag**</span></span>|<span data-ttu-id="45eb9-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45eb9-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45eb9-136">1</span><span class="sxs-lookup"><span data-stu-id="45eb9-136">1</span></span>  <br/> |<span data-ttu-id="45eb9-137">Игнорируйте регистр.</span><span class="sxs-lookup"><span data-stu-id="45eb9-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="45eb9-138">2</span><span class="sxs-lookup"><span data-stu-id="45eb9-138">2</span></span>  <br/> |<span data-ttu-id="45eb9-139">Пропуск дополнительный символов.</span><span class="sxs-lookup"><span data-stu-id="45eb9-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="45eb9-140">4</span><span class="sxs-lookup"><span data-stu-id="45eb9-140">4</span></span>  <br/> |<span data-ttu-id="45eb9-141">Игнорируйте символы.</span><span class="sxs-lookup"><span data-stu-id="45eb9-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="45eb9-142">4096</span><span class="sxs-lookup"><span data-stu-id="45eb9-142">4096</span></span>  <br/> |<span data-ttu-id="45eb9-143">Обрабатывать знаков препинания так же, как символы.</span><span class="sxs-lookup"><span data-stu-id="45eb9-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="45eb9-144">65536</span><span class="sxs-lookup"><span data-stu-id="45eb9-144">65536</span></span>  <br/> |<span data-ttu-id="45eb9-145">Не различать хирагана и катакана.</span><span class="sxs-lookup"><span data-stu-id="45eb9-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="45eb9-146">131072</span><span class="sxs-lookup"><span data-stu-id="45eb9-146">131072</span></span>  <br/> |<span data-ttu-id="45eb9-147">Не различать однобайтовых знаков и со знаком двухбайтовых знаков.</span><span class="sxs-lookup"><span data-stu-id="45eb9-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

