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
description: Возвращает отсчитываемый от нуля индекс, который указывает расположение ключа подстроки в списке, или возвращает значение -1, если конечная строка содержит разделитель.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814177"
---
# <a name="lookup-function"></a><span data-ttu-id="1eb07-103">Функция LOOKUP</span><span class="sxs-lookup"><span data-stu-id="1eb07-103">LOOKUP Function</span></span>

<span data-ttu-id="1eb07-104">Возвращает отсчитываемый от нуля индекс, который указывает расположение подстроки _ключа_ в виде _списка_, или возвращает значение -1, если конечная строка содержит _разделитель_.</span><span class="sxs-lookup"><span data-stu-id="1eb07-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1eb07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1eb07-105">Syntax</span></span>

<span data-ttu-id="1eb07-106">ПОДСТАНОВКИ ("** *ключ* **","** *списка* **"[,"** *разделитель* **"])</span><span class="sxs-lookup"><span data-stu-id="1eb07-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1eb07-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1eb07-107">Parameters</span></span>

|<span data-ttu-id="1eb07-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1eb07-108">**Name**</span></span>|<span data-ttu-id="1eb07-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="1eb07-109">**Required/Optional**</span></span>|<span data-ttu-id="1eb07-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1eb07-110">**Data Type**</span></span>|<span data-ttu-id="1eb07-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1eb07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1eb07-112">_ключ_</span><span class="sxs-lookup"><span data-stu-id="1eb07-112">_key_</span></span> <br/> |<span data-ttu-id="1eb07-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1eb07-113">Required</span></span>  <br/> |<span data-ttu-id="1eb07-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="1eb07-114">**String**</span></span> <br/> |<span data-ttu-id="1eb07-115">Строка, которую требуется найти.</span><span class="sxs-lookup"><span data-stu-id="1eb07-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="1eb07-116">_списки_</span><span class="sxs-lookup"><span data-stu-id="1eb07-116">_list_</span></span> <br/> |<span data-ttu-id="1eb07-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1eb07-117">Required</span></span>  <br/> |<span data-ttu-id="1eb07-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="1eb07-118">**String**</span></span> <br/> | <span data-ttu-id="1eb07-119">Список, в котором требуется выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="1eb07-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="1eb07-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="1eb07-120">_delimiter_</span></span> <br/> |<span data-ttu-id="1eb07-121">Optional</span><span class="sxs-lookup"><span data-stu-id="1eb07-121">Optional</span></span>  <br/> |<span data-ttu-id="1eb07-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="1eb07-122">**String**</span></span> <br/> | <span data-ttu-id="1eb07-123">Строка для использования в качестве разделителя в _списке_.</span><span class="sxs-lookup"><span data-stu-id="1eb07-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="1eb07-124">Строка _разделителя_ может быть несколько символов в длину и может включать многобайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="1eb07-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="1eb07-125">Значение по умолчанию — точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1eb07-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1eb07-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="1eb07-127">Числовой</span><span class="sxs-lookup"><span data-stu-id="1eb07-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1eb07-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="1eb07-128">Remarks</span></span>

<span data-ttu-id="1eb07-129">Функция поиска использует поиск без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="1eb07-129">The LOOKUP function uses a case-insensitive search.</span></span> <span data-ttu-id="1eb07-130">Если список начинается или заканчивается на разделителя, предполагается, что строка значение null, существующих до или после списка.</span><span class="sxs-lookup"><span data-stu-id="1eb07-130">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list.</span></span> <span data-ttu-id="1eb07-131">Последовательные разделители между подразумевает пустая строка.</span><span class="sxs-lookup"><span data-stu-id="1eb07-131">Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="1eb07-132">Все аргументы должны быть строки или выражения, которые могут быть преобразованы в строки.</span><span class="sxs-lookup"><span data-stu-id="1eb07-132">All the arguments must be strings or expressions that can be converted to strings.</span></span> <span data-ttu-id="1eb07-133">Если это не так, вызвавшей ошибку аргумент заменяется пустую строку.</span><span class="sxs-lookup"><span data-stu-id="1eb07-133">If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1eb07-134">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1eb07-134">Example 1</span></span>

<span data-ttu-id="1eb07-135">ПОДСТАНОВКИ ("rat", "кошка; rat; goat»)</span><span class="sxs-lookup"><span data-stu-id="1eb07-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="1eb07-136">Возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="1eb07-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1eb07-137">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1eb07-137">Example 2</span></span>

<span data-ttu-id="1eb07-138">ПОДСТАНОВКИ ("","; кошка; rat; goat»)</span><span class="sxs-lookup"><span data-stu-id="1eb07-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="1eb07-139">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="1eb07-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1eb07-140">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1eb07-140">Example 3</span></span>

<span data-ttu-id="1eb07-141">ПОДСТАНОВКИ ("t", "кошка; rat; goat», «»)</span><span class="sxs-lookup"><span data-stu-id="1eb07-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="1eb07-142">Возврат значения 3.</span><span class="sxs-lookup"><span data-stu-id="1eb07-142">Returns 3.</span></span>
  

