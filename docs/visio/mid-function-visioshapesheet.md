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
description: Возвращает определенное число символов из строки текста, начиная с указанной позиции, основанный на число знаков, которое можно указать.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814280"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="21008-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="21008-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="21008-104">Возвращает определенное число символов из строки текста, начиная с указанной позиции, основанный на число знаков, которое можно указать.</span><span class="sxs-lookup"><span data-stu-id="21008-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21008-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21008-105">Syntax</span></span>

<span data-ttu-id="21008-106">MID (** *текст* **, ** *Начальная позиция* **, ** *число_знаков* **)</span><span class="sxs-lookup"><span data-stu-id="21008-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21008-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="21008-107">Parameters</span></span>

|<span data-ttu-id="21008-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="21008-108">**Name**</span></span>|<span data-ttu-id="21008-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="21008-109">**Required/Optional**</span></span>|<span data-ttu-id="21008-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="21008-110">**Data Type**</span></span>|<span data-ttu-id="21008-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21008-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21008-112">_text_</span><span class="sxs-lookup"><span data-stu-id="21008-112">_text_</span></span> <br/> |<span data-ttu-id="21008-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="21008-113">Required</span></span>  <br/> |<span data-ttu-id="21008-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="21008-114">**String**</span></span> <br/> |<span data-ttu-id="21008-115">Текстовая строка, содержащая знаки, которые вы хотите извлечь.</span><span class="sxs-lookup"><span data-stu-id="21008-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="21008-116">_Начальная позиция_</span><span class="sxs-lookup"><span data-stu-id="21008-116">_start_num_</span></span> <br/> |<span data-ttu-id="21008-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="21008-117">Required</span></span>  <br/> |<span data-ttu-id="21008-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="21008-118">**Number**</span></span> <br/> |<span data-ttu-id="21008-119">Положение первого знака, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="21008-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="21008-120">Первым символом в текстовой строки — позиции 1.</span><span class="sxs-lookup"><span data-stu-id="21008-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="21008-121">_Количество_знаков_</span><span class="sxs-lookup"><span data-stu-id="21008-121">_num_chars_</span></span> <br/> |<span data-ttu-id="21008-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="21008-122">Required</span></span>  <br/> |<span data-ttu-id="21008-123">**Число**</span><span class="sxs-lookup"><span data-stu-id="21008-123">**Number**</span></span> <br/> |<span data-ttu-id="21008-124">Число возвращаемых знаков.</span><span class="sxs-lookup"><span data-stu-id="21008-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="21008-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="21008-126">Строка</span><span class="sxs-lookup"><span data-stu-id="21008-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21008-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="21008-127">Remarks</span></span>

<span data-ttu-id="21008-128">Если *Начальная позиция* :</span><span class="sxs-lookup"><span data-stu-id="21008-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="21008-129">Больше, чем длина *текста* , MID возвращает «» (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="21008-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="21008-130">Меньше, чем длина *текста* , но *Начальная_позиция* плюс *Количество_знаков* превышает длину *текста* , MID возвращает символы до конца *текста* .</span><span class="sxs-lookup"><span data-stu-id="21008-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="21008-131">Меньше 1 MID возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="21008-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="21008-132">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="21008-132">error value.</span></span> 
    
<span data-ttu-id="21008-133">Если *число_знаков* отрицательно, MID возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="21008-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="21008-134">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="21008-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="21008-135">Пример</span><span class="sxs-lookup"><span data-stu-id="21008-135">Example</span></span>

<span data-ttu-id="21008-136">MID («SSN 999-99-9999», 5, 11)</span><span class="sxs-lookup"><span data-stu-id="21008-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="21008-137">Возвращает 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="21008-137">Returns 999-99-9999.</span></span> 
  

