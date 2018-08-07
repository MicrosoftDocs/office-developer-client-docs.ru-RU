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
description: Находит одной строки текста, содержащихся в другую строку текста и возвращает положение начала текстовой строки, вы ищете относительно его положения текстовой строки, содержащей его.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813790"
---
# <a name="find-function"></a><span data-ttu-id="46f75-103">Функция FIND</span><span class="sxs-lookup"><span data-stu-id="46f75-103">FIND Function</span></span>

<span data-ttu-id="46f75-104">Находит одной строки текста, содержащихся в другую строку текста и возвращает положение начала текстовой строки, вы ищете относительно его положения текстовой строки, содержащей его.</span><span class="sxs-lookup"><span data-stu-id="46f75-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="46f75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46f75-105">Syntax</span></span>

<span data-ttu-id="46f75-106">Поиск (** *искомого* **, ** *левого края текста* **, [** *Начальная позиция* **], [** *ignore_case* **])</span><span class="sxs-lookup"><span data-stu-id="46f75-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="46f75-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46f75-107">Parameters</span></span>

|<span data-ttu-id="46f75-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="46f75-108">**Name**</span></span>|<span data-ttu-id="46f75-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="46f75-109">**Required/Optional**</span></span>|<span data-ttu-id="46f75-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="46f75-110">**Data Type**</span></span>|<span data-ttu-id="46f75-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46f75-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="46f75-112">_искомого_</span><span class="sxs-lookup"><span data-stu-id="46f75-112">_find_text_</span></span> <br/> |<span data-ttu-id="46f75-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46f75-113">Required</span></span>  <br/> |<span data-ttu-id="46f75-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="46f75-114">**String**</span></span> <br/> |<span data-ttu-id="46f75-115">Строка текста, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="46f75-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="46f75-116">_format_</span><span class="sxs-lookup"><span data-stu-id="46f75-116">_format_</span></span> <br/> |<span data-ttu-id="46f75-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46f75-117">Required</span></span>  <br/> |<span data-ttu-id="46f75-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="46f75-118">**String**</span></span> <br/> |<span data-ttu-id="46f75-119">Текстовая строка, содержащая текст, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="46f75-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="46f75-120">_Начальная позиция_</span><span class="sxs-lookup"><span data-stu-id="46f75-120">_start_num_</span></span> <br/> |<span data-ttu-id="46f75-121">Optional</span><span class="sxs-lookup"><span data-stu-id="46f75-121">Optional</span></span>  <br/> |<span data-ttu-id="46f75-122">**Число**</span><span class="sxs-lookup"><span data-stu-id="46f75-122">**Number**</span></span> <br/> |<span data-ttu-id="46f75-123">Символ, с которого следует начать поиск.</span><span class="sxs-lookup"><span data-stu-id="46f75-123">The character at which to start the search.</span></span> <span data-ttu-id="46f75-124">Первого знака _Укажите_ -1.</span><span class="sxs-lookup"><span data-stu-id="46f75-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="46f75-125">Если _Начальная позиция_ отсутствует, то предполагается, что оно является 1.</span><span class="sxs-lookup"><span data-stu-id="46f75-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="46f75-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="46f75-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="46f75-127">Optional</span><span class="sxs-lookup"><span data-stu-id="46f75-127">Optional</span></span>  <br/> |<span data-ttu-id="46f75-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="46f75-128">**Boolean**</span></span> <br/> |<span data-ttu-id="46f75-129">По умолчанию функция поиска с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="46f75-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="46f75-130">Функции поиска, следует ли игнорировать регистр, установите этот аргумент значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="46f75-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="46f75-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="46f75-132">Number</span><span class="sxs-lookup"><span data-stu-id="46f75-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46f75-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="46f75-133">Remarks</span></span>

<span data-ttu-id="46f75-134">Если несколько совпадений, функция найти возвращает позицию первого соответствия в строке.</span><span class="sxs-lookup"><span data-stu-id="46f75-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="46f75-135">Аргумент _искомого_ необходимо учитывать символы быть подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="46f75-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="46f75-136">Если _искомого_:</span><span class="sxs-lookup"><span data-stu-id="46f75-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="46f75-137">Пустое ("»), найти совпадает с первым символом в строке поиска (то есть, знак с номером _Начальная позиция_ или 1).</span><span class="sxs-lookup"><span data-stu-id="46f75-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="46f75-138">Не отображается в _левого края текста_, FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="46f75-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="46f75-139">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="46f75-139">error value.</span></span> 
    
<span data-ttu-id="46f75-140">Если _Начальная позиция_:</span><span class="sxs-lookup"><span data-stu-id="46f75-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="46f75-141">Не больше, чем нуль (0), FIND возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="46f75-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="46f75-142">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="46f75-142">error value.</span></span> 
    
- <span data-ttu-id="46f75-143">Больше, чем длина _левого края текста_, FINDreturns #VALUE!</span><span class="sxs-lookup"><span data-stu-id="46f75-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="46f75-144">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="46f75-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="46f75-145">Пример</span><span class="sxs-lookup"><span data-stu-id="46f75-145">Example</span></span>

<span data-ttu-id="46f75-146">Поиск («2003», «1 января 2003»)</span><span class="sxs-lookup"><span data-stu-id="46f75-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="46f75-147">Возвращает 12.</span><span class="sxs-lookup"><span data-stu-id="46f75-147">Returns 12.</span></span> 
  

