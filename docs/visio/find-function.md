---
title: Функция FIND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Находит одну текстовую строку, содержаную в другой строке текста, и возвращает исходное положение текстовой строки, которую вы ищете относительно ее положения в текстовой строке, содержащем ее.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426578"
---
# <a name="find-function"></a><span data-ttu-id="634c0-103">Функция FIND</span><span class="sxs-lookup"><span data-stu-id="634c0-103">FIND Function</span></span>

<span data-ttu-id="634c0-104">Находит одну текстовую строку, содержаную в другой строке текста, и возвращает исходное положение текстовой строки, которую вы ищете относительно ее положения в текстовой строке, содержащем ее.</span><span class="sxs-lookup"><span data-stu-id="634c0-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="634c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="634c0-105">Syntax</span></span>

<span data-ttu-id="634c0-106">FIND (\*\* *find_text* \*\*, \*\*\*\* within_text \**,[ \*\* *start_num* \*\* ], [* *ignore_case* \*\* ]]</span><span class="sxs-lookup"><span data-stu-id="634c0-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="634c0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="634c0-107">Parameters</span></span>

|<span data-ttu-id="634c0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="634c0-108">**Name**</span></span>|<span data-ttu-id="634c0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="634c0-109">**Required/Optional**</span></span>|<span data-ttu-id="634c0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="634c0-110">**Data Type**</span></span>|<span data-ttu-id="634c0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="634c0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="634c0-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="634c0-112">_find_text_</span></span> <br/> |<span data-ttu-id="634c0-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="634c0-113">Required</span></span>  <br/> |<span data-ttu-id="634c0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="634c0-114">**String**</span></span> <br/> |<span data-ttu-id="634c0-115">Текстовая строка, которая вам нужна.</span><span class="sxs-lookup"><span data-stu-id="634c0-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="634c0-116">_format_</span><span class="sxs-lookup"><span data-stu-id="634c0-116">_format_</span></span> <br/> |<span data-ttu-id="634c0-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="634c0-117">Required</span></span>  <br/> |<span data-ttu-id="634c0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="634c0-118">**String**</span></span> <br/> |<span data-ttu-id="634c0-119">Текстовая строка, содержаная текст, который необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="634c0-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="634c0-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="634c0-120">_start_num_</span></span> <br/> |<span data-ttu-id="634c0-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="634c0-121">Optional</span></span>  <br/> |<span data-ttu-id="634c0-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="634c0-122">**Number**</span></span> <br/> |<span data-ttu-id="634c0-123">Символ, с которого начинается поиск.</span><span class="sxs-lookup"><span data-stu-id="634c0-123">The character at which to start the search.</span></span> <span data-ttu-id="634c0-124">Первый символ в  _within_text_ — 1.</span><span class="sxs-lookup"><span data-stu-id="634c0-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="634c0-125">Если  _start_num_ отсутствует, предполагается, что это будет 1.</span><span class="sxs-lookup"><span data-stu-id="634c0-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="634c0-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="634c0-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="634c0-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="634c0-127">Optional</span></span>  <br/> |<span data-ttu-id="634c0-128">**Логический**</span><span class="sxs-lookup"><span data-stu-id="634c0-128">**Boolean**</span></span> <br/> |<span data-ttu-id="634c0-129">По умолчанию функция FIND является чувствительной к делу.</span><span class="sxs-lookup"><span data-stu-id="634c0-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="634c0-130">Если вы хотите, чтобы функция FIND проигнорировала случай, установите этот аргумент true.</span><span class="sxs-lookup"><span data-stu-id="634c0-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="634c0-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="634c0-131">Return value</span></span>

<span data-ttu-id="634c0-132">Номер</span><span class="sxs-lookup"><span data-stu-id="634c0-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="634c0-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="634c0-133">Remarks</span></span>

<span data-ttu-id="634c0-134">Если найдено несколько совпадений, функция FIND возвращает исходное положение первого совпадения в строке.</span><span class="sxs-lookup"><span data-stu-id="634c0-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="634c0-135">Аргумент  _find_text_ не считает какие-либо символы подкардами.</span><span class="sxs-lookup"><span data-stu-id="634c0-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="634c0-136">Если _find_text:_</span><span class="sxs-lookup"><span data-stu-id="634c0-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="634c0-137">Является пустым (""), FIND соответствует первому символу строки поиска  _(т._ е. символу с номером start_num или 1).</span><span class="sxs-lookup"><span data-stu-id="634c0-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="634c0-138">Не появляется в  _within_text_, FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="634c0-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="634c0-139">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="634c0-139">error value.</span></span> 
    
<span data-ttu-id="634c0-140">Если _start_num:_</span><span class="sxs-lookup"><span data-stu-id="634c0-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="634c0-141">Не больше нуля (0), FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="634c0-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="634c0-142">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="634c0-142">error value.</span></span> 
    
- <span data-ttu-id="634c0-143">Больше, чем длина  _within_text,_ FINDreturns #VALUE!</span><span class="sxs-lookup"><span data-stu-id="634c0-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="634c0-144">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="634c0-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="634c0-145">Пример</span><span class="sxs-lookup"><span data-stu-id="634c0-145">Example</span></span>

<span data-ttu-id="634c0-146">FIND ("2003", "1 января 2003 г.")</span><span class="sxs-lookup"><span data-stu-id="634c0-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="634c0-147">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="634c0-147">Returns 12.</span></span> 
  

