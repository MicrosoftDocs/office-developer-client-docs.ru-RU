---
title: Функция ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Возвращает значение TRUE, если значение ссылка_на_ячейку Ошибка типа #VALUE, где аргумент в формуле имеет неверный тип. Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814000"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="2b518-104">Функция ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="2b518-104">ISERRVALUE Function</span></span>

<span data-ttu-id="2b518-105">Возвращает значение TRUE, если значение _ссылка_на_ячейку_ Ошибка типа #VALUE, где аргумент в формуле имеет неверный тип.</span><span class="sxs-lookup"><span data-stu-id="2b518-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="2b518-106">Функция ISERRVALUE используется в логических выражениях, которые ссылаются на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="2b518-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2b518-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b518-107">Syntax</span></span>

<span data-ttu-id="2b518-108">ISERRVALUE (** *ссылка_на_ячейку* **)</span><span class="sxs-lookup"><span data-stu-id="2b518-108">ISERRVALUE(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2b518-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b518-109">Parameters</span></span>

|<span data-ttu-id="2b518-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2b518-110">**Name**</span></span>|<span data-ttu-id="2b518-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="2b518-111">**Required/Optional**</span></span>|<span data-ttu-id="2b518-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2b518-112">**Data Type**</span></span>|<span data-ttu-id="2b518-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b518-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2b518-114">_ссылка_на_ячейку_</span><span class="sxs-lookup"><span data-stu-id="2b518-114">_cellreference_</span></span> <br/> |<span data-ttu-id="2b518-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2b518-115">Required</span></span>  <br/> |<span data-ttu-id="2b518-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="2b518-116">**String**</span></span> <br/> |<span data-ttu-id="2b518-117">Ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="2b518-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b518-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b518-118">Remarks</span></span>

<span data-ttu-id="2b518-119">Вспомогательный ячейки, которые буквы от A до D не возвращают #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b518-119">Scratch cells A through D won't return a #VALUE!</span></span> <span data-ttu-id="2b518-120">Ошибка может содержать формулы и цифр в ту же строку.</span><span class="sxs-lookup"><span data-stu-id="2b518-120">error because the formula can contain numbers and letters in the same string.</span></span> <span data-ttu-id="2b518-121">Ячейки X и Y должно содержать только цифры.</span><span class="sxs-lookup"><span data-stu-id="2b518-121">Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2b518-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b518-122">Example 1</span></span>

|<span data-ttu-id="2b518-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2b518-123">**Cell**</span></span>|<span data-ttu-id="2b518-124">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="2b518-124">**Formula**</span></span>|<span data-ttu-id="2b518-125">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="2b518-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b518-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="2b518-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="2b518-127">= «Дом»</span><span class="sxs-lookup"><span data-stu-id="2b518-127">= "House"</span></span>  <br/> |<span data-ttu-id="2b518-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b518-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="2b518-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="2b518-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="2b518-130">= Если (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="2b518-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="2b518-131">2</span><span class="sxs-lookup"><span data-stu-id="2b518-131">2</span></span>  <br/> |
   
<span data-ttu-id="2b518-132">Возвращает 2, так как возвращаемое значение является #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b518-132">Returns 2 because the value returned is a #VALUE!</span></span> <span data-ttu-id="2b518-133">Ошибка и выражение указывает, что Microsoft Visio для возврата 2 вместо ошибки.</span><span class="sxs-lookup"><span data-stu-id="2b518-133">error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2b518-134">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b518-134">Example 2</span></span>

|<span data-ttu-id="2b518-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2b518-135">**Cell**</span></span>|<span data-ttu-id="2b518-136">**Формулы**</span><span class="sxs-lookup"><span data-stu-id="2b518-136">**Formula**</span></span>|<span data-ttu-id="2b518-137">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="2b518-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b518-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="2b518-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="2b518-139">= «5 + 7»</span><span class="sxs-lookup"><span data-stu-id="2b518-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="2b518-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="2b518-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="2b518-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="2b518-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="2b518-142">= Если (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="2b518-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="2b518-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="2b518-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="2b518-144">Возвращает 12 так как возвращаемое значение не является #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b518-144">Returns 12 because the value returned is not a #VALUE!</span></span> <span data-ttu-id="2b518-145">Ошибка и выражение указывает, что Visio для возврата значения первой ячейки.</span><span class="sxs-lookup"><span data-stu-id="2b518-145">error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

