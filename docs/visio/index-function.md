---
title: Функция INDEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Возвращает подстроку в индексе расположения с отсчетом от нуля в списке, разделенном разделителем. Если индекс находится вне диапазона, возвращается пустая строка или необязательный маркер, указанный в качестве аргумента еррорвалуе.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431577"
---
# <a name="index-function"></a><span data-ttu-id="b17d3-104">Функция INDEX</span><span class="sxs-lookup"><span data-stu-id="b17d3-104">INDEX Function</span></span>

<span data-ttu-id="b17d3-105">Возвращает подстроку в _индексе_ расположения с отсчетом от нуля в _списке_ , разделенном _разделителем_.</span><span class="sxs-lookup"><span data-stu-id="b17d3-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="b17d3-106">Если индекс находится вне диапазона, возвращается пустая строка или необязательный маркер, указанный в качестве аргумента *еррорвалуе* .</span><span class="sxs-lookup"><span data-stu-id="b17d3-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b17d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b17d3-107">Syntax</span></span>

<span data-ttu-id="b17d3-108">Index (\* \* *index* \* *, "* \* *List* \* *" [, [* \* *Разделитель* \* *] [, [* \* *еррорвалуе* \* \*]]])</span><span class="sxs-lookup"><span data-stu-id="b17d3-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b17d3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b17d3-109">Parameters</span></span>

|<span data-ttu-id="b17d3-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b17d3-110">**Name**</span></span>|<span data-ttu-id="b17d3-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b17d3-111">**Required/Optional**</span></span>|<span data-ttu-id="b17d3-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b17d3-112">**Data Type**</span></span>|<span data-ttu-id="b17d3-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b17d3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b17d3-114">_index_</span><span class="sxs-lookup"><span data-stu-id="b17d3-114">_index_</span></span> <br/> |<span data-ttu-id="b17d3-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="b17d3-115">Required</span></span>  <br/> |<span data-ttu-id="b17d3-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="b17d3-116">**Number**</span></span> <br/> |<span data-ttu-id="b17d3-117">Расположение, которое требуется найти.</span><span class="sxs-lookup"><span data-stu-id="b17d3-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="b17d3-118">_list_</span><span class="sxs-lookup"><span data-stu-id="b17d3-118">_list_</span></span> <br/> |<span data-ttu-id="b17d3-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b17d3-119">Required</span></span>  <br/> |<span data-ttu-id="b17d3-120">**String**</span><span class="sxs-lookup"><span data-stu-id="b17d3-120">**String**</span></span> <br/> |<span data-ttu-id="b17d3-121">Список, в котором необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="b17d3-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="b17d3-122">_разделитель_</span><span class="sxs-lookup"><span data-stu-id="b17d3-122">_delimiter_</span></span> <br/> |<span data-ttu-id="b17d3-123">Необязательна</span><span class="sxs-lookup"><span data-stu-id="b17d3-123">Optional</span></span>  <br/> |<span data-ttu-id="b17d3-124">**String**</span><span class="sxs-lookup"><span data-stu-id="b17d3-124">**String**</span></span> <br/> | <span data-ttu-id="b17d3-125">Строка, используемая в качестве разделителя в _списке_.</span><span class="sxs-lookup"><span data-stu-id="b17d3-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="b17d3-126">Строка _разделителя_ может иметь длину более одного символа и содержать многобайтовые символы.</span><span class="sxs-lookup"><span data-stu-id="b17d3-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="b17d3-127">Значение по умолчанию — точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="b17d3-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="b17d3-128">_еррорвалуе_</span><span class="sxs-lookup"><span data-stu-id="b17d3-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="b17d3-129">Необязательна</span><span class="sxs-lookup"><span data-stu-id="b17d3-129">Optional</span></span>  <br/> |<span data-ttu-id="b17d3-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="b17d3-130">**Number**</span></span> <br/> | <span data-ttu-id="b17d3-131">Заданное пользователем значение, которое возвращается, если индекс находится вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="b17d3-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="b17d3-132">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="b17d3-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b17d3-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="b17d3-133">Remarks</span></span>

<span data-ttu-id="b17d3-134">Если список начинается или заканчивается разделителем, считается, что пустая строка существует до или после списка.</span><span class="sxs-lookup"><span data-stu-id="b17d3-134">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="b17d3-135">Последовательные разделители подразумевают пустую строку между.</span><span class="sxs-lookup"><span data-stu-id="b17d3-135">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="b17d3-136">Если индекс находится вне диапазона, Visio возвращает пустую строку или необязательный маркер, указанный в качестве аргумента *еррорвалуе* .</span><span class="sxs-lookup"><span data-stu-id="b17d3-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b17d3-137">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b17d3-137">Example 1</span></span>

<span data-ttu-id="b17d3-138">Индекс (3, "Cat; Rat;; Гоат ")</span><span class="sxs-lookup"><span data-stu-id="b17d3-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="b17d3-139">Возвращает значение "Гоат".</span><span class="sxs-lookup"><span data-stu-id="b17d3-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b17d3-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b17d3-140">Example 2</span></span>

<span data-ttu-id="b17d3-141">ИНДЕКС (54, "; 1; 2; 3;", "ОШИБКА")</span><span class="sxs-lookup"><span data-stu-id="b17d3-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="b17d3-142">Возвращает значение "ERROR".</span><span class="sxs-lookup"><span data-stu-id="b17d3-142">Returns "ERROR".</span></span>
  

