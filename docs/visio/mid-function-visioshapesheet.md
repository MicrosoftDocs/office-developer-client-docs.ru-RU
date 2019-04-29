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
description: Возвращает определенное количество символов из текстовой строки, начиная с указанной позиции, в соответствии с указанным количеством символов.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410268"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="daaec-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="daaec-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="daaec-104">Возвращает определенное количество символов из текстовой строки, начиная с указанной позиции, в соответствии с указанным количеством символов.</span><span class="sxs-lookup"><span data-stu-id="daaec-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="daaec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daaec-105">Syntax</span></span>

<span data-ttu-id="daaec-106">MID (\* \* *Text* \* \*, \* \* *Нач_позиция* \* \*, \* \* *Количество_знаков* \* \*)</span><span class="sxs-lookup"><span data-stu-id="daaec-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="daaec-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="daaec-107">Parameters</span></span>

|<span data-ttu-id="daaec-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="daaec-108">**Name**</span></span>|<span data-ttu-id="daaec-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="daaec-109">**Required/Optional**</span></span>|<span data-ttu-id="daaec-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="daaec-110">**Data Type**</span></span>|<span data-ttu-id="daaec-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="daaec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="daaec-112">_text_</span><span class="sxs-lookup"><span data-stu-id="daaec-112">_text_</span></span> <br/> |<span data-ttu-id="daaec-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daaec-113">Required</span></span>  <br/> |<span data-ttu-id="daaec-114">**String**</span><span class="sxs-lookup"><span data-stu-id="daaec-114">**String**</span></span> <br/> |<span data-ttu-id="daaec-115">Текстовая строка, содержащая символы, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="daaec-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="daaec-116">_равн_</span><span class="sxs-lookup"><span data-stu-id="daaec-116">_start_num_</span></span> <br/> |<span data-ttu-id="daaec-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daaec-117">Required</span></span>  <br/> |<span data-ttu-id="daaec-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="daaec-118">**Number**</span></span> <br/> |<span data-ttu-id="daaec-119">Позиция первого символа, который необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="daaec-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="daaec-120">Первый символ в текстовой строке равен позиции 1.</span><span class="sxs-lookup"><span data-stu-id="daaec-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="daaec-121">_Количество_знаков_</span><span class="sxs-lookup"><span data-stu-id="daaec-121">_num_chars_</span></span> <br/> |<span data-ttu-id="daaec-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="daaec-122">Required</span></span>  <br/> |<span data-ttu-id="daaec-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="daaec-123">**Number**</span></span> <br/> |<span data-ttu-id="daaec-124">Число возвращаемых символов.</span><span class="sxs-lookup"><span data-stu-id="daaec-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="daaec-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="daaec-125">Return value</span></span>

<span data-ttu-id="daaec-126">String</span><span class="sxs-lookup"><span data-stu-id="daaec-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="daaec-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="daaec-127">Remarks</span></span>

<span data-ttu-id="daaec-128">Если *Нач_позиция* :</span><span class="sxs-lookup"><span data-stu-id="daaec-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="daaec-129">Больше, чем длина *текста* , то функция ПСТР возвращает значение "" (пустой текст).</span><span class="sxs-lookup"><span data-stu-id="daaec-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="daaec-130">Меньше, чем длина *текста* , а *Нач_позиция* плюс *Количество_знаков* превышают длину *текста* , то функция ПСТР возвращает символы до конца *текста* .</span><span class="sxs-lookup"><span data-stu-id="daaec-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="daaec-131">Если значение меньше 1, то функция ПСТР возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="daaec-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="daaec-132">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="daaec-132">error value.</span></span> 
    
<span data-ttu-id="daaec-133">Если *число_знаков* отрицательно, то функция пстр возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="daaec-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="daaec-134">значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="daaec-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="daaec-135">Пример</span><span class="sxs-lookup"><span data-stu-id="daaec-135">Example</span></span>

<span data-ttu-id="daaec-136">MID ("SSN 999-99-9999", 5, 11)</span><span class="sxs-lookup"><span data-stu-id="daaec-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="daaec-137">Возвращает 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="daaec-137">Returns 999-99-9999.</span></span> 
  

