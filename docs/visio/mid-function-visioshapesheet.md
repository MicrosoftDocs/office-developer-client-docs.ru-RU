---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Возвращает определенное количество символов из текстовой строки, начиная с за определяемой позиции, в зависимости от количества символов, которые вы указываете.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410268"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="df75f-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="df75f-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="df75f-104">Возвращает определенное количество символов из текстовой строки, начиная с за определяемой позиции, в зависимости от количества символов, которые вы указываете.</span><span class="sxs-lookup"><span data-stu-id="df75f-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="df75f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df75f-105">Syntax</span></span>

<span data-ttu-id="df75f-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span><span class="sxs-lookup"><span data-stu-id="df75f-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df75f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="df75f-107">Parameters</span></span>

|<span data-ttu-id="df75f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="df75f-108">**Name**</span></span>|<span data-ttu-id="df75f-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="df75f-109">**Required/Optional**</span></span>|<span data-ttu-id="df75f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="df75f-110">**Data Type**</span></span>|<span data-ttu-id="df75f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df75f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df75f-112">_text_</span><span class="sxs-lookup"><span data-stu-id="df75f-112">_text_</span></span> <br/> |<span data-ttu-id="df75f-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="df75f-113">Required</span></span>  <br/> |<span data-ttu-id="df75f-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="df75f-114">**String**</span></span> <br/> |<span data-ttu-id="df75f-115">Текстовая строка, содержаная символы, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="df75f-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="df75f-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="df75f-116">_start_num_</span></span> <br/> |<span data-ttu-id="df75f-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="df75f-117">Required</span></span>  <br/> |<span data-ttu-id="df75f-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="df75f-118">**Number**</span></span> <br/> |<span data-ttu-id="df75f-119">Положение первого символа, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="df75f-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="df75f-120">Первый символ в текстовой строке — позиция 1.</span><span class="sxs-lookup"><span data-stu-id="df75f-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="df75f-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="df75f-121">_num_chars_</span></span> <br/> |<span data-ttu-id="df75f-122">Обязательна</span><span class="sxs-lookup"><span data-stu-id="df75f-122">Required</span></span>  <br/> |<span data-ttu-id="df75f-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="df75f-123">**Number**</span></span> <br/> |<span data-ttu-id="df75f-124">Количество возвращаемого символа.</span><span class="sxs-lookup"><span data-stu-id="df75f-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df75f-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df75f-125">Return value</span></span>

<span data-ttu-id="df75f-126">String</span><span class="sxs-lookup"><span data-stu-id="df75f-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df75f-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="df75f-127">Remarks</span></span>

<span data-ttu-id="df75f-128">Если *start_num:*</span><span class="sxs-lookup"><span data-stu-id="df75f-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="df75f-129">Больше длины текста,  MID возвращает "" (пустой текст).</span><span class="sxs-lookup"><span data-stu-id="df75f-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="df75f-130">Меньше длины *текста,* но  start_num плюс *num_chars* превышает длину *текста,* MID возвращает символы до конца *текста.*</span><span class="sxs-lookup"><span data-stu-id="df75f-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="df75f-131">Менее 1 mid возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df75f-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="df75f-132">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="df75f-132">error value.</span></span> 
    
<span data-ttu-id="df75f-133">Если  *num_chars*  отрицательный, MID возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df75f-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="df75f-134">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="df75f-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="df75f-135">Пример</span><span class="sxs-lookup"><span data-stu-id="df75f-135">Example</span></span>

<span data-ttu-id="df75f-136">MID (SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="df75f-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="df75f-137">Возвращает 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="df75f-137">Returns 999-99-9999.</span></span> 
  

