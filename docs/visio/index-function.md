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
description: Возвращает подстройку в нулевом индексе расположения в списке, делимитером. Или, если индекс находится вне диапазона, возвращает пустую строку или необязательный маркер, предоставленный в качестве аргумента errorvalue.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431577"
---
# <a name="index-function"></a><span data-ttu-id="158b6-104">Функция INDEX</span><span class="sxs-lookup"><span data-stu-id="158b6-104">INDEX Function</span></span>

<span data-ttu-id="158b6-105">Возвращает подстройку в нулевом  индексе  расположения в списке, делимитером. </span><span class="sxs-lookup"><span data-stu-id="158b6-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="158b6-106">Или, если индекс находится вне диапазона, возвращает пустую строку или необязательный маркер, предоставленный в качестве *аргумента errorvalue.*</span><span class="sxs-lookup"><span data-stu-id="158b6-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="158b6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="158b6-107">Syntax</span></span>

<span data-ttu-id="158b6-108">INDEX(\*\* *index* **," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][[** *errorvalue* \*\* ]]]</span><span class="sxs-lookup"><span data-stu-id="158b6-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="158b6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="158b6-109">Parameters</span></span>

|<span data-ttu-id="158b6-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="158b6-110">**Name**</span></span>|<span data-ttu-id="158b6-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="158b6-111">**Required/Optional**</span></span>|<span data-ttu-id="158b6-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="158b6-112">**Data Type**</span></span>|<span data-ttu-id="158b6-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="158b6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="158b6-114">_index_</span><span class="sxs-lookup"><span data-stu-id="158b6-114">_index_</span></span> <br/> |<span data-ttu-id="158b6-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="158b6-115">Required</span></span>  <br/> |<span data-ttu-id="158b6-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="158b6-116">**Number**</span></span> <br/> |<span data-ttu-id="158b6-117">Расположение, которое вы хотите найти.</span><span class="sxs-lookup"><span data-stu-id="158b6-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="158b6-118">_list_</span><span class="sxs-lookup"><span data-stu-id="158b6-118">_list_</span></span> <br/> |<span data-ttu-id="158b6-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="158b6-119">Required</span></span>  <br/> |<span data-ttu-id="158b6-120">**String**</span><span class="sxs-lookup"><span data-stu-id="158b6-120">**String**</span></span> <br/> |<span data-ttu-id="158b6-121">Список, в котором необходимо искать.</span><span class="sxs-lookup"><span data-stu-id="158b6-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="158b6-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="158b6-122">_delimiter_</span></span> <br/> |<span data-ttu-id="158b6-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="158b6-123">Optional</span></span>  <br/> |<span data-ttu-id="158b6-124">**String**</span><span class="sxs-lookup"><span data-stu-id="158b6-124">**String**</span></span> <br/> | <span data-ttu-id="158b6-125">Строка, используемая в качестве делимитера в _списке._</span><span class="sxs-lookup"><span data-stu-id="158b6-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="158b6-126">Строка  _delimiter_ может иметь несколько символов в длину и включать многобайтные символы.</span><span class="sxs-lookup"><span data-stu-id="158b6-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="158b6-127">По умолчанию это полуколон.</span><span class="sxs-lookup"><span data-stu-id="158b6-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="158b6-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="158b6-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="158b6-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="158b6-129">Optional</span></span>  <br/> |<span data-ttu-id="158b6-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="158b6-130">**Number**</span></span> <br/> | <span data-ttu-id="158b6-131">Значение, указанное пользователем, возвращается, если индекс находится вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="158b6-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="158b6-132">По умолчанию это пустая строка.</span><span class="sxs-lookup"><span data-stu-id="158b6-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="158b6-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="158b6-133">Remarks</span></span>

<span data-ttu-id="158b6-134">Если список начинается или заканчивается делимитером, предполагается, что строка null существует до или после списка.</span><span class="sxs-lookup"><span data-stu-id="158b6-134">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="158b6-135">Последовательные делимитеры подразумевают нулевую строку между ними.</span><span class="sxs-lookup"><span data-stu-id="158b6-135">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="158b6-136">Если индекс находится вне диапазона, Visio возвращает пустую строку или необязательный маркер, предоставленный в качестве *аргумента errorvalue.*</span><span class="sxs-lookup"><span data-stu-id="158b6-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="158b6-137">Пример 1</span><span class="sxs-lookup"><span data-stu-id="158b6-137">Example 1</span></span>

<span data-ttu-id="158b6-138">INDEX (3,"cat;rat;; коза")</span><span class="sxs-lookup"><span data-stu-id="158b6-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="158b6-139">Возвращает "козу".</span><span class="sxs-lookup"><span data-stu-id="158b6-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="158b6-140">Пример 2</span><span class="sxs-lookup"><span data-stu-id="158b6-140">Example 2</span></span>

<span data-ttu-id="158b6-141">INDEX (54,";1;2;3;","ERROR")</span><span class="sxs-lookup"><span data-stu-id="158b6-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="158b6-142">Возвращает "ERROR".</span><span class="sxs-lookup"><span data-stu-id="158b6-142">Returns "ERROR".</span></span>
  

