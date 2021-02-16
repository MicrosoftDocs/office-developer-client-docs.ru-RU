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
description: Возвращает значение, которое представляет знак числа.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420656"
---
# <a name="sign-function"></a><span data-ttu-id="6a487-103">Функция SIGN</span><span class="sxs-lookup"><span data-stu-id="6a487-103">SIGN Function</span></span>

<span data-ttu-id="6a487-104">Возвращает значение, которое представляет знак числа.</span><span class="sxs-lookup"><span data-stu-id="6a487-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6a487-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a487-105">Syntax</span></span>

<span data-ttu-id="6a487-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6a487-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6a487-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a487-107">Parameters</span></span>

|<span data-ttu-id="6a487-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6a487-108">**Name**</span></span>|<span data-ttu-id="6a487-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="6a487-109">**Required/Optional**</span></span>|<span data-ttu-id="6a487-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6a487-110">**Data Type**</span></span>|<span data-ttu-id="6a487-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6a487-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6a487-112">_число_</span><span class="sxs-lookup"><span data-stu-id="6a487-112">_number_</span></span> <br/> |<span data-ttu-id="6a487-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="6a487-113">Required</span></span>  <br/> |<span data-ttu-id="6a487-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6a487-114">**Numeric**</span></span> <br/> | <span data-ttu-id="6a487-115">Номер, для которого нужно определить знак.</span><span class="sxs-lookup"><span data-stu-id="6a487-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="6a487-116">_fuzz_</span><span class="sxs-lookup"><span data-stu-id="6a487-116">_fuzz_</span></span> <br/> |<span data-ttu-id="6a487-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="6a487-117">Optional</span></span>  <br/> |<span data-ttu-id="6a487-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="6a487-118">**Numeric**</span></span> <br/> |<span data-ttu-id="6a487-119">Указывает, насколько близко к нулю должно быть число, чтобы считаться равным нулю.</span><span class="sxs-lookup"><span data-stu-id="6a487-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6a487-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a487-120">Return value</span></span>

<span data-ttu-id="6a487-121">Числовой</span><span class="sxs-lookup"><span data-stu-id="6a487-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a487-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a487-122">Remarks</span></span>

<span data-ttu-id="6a487-123">Функция SIGN возвращает 1, если число положительное, 0, если _число_ — ноль, или -1, если _число_ отрицательное. </span><span class="sxs-lookup"><span data-stu-id="6a487-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="6a487-124">Указание  _нечеткого_ значения помогает избежать ошибок округления с плавающей за точкой, если вычисление почти нулевое.</span><span class="sxs-lookup"><span data-stu-id="6a487-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="6a487-125">Если не указать  нечеткое значение, Visio использует 1E-9 (0,0000000001).</span><span class="sxs-lookup"><span data-stu-id="6a487-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="6a487-126">При масштабирования рисунков или при точном сравнении может потребоваться предоставить другое значение.</span><span class="sxs-lookup"><span data-stu-id="6a487-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6a487-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a487-127">Example 1</span></span>

<span data-ttu-id="6a487-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="6a487-128">SIGN(-5)</span></span>
  
<span data-ttu-id="6a487-129">Возвращает -1.</span><span class="sxs-lookup"><span data-stu-id="6a487-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6a487-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6a487-130">Example 2</span></span>

<span data-ttu-id="6a487-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="6a487-131">SIGN(0)</span></span>
  
<span data-ttu-id="6a487-132">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="6a487-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6a487-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6a487-133">Example 3</span></span>

<span data-ttu-id="6a487-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="6a487-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="6a487-135">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="6a487-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6a487-136">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6a487-136">Example 4</span></span>

<span data-ttu-id="6a487-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="6a487-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="6a487-138">Возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="6a487-138">Returns 1.</span></span>
  

