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
# <a name="find-function"></a><span data-ttu-id="a253a-103">Функция FIND</span><span class="sxs-lookup"><span data-stu-id="a253a-103">FIND Function</span></span>

<span data-ttu-id="a253a-104">Находит одну текстовую строку, содержащуюся в другой текстовой строке, и возвращает начальную позицию искомой текстовой строки относительно ее позиции в текстовой строке, содержащей ее.</span><span class="sxs-lookup"><span data-stu-id="a253a-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a253a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a253a-105">Syntax</span></span>

<span data-ttu-id="a253a-106">Find (\* \* *искомый_текст* \* \*, \* \* *просматриваемый_текст* \* *, [* \* *Нач_позиция* \* *], [* \* *игноре_касе* \* \*])</span><span class="sxs-lookup"><span data-stu-id="a253a-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a253a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a253a-107">Parameters</span></span>

|<span data-ttu-id="a253a-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a253a-108">**Name**</span></span>|<span data-ttu-id="a253a-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a253a-109">**Required/Optional**</span></span>|<span data-ttu-id="a253a-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a253a-110">**Data Type**</span></span>|<span data-ttu-id="a253a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a253a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a253a-112">_искомый_текст_</span><span class="sxs-lookup"><span data-stu-id="a253a-112">_find_text_</span></span> <br/> |<span data-ttu-id="a253a-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a253a-113">Required</span></span>  <br/> |<span data-ttu-id="a253a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a253a-114">**String**</span></span> <br/> |<span data-ttu-id="a253a-115">Текстовая строка, которую нужно найти.</span><span class="sxs-lookup"><span data-stu-id="a253a-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="a253a-116">_format_</span><span class="sxs-lookup"><span data-stu-id="a253a-116">_format_</span></span> <br/> |<span data-ttu-id="a253a-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a253a-117">Required</span></span>  <br/> |<span data-ttu-id="a253a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a253a-118">**String**</span></span> <br/> |<span data-ttu-id="a253a-119">Текстовая строка, содержащая текст, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="a253a-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="a253a-120">_равн_</span><span class="sxs-lookup"><span data-stu-id="a253a-120">_start_num_</span></span> <br/> |<span data-ttu-id="a253a-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a253a-121">Optional</span></span>  <br/> |<span data-ttu-id="a253a-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="a253a-122">**Number**</span></span> <br/> |<span data-ttu-id="a253a-123">Символ, с которого начинается поиск.</span><span class="sxs-lookup"><span data-stu-id="a253a-123">The character at which to start the search.</span></span> <span data-ttu-id="a253a-124">Первый символ в параметре _текст_для_поиска_ равен 1.</span><span class="sxs-lookup"><span data-stu-id="a253a-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="a253a-125">Если _аргумент нач_позиция_ отсутствует, предполагается, что он равен 1.</span><span class="sxs-lookup"><span data-stu-id="a253a-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="a253a-126">_игноре_касе_</span><span class="sxs-lookup"><span data-stu-id="a253a-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="a253a-127">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a253a-127">Optional</span></span>  <br/> |<span data-ttu-id="a253a-128">**Логический**</span><span class="sxs-lookup"><span data-stu-id="a253a-128">**Boolean**</span></span> <br/> |<span data-ttu-id="a253a-129">По умолчанию функция поиска учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a253a-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="a253a-130">Если вы хотите, чтобы функция поиска игнорировала регистр, установите для этого аргумента значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a253a-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a253a-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a253a-131">Return value</span></span>

<span data-ttu-id="a253a-132">Число</span><span class="sxs-lookup"><span data-stu-id="a253a-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a253a-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="a253a-133">Remarks</span></span>

<span data-ttu-id="a253a-134">Если найдено несколько совпадений, функция найти Возвращает начальную позицию первого совпадения в строке.</span><span class="sxs-lookup"><span data-stu-id="a253a-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="a253a-135">Аргумент _искомый_текст_ не учитывает символы с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="a253a-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="a253a-136">Если _искомый_текст_:</span><span class="sxs-lookup"><span data-stu-id="a253a-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="a253a-137">Является пустым (""), то функция найти соответствует первому символу в строке поиска (то есть символу номер _Нач_позиция_ или 1).</span><span class="sxs-lookup"><span data-stu-id="a253a-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="a253a-138">Не отображается в _просматриваемый_текст_, то FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a253a-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="a253a-139">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a253a-139">error value.</span></span> 
    
<span data-ttu-id="a253a-140">Если _Нач_позиция_:</span><span class="sxs-lookup"><span data-stu-id="a253a-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="a253a-141">Не больше нуля (0), то FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a253a-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="a253a-142">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a253a-142">error value.</span></span> 
    
- <span data-ttu-id="a253a-143">Больше, чем длина _просматриваемый_текст_, финдретурнс #VALUE!</span><span class="sxs-lookup"><span data-stu-id="a253a-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="a253a-144">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a253a-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="a253a-145">Пример</span><span class="sxs-lookup"><span data-stu-id="a253a-145">Example</span></span>

<span data-ttu-id="a253a-146">FIND ("2003", "1 января, 2003")</span><span class="sxs-lookup"><span data-stu-id="a253a-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="a253a-147">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="a253a-147">Returns 12.</span></span> 
  

