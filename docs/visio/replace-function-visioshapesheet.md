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
description: Заменяет часть текстовой строки на заданное число символов другой текстовой строкой.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320162"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="6d6eb-103">REPLACE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6d6eb-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6d6eb-104">Заменяет часть текстовой строки на заданное число символов другой текстовой строкой.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6d6eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d6eb-105">Syntax</span></span>

<span data-ttu-id="6d6eb-106">RePLACE (\* \* *стар_текст* \* \*, \* \* *Нач_позиция* \* \*, \* \* *Количество_знаков* \* \*, \* \* *новый_текст* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6d6eb-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d6eb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d6eb-107">Parameters</span></span>

|<span data-ttu-id="6d6eb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-108">**Name**</span></span>|<span data-ttu-id="6d6eb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-109">**Required/Optional**</span></span>|<span data-ttu-id="6d6eb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-110">**Data Type**</span></span>|<span data-ttu-id="6d6eb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d6eb-112">_стар_текст_</span><span class="sxs-lookup"><span data-stu-id="6d6eb-112">_old_text_</span></span> <br/> |<span data-ttu-id="6d6eb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d6eb-113">Required</span></span>  <br/> |<span data-ttu-id="6d6eb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-114">**String**</span></span> <br/> |<span data-ttu-id="6d6eb-115">Текст, в котором нужно заменить некоторые символы.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="6d6eb-116">_равн_</span><span class="sxs-lookup"><span data-stu-id="6d6eb-116">_start_num_</span></span> <br/> |<span data-ttu-id="6d6eb-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d6eb-117">Required</span></span>  <br/> |<span data-ttu-id="6d6eb-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-118">**Number**</span></span> <br/> |<span data-ttu-id="6d6eb-119">Позиция знака в _тексте старый_текст_ , которую нужно заменить на _новый_текст_.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="6d6eb-120">Первый символ в строке равен позиции 1.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="6d6eb-121">_Количество_знаков_</span><span class="sxs-lookup"><span data-stu-id="6d6eb-121">_num_chars_</span></span> <br/> |<span data-ttu-id="6d6eb-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d6eb-122">Required</span></span>  <br/> |<span data-ttu-id="6d6eb-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-123">**Number**</span></span> <br/> |<span data-ttu-id="6d6eb-124">Число знаков в тексте _старый_текст_ , которые необходимо заменить</span><span class="sxs-lookup"><span data-stu-id="6d6eb-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="6d6eb-125">_новый_текст_</span><span class="sxs-lookup"><span data-stu-id="6d6eb-125">_new_text_</span></span> <br/> |<span data-ttu-id="6d6eb-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6d6eb-126">Required</span></span>  <br/> |<span data-ttu-id="6d6eb-127">**String**</span><span class="sxs-lookup"><span data-stu-id="6d6eb-127">**String**</span></span> <br/> |<span data-ttu-id="6d6eb-128">Текст, который заменит символы в _тексте старый_текст_.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6d6eb-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d6eb-129">Return value</span></span>

<span data-ttu-id="6d6eb-130">Строка</span><span class="sxs-lookup"><span data-stu-id="6d6eb-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d6eb-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d6eb-131">Remarks</span></span>

<span data-ttu-id="6d6eb-132">Используйте функцию rePLACE, чтобы заменить текст, который находится в определенном месте в текстовой строке.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-132">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string.</span></span> <span data-ttu-id="6d6eb-133">Если вы хотите заменить определенный текст в текстовой строке, используйте функцию подСТАНОВКи.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-133">If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="6d6eb-134">Пример</span><span class="sxs-lookup"><span data-stu-id="6d6eb-134">Example</span></span>

<span data-ttu-id="6d6eb-135">REPLACE ("01/03/2002", 9, 2, "03")</span><span class="sxs-lookup"><span data-stu-id="6d6eb-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="6d6eb-136">Возвращает 01/03/2003.</span><span class="sxs-lookup"><span data-stu-id="6d6eb-136">Returns 01/03/2003.</span></span> 
  

