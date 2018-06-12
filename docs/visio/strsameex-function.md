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
# <a name="strsameex-function"></a><span data-ttu-id="c4bc6-103">Функция STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="c4bc6-103">STRSAMEEX Function</span></span>

<span data-ttu-id="c4bc6-104">Определяет, одинаковы ли две строки.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c4bc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4bc6-105">Syntax</span></span>

<span data-ttu-id="c4bc6-106">STRSAMEEX (» ** *string1* ** «,» ** *string2* ** «, ** *localeID* **, ** *флаг* **)</span><span class="sxs-lookup"><span data-stu-id="c4bc6-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4bc6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4bc6-107">Parameters</span></span>

|<span data-ttu-id="c4bc6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-108">**Name**</span></span>|<span data-ttu-id="c4bc6-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-109">**Required/Optional**</span></span>|<span data-ttu-id="c4bc6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-110">**Data Type**</span></span>|<span data-ttu-id="c4bc6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4bc6-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="c4bc6-112">_string1_</span></span> <br/> |<span data-ttu-id="c4bc6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4bc6-113">Required</span></span>  <br/> |<span data-ttu-id="c4bc6-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-114">**String**</span></span> <br/> |<span data-ttu-id="c4bc6-115">Первая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="c4bc6-116">_Строка string2_</span><span class="sxs-lookup"><span data-stu-id="c4bc6-116">_string2_</span></span> <br/> |<span data-ttu-id="c4bc6-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4bc6-117">Required</span></span>  <br/> |<span data-ttu-id="c4bc6-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-118">**String**</span></span> <br/> | <span data-ttu-id="c4bc6-119">Вторая строка для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="c4bc6-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="c4bc6-120">_localeID_</span></span> <br/> |<span data-ttu-id="c4bc6-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4bc6-121">Required</span></span>  <br/> |<span data-ttu-id="c4bc6-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-122">**Numeric**</span></span> <br/> |<span data-ttu-id="c4bc6-123">Код идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="c4bc6-124">_флаг_</span><span class="sxs-lookup"><span data-stu-id="c4bc6-124">_flag_</span></span> <br/> |<span data-ttu-id="c4bc6-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c4bc6-125">Required</span></span>  <br/> |<span data-ttu-id="c4bc6-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-126">**Numeric**</span></span> <br/> | <span data-ttu-id="c4bc6-127">Бит, указывающий тип сравнения.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c4bc6-128">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c4bc6-128">Return value</span></span>

<span data-ttu-id="c4bc6-129">Логический</span><span class="sxs-lookup"><span data-stu-id="c4bc6-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4bc6-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4bc6-130">Remarks</span></span>

<span data-ttu-id="c4bc6-131">STRSAMEEX возвращает значение TRUE, если оба входных строк совпадают с и значение FALSE, если они не.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="c4bc6-132">Эта функция используется для сравнения строк из нескольких байтов или для выполнения сравнения, использующие делами правил для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="c4bc6-133">Сочетание любых из следующих флагов можно использовать с помощью функции STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="c4bc6-134">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-134">**Flag**</span></span>|<span data-ttu-id="c4bc6-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4bc6-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4bc6-136">1</span><span class="sxs-lookup"><span data-stu-id="c4bc6-136">1</span></span>  <br/> |<span data-ttu-id="c4bc6-137">Игнорируйте регистр.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="c4bc6-138">2</span><span class="sxs-lookup"><span data-stu-id="c4bc6-138">2</span></span>  <br/> |<span data-ttu-id="c4bc6-139">Пропуск дополнительный символов.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="c4bc6-140">4</span><span class="sxs-lookup"><span data-stu-id="c4bc6-140">4</span></span>  <br/> |<span data-ttu-id="c4bc6-141">Игнорируйте символы.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="c4bc6-142">4096</span><span class="sxs-lookup"><span data-stu-id="c4bc6-142">4096</span></span>  <br/> |<span data-ttu-id="c4bc6-143">Обрабатывать знаков препинания так же, как символы.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="c4bc6-144">65536</span><span class="sxs-lookup"><span data-stu-id="c4bc6-144">65536</span></span>  <br/> |<span data-ttu-id="c4bc6-145">Не различать хирагана и катакана.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="c4bc6-146">131072</span><span class="sxs-lookup"><span data-stu-id="c4bc6-146">131072</span></span>  <br/> |<span data-ttu-id="c4bc6-147">Не различать однобайтовых знаков и со знаком двухбайтовых знаков.</span><span class="sxs-lookup"><span data-stu-id="c4bc6-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

