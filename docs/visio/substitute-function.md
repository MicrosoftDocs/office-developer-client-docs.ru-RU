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
description: Заменяет часть текстовой строки другой текстовой строкой.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346825"
---
# <a name="substitute-function"></a><span data-ttu-id="484b5-103">Функция SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="484b5-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="484b5-104">Заменяет часть текстовой строки другой текстовой строкой.</span><span class="sxs-lookup"><span data-stu-id="484b5-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="484b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="484b5-105">Syntax</span></span>

 <span data-ttu-id="484b5-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="484b5-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="484b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="484b5-107">Parameters</span></span>

|<span data-ttu-id="484b5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="484b5-108">**Name**</span></span>|<span data-ttu-id="484b5-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="484b5-109">**Required/Optional**</span></span>|<span data-ttu-id="484b5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="484b5-110">**Data Type**</span></span>|<span data-ttu-id="484b5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="484b5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="484b5-112">_text_</span><span class="sxs-lookup"><span data-stu-id="484b5-112">_text_</span></span> <br/> |<span data-ttu-id="484b5-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="484b5-113">Required</span></span>  <br/> |<span data-ttu-id="484b5-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="484b5-114">**String**</span></span> <br/> | <span data-ttu-id="484b5-115">Текст или ссылка на ячейку, содержащую текст, для которого нужно заменить символы.</span><span class="sxs-lookup"><span data-stu-id="484b5-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="484b5-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="484b5-116">_old_text_</span></span> <br/> |<span data-ttu-id="484b5-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="484b5-117">Required</span></span>  <br/> |<span data-ttu-id="484b5-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="484b5-118">**String**</span></span> <br/> | <span data-ttu-id="484b5-119">Текст, который необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="484b5-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="484b5-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="484b5-120">_new_text_</span></span> <br/> |<span data-ttu-id="484b5-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="484b5-121">Required</span></span>  <br/> |<span data-ttu-id="484b5-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="484b5-122">**String**</span></span> <br/> | <span data-ttu-id="484b5-123">Текст, который вы хотите использовать для  _замены_ old_text.</span><span class="sxs-lookup"><span data-stu-id="484b5-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="484b5-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="484b5-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="484b5-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="484b5-125">Optional</span></span>  <br/> |<span data-ttu-id="484b5-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="484b5-126">**Numeric**</span></span> <br/> |<span data-ttu-id="484b5-127">Указывает, какие вхождения old_text заменяются.</span><span class="sxs-lookup"><span data-stu-id="484b5-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="484b5-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="484b5-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="484b5-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="484b5-129">Optional</span></span>  <br/> |<span data-ttu-id="484b5-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="484b5-130">**Boolean**</span></span> <br/> |<span data-ttu-id="484b5-131">FALSE, если чувствительный к делу; в противном случае true.</span><span class="sxs-lookup"><span data-stu-id="484b5-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="484b5-132">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="484b5-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="484b5-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="484b5-133">Return value</span></span>

<span data-ttu-id="484b5-134">String</span><span class="sxs-lookup"><span data-stu-id="484b5-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="484b5-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="484b5-135">Remarks</span></span>

 <span data-ttu-id="484b5-136">Если указать _start_num_opt,_ заменяется только _old_text._</span><span class="sxs-lookup"><span data-stu-id="484b5-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="484b5-137">В противном случае каждое  _old_text_  _в тексте меняется_ на  _new_text._</span><span class="sxs-lookup"><span data-stu-id="484b5-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="484b5-138">Используйте функцию SUBSTITUTE, чтобы заменить определенный текст в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="484b5-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="484b5-139">Если вы хотите заменить текст, который находится в определенном расположении в текстовой строке, используйте функцию REPLACE.</span><span class="sxs-lookup"><span data-stu-id="484b5-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="484b5-140">Пример</span><span class="sxs-lookup"><span data-stu-id="484b5-140">Example</span></span>

<span data-ttu-id="484b5-141">SUBSTITUTE ("1 января 2003 г.", "Январь", "JAN")</span><span class="sxs-lookup"><span data-stu-id="484b5-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="484b5-142">Возвращает "1 ЯНВАРь 2003 г.".</span><span class="sxs-lookup"><span data-stu-id="484b5-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="484b5-143">SUBSTITUTE ("1 января 2003 г.","january","JAN")</span><span class="sxs-lookup"><span data-stu-id="484b5-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="484b5-144">Возвращает "1 января 2003 г.".</span><span class="sxs-lookup"><span data-stu-id="484b5-144">Returns "1 January 2003".</span></span> <span data-ttu-id="484b5-145">Никакие изменения не вносяся, так как в поиске текста с чувствительностью к делу.</span><span class="sxs-lookup"><span data-stu-id="484b5-145">No change is made because the text search is case-sensitive.</span></span> 
  

