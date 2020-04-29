---
title: Функция SIGN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Возвращает значение, представляющее знак числа.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420656"
---
# <a name="sign-function"></a><span data-ttu-id="d1864-103">Функция SIGN</span><span class="sxs-lookup"><span data-stu-id="d1864-103">SIGN Function</span></span>

<span data-ttu-id="d1864-104">Возвращает значение, представляющее знак числа.</span><span class="sxs-lookup"><span data-stu-id="d1864-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d1864-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1864-105">Syntax</span></span>

<span data-ttu-id="d1864-106">SIGN (\* \* *Number* \* \*, \* \* *Монте* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d1864-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d1864-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1864-107">Parameters</span></span>

|<span data-ttu-id="d1864-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d1864-108">**Name**</span></span>|<span data-ttu-id="d1864-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d1864-109">**Required/Optional**</span></span>|<span data-ttu-id="d1864-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d1864-110">**Data Type**</span></span>|<span data-ttu-id="d1864-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1864-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1864-112">_число_</span><span class="sxs-lookup"><span data-stu-id="d1864-112">_number_</span></span> <br/> |<span data-ttu-id="d1864-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="d1864-113">Required</span></span>  <br/> |<span data-ttu-id="d1864-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="d1864-114">**Numeric**</span></span> <br/> | <span data-ttu-id="d1864-115">Число, для которого нужно определить знак.</span><span class="sxs-lookup"><span data-stu-id="d1864-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="d1864-116">_«_</span><span class="sxs-lookup"><span data-stu-id="d1864-116">_fuzz_</span></span> <br/> |<span data-ttu-id="d1864-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d1864-117">Optional</span></span>  <br/> |<span data-ttu-id="d1864-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="d1864-118">**Numeric**</span></span> <br/> |<span data-ttu-id="d1864-119">Указывает, насколько близко к нулю число должно считаться равным нулю.</span><span class="sxs-lookup"><span data-stu-id="d1864-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d1864-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1864-120">Return value</span></span>

<span data-ttu-id="d1864-121">Числовой</span><span class="sxs-lookup"><span data-stu-id="d1864-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1864-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d1864-122">Remarks</span></span>

<span data-ttu-id="d1864-123">Функция SIGN возвращает 1, если _число_ положительно, 0, _Если число_ равно нулю, или-1, если _число_ отрицательное.</span><span class="sxs-lookup"><span data-stu-id="d1864-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="d1864-124">Указание значения параметра _Монте-Карло_ помогает избежать ошибок раундофф с плавающей запятой, если вычисление практически не выполнялось.</span><span class="sxs-lookup"><span data-stu-id="d1864-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="d1864-125">Если не указать значение Монте- _Карло_ , Visio будет использовать 1E-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="d1864-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="d1864-126">При масштабировании рисунков или при необходимости точного сравнения может потребоваться указать другое значение.</span><span class="sxs-lookup"><span data-stu-id="d1864-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d1864-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1864-127">Example 1</span></span>

<span data-ttu-id="d1864-128">SIGN (-5)</span><span class="sxs-lookup"><span data-stu-id="d1864-128">SIGN(-5)</span></span>
  
<span data-ttu-id="d1864-129">Возвращает значение – 1.</span><span class="sxs-lookup"><span data-stu-id="d1864-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d1864-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d1864-130">Example 2</span></span>

<span data-ttu-id="d1864-131">ЗНАК (0)</span><span class="sxs-lookup"><span data-stu-id="d1864-131">SIGN(0)</span></span>
  
<span data-ttu-id="d1864-132">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="d1864-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d1864-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d1864-133">Example 3</span></span>

<span data-ttu-id="d1864-134">SIGN (0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="d1864-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="d1864-135">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="d1864-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="d1864-136">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d1864-136">Example 4</span></span>

<span data-ttu-id="d1864-137">SIGN (0.00000000001, 0)</span><span class="sxs-lookup"><span data-stu-id="d1864-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="d1864-138">Возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="d1864-138">Returns 1.</span></span>
  

