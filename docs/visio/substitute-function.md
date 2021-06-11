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
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346825"
---
# <a name="substitute-function"></a><span data-ttu-id="bf2f4-103">Функция SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="bf2f4-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="bf2f4-104">Заменяет часть текстовой строки другой строкой текста.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bf2f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf2f4-105">Syntax</span></span>

 <span data-ttu-id="bf2f4-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \**, \*\*\*\* new_text \*\* [, \*\*\* start_num* \*\* ][, \*\* *ignore_case_opt* \*\* \* \* )</span><span class="sxs-lookup"><span data-stu-id="bf2f4-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bf2f4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf2f4-107">Parameters</span></span>

|<span data-ttu-id="bf2f4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-108">**Name**</span></span>|<span data-ttu-id="bf2f4-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-109">**Required/Optional**</span></span>|<span data-ttu-id="bf2f4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-110">**Data Type**</span></span>|<span data-ttu-id="bf2f4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bf2f4-112">_text_</span><span class="sxs-lookup"><span data-stu-id="bf2f4-112">_text_</span></span> <br/> |<span data-ttu-id="bf2f4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf2f4-113">Required</span></span>  <br/> |<span data-ttu-id="bf2f4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-114">**String**</span></span> <br/> | <span data-ttu-id="bf2f4-115">Текст или ссылка на ячейку, содержащую текст, для которого необходимо заменить символы.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="bf2f4-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="bf2f4-116">_old_text_</span></span> <br/> |<span data-ttu-id="bf2f4-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf2f4-117">Required</span></span>  <br/> |<span data-ttu-id="bf2f4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-118">**String**</span></span> <br/> | <span data-ttu-id="bf2f4-119">Текст, который необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="bf2f4-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="bf2f4-120">_new_text_</span></span> <br/> |<span data-ttu-id="bf2f4-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf2f4-121">Required</span></span>  <br/> |<span data-ttu-id="bf2f4-122">**String**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-122">**String**</span></span> <br/> | <span data-ttu-id="bf2f4-123">Текст, который необходимо использовать для замены _old_text._</span><span class="sxs-lookup"><span data-stu-id="bf2f4-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="bf2f4-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="bf2f4-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="bf2f4-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2f4-125">Optional</span></span>  <br/> |<span data-ttu-id="bf2f4-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-126">**Numeric**</span></span> <br/> |<span data-ttu-id="bf2f4-127">Указывает, какие случаи old_text заменить.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="bf2f4-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="bf2f4-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="bf2f4-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="bf2f4-129">Optional</span></span>  <br/> |<span data-ttu-id="bf2f4-130">**Логический**</span><span class="sxs-lookup"><span data-stu-id="bf2f4-130">**Boolean**</span></span> <br/> |<span data-ttu-id="bf2f4-131">FALSE, если он чувствителен к делу; в противном случае TRUE.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="bf2f4-132">По умолчанию значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bf2f4-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf2f4-133">Return value</span></span>

<span data-ttu-id="bf2f4-134">String</span><span class="sxs-lookup"><span data-stu-id="bf2f4-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf2f4-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf2f4-135">Remarks</span></span>

 <span data-ttu-id="bf2f4-136">Если указать _start_num_opt,_ заменяется только _old_text._</span><span class="sxs-lookup"><span data-stu-id="bf2f4-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="bf2f4-137">В противном случае каждое  _old_text_  _в тексте_ меняется на  _new_text._</span><span class="sxs-lookup"><span data-stu-id="bf2f4-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="bf2f4-138">Используйте функцию SUBSTITUTE, когда необходимо заменить определенный текст в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="bf2f4-139">Если вы хотите заменить текст, который происходит в определенном расположении в текстовой строке, используйте функцию REPLACE.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="bf2f4-140">Пример</span><span class="sxs-lookup"><span data-stu-id="bf2f4-140">Example</span></span>

<span data-ttu-id="bf2f4-141">SUBSTITUTE ("1 января 2003 г.", "Январь", "JAN")</span><span class="sxs-lookup"><span data-stu-id="bf2f4-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="bf2f4-142">Возвращает "1 JAN 2003".</span><span class="sxs-lookup"><span data-stu-id="bf2f4-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="bf2f4-143">SUBSTITUTE ("1 января 2003 г.", "январь", "JAN")</span><span class="sxs-lookup"><span data-stu-id="bf2f4-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="bf2f4-144">Возвращает "1 января 2003 года".</span><span class="sxs-lookup"><span data-stu-id="bf2f4-144">Returns "1 January 2003".</span></span> <span data-ttu-id="bf2f4-145">Изменения не вносясь, так как текстовый поиск является конфиденциальным к делу.</span><span class="sxs-lookup"><span data-stu-id="bf2f4-145">No change is made because the text search is case-sensitive.</span></span> 
  

