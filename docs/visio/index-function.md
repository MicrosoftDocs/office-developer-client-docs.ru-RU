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
description: Возвращает подстроку в индексе расположения на основе нуля в списке, относя к списку с помощью делегировок. Или, если индекс находится вне диапазона, возвращает пустую строку или необязательный маркер, предоставленный в качестве аргумента errorvalue.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431577"
---
# <a name="index-function"></a><span data-ttu-id="14e14-104">Функция INDEX</span><span class="sxs-lookup"><span data-stu-id="14e14-104">INDEX Function</span></span>

<span data-ttu-id="14e14-105">Возвращает подстроку в индексе расположения  на  основе нуля в списке, относя к списку с помощью _делегировок._</span><span class="sxs-lookup"><span data-stu-id="14e14-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="14e14-106">Или, если индекс находится вне диапазона, возвращает пустую строку или необязательный маркер, предоставленный в качестве *аргумента errorvalue.*</span><span class="sxs-lookup"><span data-stu-id="14e14-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="14e14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14e14-107">Syntax</span></span>

<span data-ttu-id="14e14-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span><span class="sxs-lookup"><span data-stu-id="14e14-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="14e14-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="14e14-109">Parameters</span></span>

|<span data-ttu-id="14e14-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="14e14-110">**Name**</span></span>|<span data-ttu-id="14e14-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="14e14-111">**Required/Optional**</span></span>|<span data-ttu-id="14e14-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="14e14-112">**Data Type**</span></span>|<span data-ttu-id="14e14-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14e14-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="14e14-114">_индекс_</span><span class="sxs-lookup"><span data-stu-id="14e14-114">_index_</span></span> <br/> |<span data-ttu-id="14e14-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="14e14-115">Required</span></span>  <br/> |<span data-ttu-id="14e14-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="14e14-116">**Number**</span></span> <br/> |<span data-ttu-id="14e14-117">Расположение, которое вы хотите найти.</span><span class="sxs-lookup"><span data-stu-id="14e14-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="14e14-118">_списке_</span><span class="sxs-lookup"><span data-stu-id="14e14-118">_list_</span></span> <br/> |<span data-ttu-id="14e14-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="14e14-119">Required</span></span>  <br/> |<span data-ttu-id="14e14-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="14e14-120">**String**</span></span> <br/> |<span data-ttu-id="14e14-121">Список, в котором нужно найти.</span><span class="sxs-lookup"><span data-stu-id="14e14-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="14e14-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="14e14-122">_delimiter_</span></span> <br/> |<span data-ttu-id="14e14-123">Необязательна</span><span class="sxs-lookup"><span data-stu-id="14e14-123">Optional</span></span>  <br/> |<span data-ttu-id="14e14-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="14e14-124">**String**</span></span> <br/> | <span data-ttu-id="14e14-125">Строка, используемая в качестве делегировки в _списке._</span><span class="sxs-lookup"><span data-stu-id="14e14-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="14e14-126">Строка  _с делегировкой_ может иметь длину более одного символа и включать многобайтные символы.</span><span class="sxs-lookup"><span data-stu-id="14e14-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="14e14-127">Значение по умолчанию — 1 с зачетом.</span><span class="sxs-lookup"><span data-stu-id="14e14-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="14e14-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="14e14-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="14e14-129">Необязательна</span><span class="sxs-lookup"><span data-stu-id="14e14-129">Optional</span></span>  <br/> |<span data-ttu-id="14e14-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="14e14-130">**Number**</span></span> <br/> | <span data-ttu-id="14e14-131">Указанное пользователем значение, возвращаемого, если индекс находится вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="14e14-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="14e14-132">Значение по умолчанию — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="14e14-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14e14-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="14e14-133">Remarks</span></span>

<span data-ttu-id="14e14-134">Если список начинается или заканчивается с помощью разбиений, предполагается, что строка null существует до или после списка.</span><span class="sxs-lookup"><span data-stu-id="14e14-134">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="14e14-135">Последовательные заметивы подразумевают нулевую строку между ними.</span><span class="sxs-lookup"><span data-stu-id="14e14-135">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="14e14-136">Если индекс находится вне диапазона, Visio возвращает пустую строку или необязательный маркер, предоставленный в качестве *аргумента errorvalue.*</span><span class="sxs-lookup"><span data-stu-id="14e14-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="14e14-137">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14e14-137">Example 1</span></span>

<span data-ttu-id="14e14-138">INDEX(3,"cat;cat;; ")</span><span class="sxs-lookup"><span data-stu-id="14e14-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="14e14-139">Возвращает "ветвь".</span><span class="sxs-lookup"><span data-stu-id="14e14-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="14e14-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="14e14-140">Example 2</span></span>

<span data-ttu-id="14e14-141">INDEX(54,";1;2;3;","ERROR")</span><span class="sxs-lookup"><span data-stu-id="14e14-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="14e14-142">Возвращает "ERROR".</span><span class="sxs-lookup"><span data-stu-id="14e14-142">Returns "ERROR".</span></span>
  

