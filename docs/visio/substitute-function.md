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
# <a name="substitute-function"></a><span data-ttu-id="993e9-103">Функция SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="993e9-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="993e9-104">Заменяет часть текстовой строки другой текстовой строкой.</span><span class="sxs-lookup"><span data-stu-id="993e9-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="993e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="993e9-105">Syntax</span></span>

 <span data-ttu-id="993e9-106">Замена (\* \* *текстовый* \* \*, \* \* *стар_текст* \* \*, \* \* *новый_текст* \* \* [, \* \* *Нач_позиция* \* \*] [, \* \* *игноре_касе_опт* \* \*)</span><span class="sxs-lookup"><span data-stu-id="993e9-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="993e9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="993e9-107">Parameters</span></span>

|<span data-ttu-id="993e9-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="993e9-108">**Name**</span></span>|<span data-ttu-id="993e9-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="993e9-109">**Required/Optional**</span></span>|<span data-ttu-id="993e9-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="993e9-110">**Data Type**</span></span>|<span data-ttu-id="993e9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="993e9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="993e9-112">_text_</span><span class="sxs-lookup"><span data-stu-id="993e9-112">_text_</span></span> <br/> |<span data-ttu-id="993e9-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="993e9-113">Required</span></span>  <br/> |<span data-ttu-id="993e9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="993e9-114">**String**</span></span> <br/> | <span data-ttu-id="993e9-115">Текст или ссылка на ячейку, содержащую текст, для которого нужно заменять символы.</span><span class="sxs-lookup"><span data-stu-id="993e9-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="993e9-116">_стар_текст_</span><span class="sxs-lookup"><span data-stu-id="993e9-116">_old_text_</span></span> <br/> |<span data-ttu-id="993e9-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="993e9-117">Required</span></span>  <br/> |<span data-ttu-id="993e9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="993e9-118">**String**</span></span> <br/> | <span data-ttu-id="993e9-119">Текст, который необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="993e9-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="993e9-120">_новый_текст_</span><span class="sxs-lookup"><span data-stu-id="993e9-120">_new_text_</span></span> <br/> |<span data-ttu-id="993e9-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="993e9-121">Required</span></span>  <br/> |<span data-ttu-id="993e9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="993e9-122">**String**</span></span> <br/> | <span data-ttu-id="993e9-123">Текст, который будет использоваться для замены _стар_текст_.</span><span class="sxs-lookup"><span data-stu-id="993e9-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="993e9-124">_старт_нум_опт_</span><span class="sxs-lookup"><span data-stu-id="993e9-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="993e9-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="993e9-125">Optional</span></span>  <br/> |<span data-ttu-id="993e9-126">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="993e9-126">**Numeric**</span></span> <br/> |<span data-ttu-id="993e9-127">Указывает, какие экземпляры стар_текст заменяют.</span><span class="sxs-lookup"><span data-stu-id="993e9-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="993e9-128">_игноре_касе_опт_</span><span class="sxs-lookup"><span data-stu-id="993e9-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="993e9-129">Необязательно</span><span class="sxs-lookup"><span data-stu-id="993e9-129">Optional</span></span>  <br/> |<span data-ttu-id="993e9-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="993e9-130">**Boolean**</span></span> <br/> |<span data-ttu-id="993e9-131">ЗНАЧЕНИЕ FALSE в случае учета регистра; в противном случае — значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="993e9-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="993e9-132">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="993e9-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="993e9-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="993e9-133">Return value</span></span>

<span data-ttu-id="993e9-134">Строка</span><span class="sxs-lookup"><span data-stu-id="993e9-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="993e9-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="993e9-135">Remarks</span></span>

 <span data-ttu-id="993e9-136">Если вы укажете _старт_нум_опт_, заменяется только это вхождение _стар_текст_ .</span><span class="sxs-lookup"><span data-stu-id="993e9-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="993e9-137">В противном случае каждое вхождение _стар_текст_ в _тексте_ изменится на _новый_текст._</span><span class="sxs-lookup"><span data-stu-id="993e9-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="993e9-138">Используйте функцию подСТАНОВКи, если хотите заменить определенный текст в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="993e9-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="993e9-139">Если вы хотите заменить текст, который находится в определенном месте в текстовой строке, используйте функцию rePLACE.</span><span class="sxs-lookup"><span data-stu-id="993e9-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="993e9-140">Пример</span><span class="sxs-lookup"><span data-stu-id="993e9-140">Example</span></span>

<span data-ttu-id="993e9-141">Замена ("1 января января", "Январь", "Янв")</span><span class="sxs-lookup"><span data-stu-id="993e9-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="993e9-142">Возвращает значение "1 января 2003".</span><span class="sxs-lookup"><span data-stu-id="993e9-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="993e9-143">Замена ("1 января 2003 г.", "Январь", "Янв")</span><span class="sxs-lookup"><span data-stu-id="993e9-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="993e9-144">Возвращает значение "1 января 2003".</span><span class="sxs-lookup"><span data-stu-id="993e9-144">Returns "1 January 2003".</span></span> <span data-ttu-id="993e9-145">Изменения не выполняются, так как при поиске текста учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="993e9-145">No change is made because the text search is case-sensitive.</span></span> 
  

