---
title: ЗАМЕНИТЕ функцию (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Заменяет часть строки текста, на основе числа символов, с другой строкой текста.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814569"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="0b07d-103">ЗАМЕНИТЕ функцию (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0b07d-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0b07d-104">Заменяет часть строки текста, на основе числа символов, с другой строкой текста.</span><span class="sxs-lookup"><span data-stu-id="0b07d-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0b07d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b07d-105">Syntax</span></span>

<span data-ttu-id="0b07d-106">ЗАМЕНИТЕ (** *стар_текст* **, ** *Начальная позиция* **, ** *число_знаков* **, ** *нов_текст* **)</span><span class="sxs-lookup"><span data-stu-id="0b07d-106">REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0b07d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b07d-107">Parameters</span></span>

|<span data-ttu-id="0b07d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0b07d-108">**Name**</span></span>|<span data-ttu-id="0b07d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="0b07d-109">**Required/Optional**</span></span>|<span data-ttu-id="0b07d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0b07d-110">**Data Type**</span></span>|<span data-ttu-id="0b07d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0b07d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0b07d-112">_стар_текст_</span><span class="sxs-lookup"><span data-stu-id="0b07d-112">_old_text_</span></span> <br/> |<span data-ttu-id="0b07d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b07d-113">Required</span></span>  <br/> |<span data-ttu-id="0b07d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0b07d-114">**String**</span></span> <br/> |<span data-ttu-id="0b07d-115">Текст, в котором вы хотите заменить некоторые знаки.</span><span class="sxs-lookup"><span data-stu-id="0b07d-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="0b07d-116">_Начальная позиция_</span><span class="sxs-lookup"><span data-stu-id="0b07d-116">_start_num_</span></span> <br/> |<span data-ttu-id="0b07d-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b07d-117">Required</span></span>  <br/> |<span data-ttu-id="0b07d-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="0b07d-118">**Number**</span></span> <br/> |<span data-ttu-id="0b07d-119">Позиция символа в _стар_текст_ , который вы хотите заменить на _нов_текст_.</span><span class="sxs-lookup"><span data-stu-id="0b07d-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="0b07d-120">Первый символ в строке является позиции 1.</span><span class="sxs-lookup"><span data-stu-id="0b07d-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="0b07d-121">_Количество_знаков_</span><span class="sxs-lookup"><span data-stu-id="0b07d-121">_num_chars_</span></span> <br/> |<span data-ttu-id="0b07d-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b07d-122">Required</span></span>  <br/> |<span data-ttu-id="0b07d-123">**Число**</span><span class="sxs-lookup"><span data-stu-id="0b07d-123">**Number**</span></span> <br/> |<span data-ttu-id="0b07d-124">Число знаков в _тексте старый_текст_ , который вы хотите заменить</span><span class="sxs-lookup"><span data-stu-id="0b07d-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="0b07d-125">_нов_текст_</span><span class="sxs-lookup"><span data-stu-id="0b07d-125">_new_text_</span></span> <br/> |<span data-ttu-id="0b07d-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0b07d-126">Required</span></span>  <br/> |<span data-ttu-id="0b07d-127">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0b07d-127">**String**</span></span> <br/> |<span data-ttu-id="0b07d-128">Текст, который заменяет знаки в _тексте старый_текст_.</span><span class="sxs-lookup"><span data-stu-id="0b07d-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0b07d-129">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0b07d-129">Return value</span></span>

<span data-ttu-id="0b07d-130">Строка</span><span class="sxs-lookup"><span data-stu-id="0b07d-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b07d-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="0b07d-131">Remarks</span></span>

<span data-ttu-id="0b07d-132">Функция REPLACE для замены текста, что происходит в определенное расположение в текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="0b07d-132">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string.</span></span> <span data-ttu-id="0b07d-133">Если вы хотите заменить определенный текст в текстовой строке, используйте функцию ЗАМЕНЫ.</span><span class="sxs-lookup"><span data-stu-id="0b07d-133">If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="0b07d-134">Пример</span><span class="sxs-lookup"><span data-stu-id="0b07d-134">Example</span></span>

<span data-ttu-id="0b07d-135">ЗАМЕНИТЕ («01/03/2002», 9,2, «03»)</span><span class="sxs-lookup"><span data-stu-id="0b07d-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="0b07d-136">Возвращает 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="0b07d-136">Returns 01/03/2003.</span></span> 
  

