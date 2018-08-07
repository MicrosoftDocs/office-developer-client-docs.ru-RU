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
description: Возвращает подстроки в индекс с отсчетом от нуля местоположение в списке разделителем. Или, если индекс находится вне диапазона, возвращает пустую строку или маркер необязательно, представленные в качестве аргумента errorvalue.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813952"
---
# <a name="index-function"></a><span data-ttu-id="6e00c-104">Функция INDEX</span><span class="sxs-lookup"><span data-stu-id="6e00c-104">INDEX Function</span></span>

<span data-ttu-id="6e00c-105">Возвращает подстроки с отсчетом от нуля расположение _индекса_ в _списке_ _разделителем_.</span><span class="sxs-lookup"><span data-stu-id="6e00c-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="6e00c-106">Или, если индекс находится вне диапазона, возвращает пустую строку или маркер необязательно, представленные в качестве аргумента *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="6e00c-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6e00c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e00c-107">Syntax</span></span>

<span data-ttu-id="6e00c-108">Индекс (** *индекса* **, "** *списка* **" [, [** *разделитель* **] [, [** *errorvalue* **]]])</span><span class="sxs-lookup"><span data-stu-id="6e00c-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e00c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e00c-109">Parameters</span></span>

|<span data-ttu-id="6e00c-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6e00c-110">**Name**</span></span>|<span data-ttu-id="6e00c-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6e00c-111">**Required/Optional**</span></span>|<span data-ttu-id="6e00c-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6e00c-112">**Data Type**</span></span>|<span data-ttu-id="6e00c-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e00c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e00c-114">_index_</span><span class="sxs-lookup"><span data-stu-id="6e00c-114">_index_</span></span> <br/> |<span data-ttu-id="6e00c-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e00c-115">Required</span></span>  <br/> |<span data-ttu-id="6e00c-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="6e00c-116">**Number**</span></span> <br/> |<span data-ttu-id="6e00c-117">Расположение, которое требуется найти.</span><span class="sxs-lookup"><span data-stu-id="6e00c-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="6e00c-118">_списки_</span><span class="sxs-lookup"><span data-stu-id="6e00c-118">_list_</span></span> <br/> |<span data-ttu-id="6e00c-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e00c-119">Required</span></span>  <br/> |<span data-ttu-id="6e00c-120">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6e00c-120">**String**</span></span> <br/> |<span data-ttu-id="6e00c-121">Список, в котором требуется выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="6e00c-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="6e00c-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="6e00c-122">_delimiter_</span></span> <br/> |<span data-ttu-id="6e00c-123">Optional</span><span class="sxs-lookup"><span data-stu-id="6e00c-123">Optional</span></span>  <br/> |<span data-ttu-id="6e00c-124">**Строка**</span><span class="sxs-lookup"><span data-stu-id="6e00c-124">**String**</span></span> <br/> | <span data-ttu-id="6e00c-125">Строка для использования в качестве разделителя в _списке_.</span><span class="sxs-lookup"><span data-stu-id="6e00c-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="6e00c-126">Строка _разделителя_ может быть несколько символов в длину и включать многобайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="6e00c-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="6e00c-127">Значение по умолчанию — точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="6e00c-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="6e00c-128">_ERRORVALUE_</span><span class="sxs-lookup"><span data-stu-id="6e00c-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="6e00c-129">Optional</span><span class="sxs-lookup"><span data-stu-id="6e00c-129">Optional</span></span>  <br/> |<span data-ttu-id="6e00c-130">**Число**</span><span class="sxs-lookup"><span data-stu-id="6e00c-130">**Number**</span></span> <br/> | <span data-ttu-id="6e00c-131">Определенные пользователем значения для возврата, если индекс находится вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="6e00c-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="6e00c-132">По умолчанию используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="6e00c-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e00c-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e00c-133">Remarks</span></span>

<span data-ttu-id="6e00c-134">Если список начинается или заканчивается на разделителя, предполагается, что строка значение null, существующих до или после списка.</span><span class="sxs-lookup"><span data-stu-id="6e00c-134">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="6e00c-135">Последовательные разделители между подразумевает пустая строка.</span><span class="sxs-lookup"><span data-stu-id="6e00c-135">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="6e00c-136">Если индекс находится вне диапазона, Visio возвращает пустую строку или необязательный маркер, предоставленный в качестве аргумента *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="6e00c-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6e00c-137">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e00c-137">Example 1</span></span>

<span data-ttu-id="6e00c-138">Индекс (3, "кошка; rat; goat»)</span><span class="sxs-lookup"><span data-stu-id="6e00c-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="6e00c-139">Возвращает «goat».</span><span class="sxs-lookup"><span data-stu-id="6e00c-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6e00c-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e00c-140">Example 2</span></span>

<span data-ttu-id="6e00c-141">INDEX(54,";1;2;3;",,"ERROR")</span><span class="sxs-lookup"><span data-stu-id="6e00c-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="6e00c-142">Возврат значения «Ошибка».</span><span class="sxs-lookup"><span data-stu-id="6e00c-142">Returns "ERROR".</span></span>
  

