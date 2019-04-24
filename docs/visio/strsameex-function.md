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
description: Определяет, совпадают ли две строки.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329794"
---
# <a name="strsameex-function"></a><span data-ttu-id="72f8d-103">Функция STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="72f8d-103">STRSAMEEX Function</span></span>

<span data-ttu-id="72f8d-104">Определяет, совпадают ли две строки.</span><span class="sxs-lookup"><span data-stu-id="72f8d-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="72f8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72f8d-105">Syntax</span></span>

<span data-ttu-id="72f8d-106">STRSAMEEX ("\* \* *строка_поиска* \* *", "* \* *строка2* \* \*", \* \* *LocaleID* \* \*, \* \* *Flag* \* \*)</span><span class="sxs-lookup"><span data-stu-id="72f8d-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="72f8d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="72f8d-107">Parameters</span></span>

|<span data-ttu-id="72f8d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="72f8d-108">**Name**</span></span>|<span data-ttu-id="72f8d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="72f8d-109">**Required/Optional**</span></span>|<span data-ttu-id="72f8d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="72f8d-110">**Data Type**</span></span>|<span data-ttu-id="72f8d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72f8d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="72f8d-112">_строка1_</span><span class="sxs-lookup"><span data-stu-id="72f8d-112">_string1_</span></span> <br/> |<span data-ttu-id="72f8d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="72f8d-113">Required</span></span>  <br/> |<span data-ttu-id="72f8d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="72f8d-114">**String**</span></span> <br/> |<span data-ttu-id="72f8d-115">Первая сравниваемая строка.</span><span class="sxs-lookup"><span data-stu-id="72f8d-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="72f8d-116">_строка2_</span><span class="sxs-lookup"><span data-stu-id="72f8d-116">_string2_</span></span> <br/> |<span data-ttu-id="72f8d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="72f8d-117">Required</span></span>  <br/> |<span data-ttu-id="72f8d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="72f8d-118">**String**</span></span> <br/> | <span data-ttu-id="72f8d-119">Вторая сравниваемая строка.</span><span class="sxs-lookup"><span data-stu-id="72f8d-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="72f8d-120">_Языка_</span><span class="sxs-lookup"><span data-stu-id="72f8d-120">_localeID_</span></span> <br/> |<span data-ttu-id="72f8d-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="72f8d-121">Required</span></span>  <br/> |<span data-ttu-id="72f8d-122">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="72f8d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="72f8d-123">Код языка.</span><span class="sxs-lookup"><span data-stu-id="72f8d-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="72f8d-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="72f8d-124">_flag_</span></span> <br/> |<span data-ttu-id="72f8d-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="72f8d-125">Required</span></span>  <br/> |<span data-ttu-id="72f8d-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="72f8d-126">**Numeric**</span></span> <br/> | <span data-ttu-id="72f8d-127">Бит, указывающий тип сравнения.</span><span class="sxs-lookup"><span data-stu-id="72f8d-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="72f8d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72f8d-128">Return value</span></span>

<span data-ttu-id="72f8d-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="72f8d-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="72f8d-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="72f8d-130">Remarks</span></span>

<span data-ttu-id="72f8d-131">STRSAMEEX возвращает значение TRUE, если входные строки одинаковы, и значение FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="72f8d-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="72f8d-132">Эта функция используется для сравнения многобайтовых строк или для сравнения, использующих правила для определенного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="72f8d-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="72f8d-133">С помощью функции STRSAMEEX можно использовать любой из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="72f8d-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="72f8d-134">**Флаг**</span><span class="sxs-lookup"><span data-stu-id="72f8d-134">**Flag**</span></span>|<span data-ttu-id="72f8d-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72f8d-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72f8d-136">1,1</span><span class="sxs-lookup"><span data-stu-id="72f8d-136">1</span></span>  <br/> |<span data-ttu-id="72f8d-137">Не учитывать регистр.</span><span class="sxs-lookup"><span data-stu-id="72f8d-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="72f8d-138">2</span><span class="sxs-lookup"><span data-stu-id="72f8d-138">2</span></span>  <br/> |<span data-ttu-id="72f8d-139">ПроПускать символы, отличные от пробелов.</span><span class="sxs-lookup"><span data-stu-id="72f8d-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="72f8d-140">SP4</span><span class="sxs-lookup"><span data-stu-id="72f8d-140">4</span></span>  <br/> |<span data-ttu-id="72f8d-141">Игнорировать символы.</span><span class="sxs-lookup"><span data-stu-id="72f8d-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="72f8d-142">4096</span><span class="sxs-lookup"><span data-stu-id="72f8d-142">4096</span></span>  <br/> |<span data-ttu-id="72f8d-143">Знаки препинания считаются символами.</span><span class="sxs-lookup"><span data-stu-id="72f8d-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="72f8d-144">65536</span><span class="sxs-lookup"><span data-stu-id="72f8d-144">65536</span></span>  <br/> |<span data-ttu-id="72f8d-145">Не различаются символы хирагана и катакана.</span><span class="sxs-lookup"><span data-stu-id="72f8d-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="72f8d-146">131072</span><span class="sxs-lookup"><span data-stu-id="72f8d-146">131072</span></span>  <br/> |<span data-ttu-id="72f8d-147">Не следует отличать однобайтовый символ и тот же символ как двухбайтовый символ.</span><span class="sxs-lookup"><span data-stu-id="72f8d-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

