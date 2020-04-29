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
description: Находит одну текстовую строку, содержащуюся в другой текстовой строке, и возвращает начальную позицию искомой текстовой строки относительно ее позиции в текстовой строке, содержащей ее.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426578"
---
# <a name="find-function"></a><span data-ttu-id="eaa6f-103">Функция FIND</span><span class="sxs-lookup"><span data-stu-id="eaa6f-103">FIND Function</span></span>

<span data-ttu-id="eaa6f-104">Находит одну текстовую строку, содержащуюся в другой текстовой строке, и возвращает начальную позицию искомой текстовой строки относительно ее позиции в текстовой строке, содержащей ее.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eaa6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eaa6f-105">Syntax</span></span>

<span data-ttu-id="eaa6f-106">Find (\* \* *find_text* \* \*, \* \* *within_text* \* *, [* \* *start_num* \* *], [* \* *ignore_case* \* \*])</span><span class="sxs-lookup"><span data-stu-id="eaa6f-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eaa6f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaa6f-107">Parameters</span></span>

|<span data-ttu-id="eaa6f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-108">**Name**</span></span>|<span data-ttu-id="eaa6f-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-109">**Required/Optional**</span></span>|<span data-ttu-id="eaa6f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-110">**Data Type**</span></span>|<span data-ttu-id="eaa6f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eaa6f-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="eaa6f-112">_find_text_</span></span> <br/> |<span data-ttu-id="eaa6f-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eaa6f-113">Required</span></span>  <br/> |<span data-ttu-id="eaa6f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-114">**String**</span></span> <br/> |<span data-ttu-id="eaa6f-115">Текстовая строка, которую нужно найти.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="eaa6f-116">_format_</span><span class="sxs-lookup"><span data-stu-id="eaa6f-116">_format_</span></span> <br/> |<span data-ttu-id="eaa6f-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eaa6f-117">Required</span></span>  <br/> |<span data-ttu-id="eaa6f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-118">**String**</span></span> <br/> |<span data-ttu-id="eaa6f-119">Текстовая строка, содержащая текст, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="eaa6f-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="eaa6f-120">_start_num_</span></span> <br/> |<span data-ttu-id="eaa6f-121">Необязательна</span><span class="sxs-lookup"><span data-stu-id="eaa6f-121">Optional</span></span>  <br/> |<span data-ttu-id="eaa6f-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-122">**Number**</span></span> <br/> |<span data-ttu-id="eaa6f-123">Символ, с которого начинается поиск.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-123">The character at which to start the search.</span></span> <span data-ttu-id="eaa6f-124">Первый символ в _within_textю_ 1.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="eaa6f-125">Если _start_num_ отсутствует, предполагается, что он равен 1.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="eaa6f-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="eaa6f-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="eaa6f-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="eaa6f-127">Optional</span></span>  <br/> |<span data-ttu-id="eaa6f-128">**Логический**</span><span class="sxs-lookup"><span data-stu-id="eaa6f-128">**Boolean**</span></span> <br/> |<span data-ttu-id="eaa6f-129">По умолчанию функция поиска учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="eaa6f-130">Если вы хотите, чтобы функция поиска игнорировала регистр, установите для этого аргумента значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eaa6f-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaa6f-131">Return value</span></span>

<span data-ttu-id="eaa6f-132">Номер</span><span class="sxs-lookup"><span data-stu-id="eaa6f-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eaa6f-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="eaa6f-133">Remarks</span></span>

<span data-ttu-id="eaa6f-134">Если найдено несколько совпадений, функция найти Возвращает начальную позицию первого совпадения в строке.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="eaa6f-135">Аргумент _find_text_ не учитывает символы с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="eaa6f-136">Если _find_text_:</span><span class="sxs-lookup"><span data-stu-id="eaa6f-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="eaa6f-137">Не задан (""), то функция найти соответствует первому символу в строке поиска (то есть символу, пронумерованному _start_num_ или 1).</span><span class="sxs-lookup"><span data-stu-id="eaa6f-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="eaa6f-138">Не отображается в _within_text_, Find возвращает значение #VALUE!</span><span class="sxs-lookup"><span data-stu-id="eaa6f-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="eaa6f-139">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-139">error value.</span></span> 
    
<span data-ttu-id="eaa6f-140">Если _start_num_:</span><span class="sxs-lookup"><span data-stu-id="eaa6f-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="eaa6f-141">Не больше нуля (0), то FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="eaa6f-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="eaa6f-142">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-142">error value.</span></span> 
    
- <span data-ttu-id="eaa6f-143">Больше, чем длина _within_text_, финдретурнс #VALUE!</span><span class="sxs-lookup"><span data-stu-id="eaa6f-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="eaa6f-144">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="eaa6f-145">Пример</span><span class="sxs-lookup"><span data-stu-id="eaa6f-145">Example</span></span>

<span data-ttu-id="eaa6f-146">FIND ("2003", "1 января, 2003")</span><span class="sxs-lookup"><span data-stu-id="eaa6f-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="eaa6f-147">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="eaa6f-147">Returns 12.</span></span> 
  

