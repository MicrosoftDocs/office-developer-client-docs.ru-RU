---
title: Функция SUBSTITUTE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Заменяет часть текстовой строки другой строкой текста.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814970"
---
# <a name="substitute-function"></a><span data-ttu-id="31394-103">Функция SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="31394-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="31394-104">Заменяет часть текстовой строки другой строкой текста.</span><span class="sxs-lookup"><span data-stu-id="31394-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="31394-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31394-105">Syntax</span></span>

 <span data-ttu-id="31394-106">ЗАМЕНА (** *текст* **, ** *стар_текст* **, ** *нов_текст* ** [, ** *Начальная позиция* **] [, ** *ignore_case_opt* **)</span><span class="sxs-lookup"><span data-stu-id="31394-106">SUBSTITUTE (** *text* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* ** ][, ** *ignore_case_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="31394-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31394-107">Parameters</span></span>

|<span data-ttu-id="31394-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="31394-108">**Name**</span></span>|<span data-ttu-id="31394-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="31394-109">**Required/Optional**</span></span>|<span data-ttu-id="31394-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="31394-110">**Data Type**</span></span>|<span data-ttu-id="31394-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31394-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="31394-112">_text_</span><span class="sxs-lookup"><span data-stu-id="31394-112">_text_</span></span> <br/> |<span data-ttu-id="31394-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31394-113">Required</span></span>  <br/> |<span data-ttu-id="31394-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="31394-114">**String**</span></span> <br/> | <span data-ttu-id="31394-115">Текст или ссылка на ячейку, содержащую текст, для которого требуется замена знаков.</span><span class="sxs-lookup"><span data-stu-id="31394-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="31394-116">_стар_текст_</span><span class="sxs-lookup"><span data-stu-id="31394-116">_old_text_</span></span> <br/> |<span data-ttu-id="31394-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31394-117">Required</span></span>  <br/> |<span data-ttu-id="31394-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="31394-118">**String**</span></span> <br/> | <span data-ttu-id="31394-119">Текст, который вы хотите заменить.</span><span class="sxs-lookup"><span data-stu-id="31394-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="31394-120">_нов_текст_</span><span class="sxs-lookup"><span data-stu-id="31394-120">_new_text_</span></span> <br/> |<span data-ttu-id="31394-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31394-121">Required</span></span>  <br/> |<span data-ttu-id="31394-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="31394-122">**String**</span></span> <br/> | <span data-ttu-id="31394-123">Текст, который будет использоваться для замены _стар_текст_.</span><span class="sxs-lookup"><span data-stu-id="31394-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="31394-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="31394-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="31394-125">Optional</span><span class="sxs-lookup"><span data-stu-id="31394-125">Optional</span></span>  <br/> |<span data-ttu-id="31394-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="31394-126">**Numeric**</span></span> <br/> |<span data-ttu-id="31394-127">Указывает, какие случаями стар_текст для замены.</span><span class="sxs-lookup"><span data-stu-id="31394-127">Specifies which occurences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="31394-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="31394-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="31394-129">Optional</span><span class="sxs-lookup"><span data-stu-id="31394-129">Optional</span></span>  <br/> |<span data-ttu-id="31394-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="31394-130">**Boolean**</span></span> <br/> |<span data-ttu-id="31394-131">FALSE, если с учетом регистра; в противном случае — значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="31394-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="31394-132">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="31394-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="31394-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3">Return value</span></span>

<span data-ttu-id="31394-134">Строка</span><span class="sxs-lookup"><span data-stu-id="31394-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31394-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="31394-135">Remarks</span></span>

 <span data-ttu-id="31394-136">При указании _start_num_opt_заменяется только это вхождение _стар_текст_ .</span><span class="sxs-lookup"><span data-stu-id="31394-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="31394-137">В противном случае каждого вхождения _стар_текст_ в _тексте_ изменяется на _нов_текст._</span><span class="sxs-lookup"><span data-stu-id="31394-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="31394-138">Используйте функцию ЗАМЕНЫ, когда необходимо заменить определенный текст в текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="31394-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="31394-139">Если вы хотите заменить текст, который встречается в определенное расположение в строку текста, используйте функцию REPLACE.</span><span class="sxs-lookup"><span data-stu-id="31394-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="31394-140">Пример</span><span class="sxs-lookup"><span data-stu-id="31394-140">Example</span></span>

<span data-ttu-id="31394-141">Заменить («1 января 2003», «Январь», «Янв»)</span><span class="sxs-lookup"><span data-stu-id="31394-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="31394-142">Возвращает «1 ЯНВАРЯ 2003».</span><span class="sxs-lookup"><span data-stu-id="31394-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="31394-143">Заменить («1 января 2003», «январь», «Янв»)</span><span class="sxs-lookup"><span data-stu-id="31394-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="31394-144">Возвращает «1 января 2003».</span><span class="sxs-lookup"><span data-stu-id="31394-144">Returns "1 January 2003".</span></span> <span data-ttu-id="31394-145">Не является изменений, так как поиск текста задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="31394-145">No change is made because the text search is case-sensitive.</span></span> 
  

