---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Заменяет часть текстовой строки, основанную на количестве символов, на другую текстовую строку.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414356"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="b9515-103">REPLACE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b9515-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b9515-104">Заменяет часть текстовой строки, основанную на количестве символов, на другую текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="b9515-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b9515-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9515-105">Syntax</span></span>

<span data-ttu-id="b9515-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b9515-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b9515-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9515-107">Parameters</span></span>

|<span data-ttu-id="b9515-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b9515-108">**Name**</span></span>|<span data-ttu-id="b9515-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b9515-109">**Required/Optional**</span></span>|<span data-ttu-id="b9515-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b9515-110">**Data Type**</span></span>|<span data-ttu-id="b9515-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9515-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b9515-112">_old_text_</span><span class="sxs-lookup"><span data-stu-id="b9515-112">_old_text_</span></span> <br/> |<span data-ttu-id="b9515-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="b9515-113">Required</span></span>  <br/> |<span data-ttu-id="b9515-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="b9515-114">**String**</span></span> <br/> |<span data-ttu-id="b9515-115">Текст, в котором необходимо заменить некоторые символы.</span><span class="sxs-lookup"><span data-stu-id="b9515-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="b9515-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="b9515-116">_start_num_</span></span> <br/> |<span data-ttu-id="b9515-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="b9515-117">Required</span></span>  <br/> |<span data-ttu-id="b9515-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="b9515-118">**Number**</span></span> <br/> |<span data-ttu-id="b9515-119">Положение символа в  _old_text,_ который необходимо заменить  _на_ new_text .</span><span class="sxs-lookup"><span data-stu-id="b9515-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="b9515-120">Первый символ в строке — позиция 1.</span><span class="sxs-lookup"><span data-stu-id="b9515-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="b9515-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="b9515-121">_num_chars_</span></span> <br/> |<span data-ttu-id="b9515-122">Обязательна</span><span class="sxs-lookup"><span data-stu-id="b9515-122">Required</span></span>  <br/> |<span data-ttu-id="b9515-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="b9515-123">**Number**</span></span> <br/> |<span data-ttu-id="b9515-124">Количество символов в  _old_text,_ которые необходимо заменить</span><span class="sxs-lookup"><span data-stu-id="b9515-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="b9515-125">_new_text_</span><span class="sxs-lookup"><span data-stu-id="b9515-125">_new_text_</span></span> <br/> |<span data-ttu-id="b9515-126">Обязательно</span><span class="sxs-lookup"><span data-stu-id="b9515-126">Required</span></span>  <br/> |<span data-ttu-id="b9515-127">**Строка**</span><span class="sxs-lookup"><span data-stu-id="b9515-127">**String**</span></span> <br/> |<span data-ttu-id="b9515-128">Текст, который будет заменять символы в _old_text._</span><span class="sxs-lookup"><span data-stu-id="b9515-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b9515-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9515-129">Return value</span></span>

<span data-ttu-id="b9515-130">String</span><span class="sxs-lookup"><span data-stu-id="b9515-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9515-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9515-131">Remarks</span></span>

<span data-ttu-id="b9515-132">Используйте функцию REPLACE, чтобы заменить текст, который происходит в определенном расположении в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="b9515-132">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string.</span></span> <span data-ttu-id="b9515-133">Если вы хотите заменить определенный текст в текстовой строке, используйте функцию SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="b9515-133">If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="b9515-134">Пример</span><span class="sxs-lookup"><span data-stu-id="b9515-134">Example</span></span>

<span data-ttu-id="b9515-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="b9515-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="b9515-136">Возвращает 03.01.2003.</span><span class="sxs-lookup"><span data-stu-id="b9515-136">Returns 01/03/2003.</span></span> 
  

