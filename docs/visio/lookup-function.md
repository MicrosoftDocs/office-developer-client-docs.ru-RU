---
title: Функция LOOKUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Возвращает отсчитываемый от нуля индекс, указывающий расположение ключа подстроки в списке, или значение "– 1", если целевая строка содержит разделитель.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410331"
---
# <a name="lookup-function"></a><span data-ttu-id="391ab-103">Функция LOOKUP</span><span class="sxs-lookup"><span data-stu-id="391ab-103">LOOKUP Function</span></span>

<span data-ttu-id="391ab-104">Возвращает отсчитываемый от нуля индекс, указывающий расположение _ключа_ подстроки в _списке_, или значение "– 1", если целевая строка содержит _Разделитель_.</span><span class="sxs-lookup"><span data-stu-id="391ab-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="391ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="391ab-105">Syntax</span></span>

<span data-ttu-id="391ab-106">Lookup ("\* \* *Key* \* *", "* \* *List* \* *" [, "* \* *Разделитель* \* \*"])</span><span class="sxs-lookup"><span data-stu-id="391ab-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="391ab-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="391ab-107">Parameters</span></span>

|<span data-ttu-id="391ab-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="391ab-108">**Name**</span></span>|<span data-ttu-id="391ab-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="391ab-109">**Required/Optional**</span></span>|<span data-ttu-id="391ab-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="391ab-110">**Data Type**</span></span>|<span data-ttu-id="391ab-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="391ab-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="391ab-112">_key_</span><span class="sxs-lookup"><span data-stu-id="391ab-112">_key_</span></span> <br/> |<span data-ttu-id="391ab-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="391ab-113">Required</span></span>  <br/> |<span data-ttu-id="391ab-114">**String**</span><span class="sxs-lookup"><span data-stu-id="391ab-114">**String**</span></span> <br/> |<span data-ttu-id="391ab-115">Строка, которую требуется найти.</span><span class="sxs-lookup"><span data-stu-id="391ab-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="391ab-116">_list_</span><span class="sxs-lookup"><span data-stu-id="391ab-116">_list_</span></span> <br/> |<span data-ttu-id="391ab-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="391ab-117">Required</span></span>  <br/> |<span data-ttu-id="391ab-118">**String**</span><span class="sxs-lookup"><span data-stu-id="391ab-118">**String**</span></span> <br/> | <span data-ttu-id="391ab-119">Список, в котором необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="391ab-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="391ab-120">_разделитель_</span><span class="sxs-lookup"><span data-stu-id="391ab-120">_delimiter_</span></span> <br/> |<span data-ttu-id="391ab-121">Необязательный</span><span class="sxs-lookup"><span data-stu-id="391ab-121">Optional</span></span>  <br/> |<span data-ttu-id="391ab-122">**String**</span><span class="sxs-lookup"><span data-stu-id="391ab-122">**String**</span></span> <br/> | <span data-ttu-id="391ab-123">Строка, используемая в качестве разделителя в _списке_.</span><span class="sxs-lookup"><span data-stu-id="391ab-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="391ab-124">Строка _разделителя_ может иметь длину более одного символа и может содержать многобайтовые символы.</span><span class="sxs-lookup"><span data-stu-id="391ab-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="391ab-125">Значение по умолчанию — точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="391ab-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="391ab-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="391ab-126">Return value</span></span>

<span data-ttu-id="391ab-127">Числовой</span><span class="sxs-lookup"><span data-stu-id="391ab-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="391ab-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="391ab-128">Remarks</span></span>

<span data-ttu-id="391ab-129">Функция поиска использует поиск без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="391ab-129">The LOOKUP function uses a case-insensitive search.</span></span> <span data-ttu-id="391ab-130">Если список начинается или заканчивается разделителем, считается, что пустая строка существует до или после списка.</span><span class="sxs-lookup"><span data-stu-id="391ab-130">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="391ab-131">Последовательные разделители подразумевают пустую строку между.</span><span class="sxs-lookup"><span data-stu-id="391ab-131">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="391ab-132">Все аргументы должны быть строками или выражениями, которые могут быть преобразованы в строки.</span><span class="sxs-lookup"><span data-stu-id="391ab-132">All the arguments must be strings or expressions that can be converted to strings.</span></span> <span data-ttu-id="391ab-133">В противном случае для аргумента, вызывающего ошибку, заменяется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="391ab-133">If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="391ab-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="391ab-134">Example 1</span></span>

<span data-ttu-id="391ab-135">Поиск ("Rat", "Cat; Rat;"; Гоат ")</span><span class="sxs-lookup"><span data-stu-id="391ab-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="391ab-136">Возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="391ab-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="391ab-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="391ab-137">Example 2</span></span>

<span data-ttu-id="391ab-138">Поиск ("", "; Cat; Rat;; Гоат ")</span><span class="sxs-lookup"><span data-stu-id="391ab-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="391ab-139">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="391ab-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="391ab-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="391ab-140">Example 3</span></span>

<span data-ttu-id="391ab-141">Поиск ("t", "Cat; Rat;; Гоат "," a ")</span><span class="sxs-lookup"><span data-stu-id="391ab-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="391ab-142">Возвращает значение 3.</span><span class="sxs-lookup"><span data-stu-id="391ab-142">Returns 3.</span></span>
  

