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
description: Заменяет часть текстовой строки в зависимости от количества символов, которые вы указываете, другой строкой текста.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414356"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="43969-103">REPLACE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="43969-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="43969-104">Заменяет часть текстовой строки в зависимости от количества символов, которые вы указываете, другой строкой текста.</span><span class="sxs-lookup"><span data-stu-id="43969-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="43969-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43969-105">Syntax</span></span>

<span data-ttu-id="43969-106">REPLACE (\*\* *old_text* \*\*, \*\*\*\* start_num \*\*, \*\*\*\* num_chars \*\*, \*\* *new_text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="43969-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43969-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43969-107">Parameters</span></span>

|<span data-ttu-id="43969-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="43969-108">**Name**</span></span>|<span data-ttu-id="43969-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="43969-109">**Required/Optional**</span></span>|<span data-ttu-id="43969-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="43969-110">**Data Type**</span></span>|<span data-ttu-id="43969-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="43969-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43969-112">_old_text_</span><span class="sxs-lookup"><span data-stu-id="43969-112">_old_text_</span></span> <br/> |<span data-ttu-id="43969-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="43969-113">Required</span></span>  <br/> |<span data-ttu-id="43969-114">**String**</span><span class="sxs-lookup"><span data-stu-id="43969-114">**String**</span></span> <br/> |<span data-ttu-id="43969-115">Текст, в котором необходимо заменить некоторые символы.</span><span class="sxs-lookup"><span data-stu-id="43969-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="43969-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="43969-116">_start_num_</span></span> <br/> |<span data-ttu-id="43969-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="43969-117">Required</span></span>  <br/> |<span data-ttu-id="43969-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="43969-118">**Number**</span></span> <br/> |<span data-ttu-id="43969-119">Положение символа в  _old_text,_ которое необходимо заменить  _new_text_.</span><span class="sxs-lookup"><span data-stu-id="43969-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="43969-120">Первый символ строки — позиция 1.</span><span class="sxs-lookup"><span data-stu-id="43969-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="43969-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="43969-121">_num_chars_</span></span> <br/> |<span data-ttu-id="43969-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="43969-122">Required</span></span>  <br/> |<span data-ttu-id="43969-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="43969-123">**Number**</span></span> <br/> |<span data-ttu-id="43969-124">Количество символов в  _old_text,_ которые необходимо заменить</span><span class="sxs-lookup"><span data-stu-id="43969-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="43969-125">_new_text_</span><span class="sxs-lookup"><span data-stu-id="43969-125">_new_text_</span></span> <br/> |<span data-ttu-id="43969-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="43969-126">Required</span></span>  <br/> |<span data-ttu-id="43969-127">**String**</span><span class="sxs-lookup"><span data-stu-id="43969-127">**String**</span></span> <br/> |<span data-ttu-id="43969-128">Текст, который заменит символы  _в old_text_.</span><span class="sxs-lookup"><span data-stu-id="43969-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="43969-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43969-129">Return value</span></span>

<span data-ttu-id="43969-130">String</span><span class="sxs-lookup"><span data-stu-id="43969-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43969-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="43969-131">Remarks</span></span>

<span data-ttu-id="43969-132">Используйте функцию REPLACE, когда необходимо заменить текст, который происходит в определенном расположении в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="43969-132">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string.</span></span> <span data-ttu-id="43969-133">Если вы хотите заменить определенный текст в текстовой строке, используйте функцию SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="43969-133">If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="43969-134">Пример</span><span class="sxs-lookup"><span data-stu-id="43969-134">Example</span></span>

<span data-ttu-id="43969-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="43969-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="43969-136">Возвращает 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="43969-136">Returns 01/03/2003.</span></span> 
  

