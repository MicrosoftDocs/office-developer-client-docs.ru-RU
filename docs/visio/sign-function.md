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
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814878"
---
# <a name="sign-function"></a><span data-ttu-id="482de-103">Функция SIGN</span><span class="sxs-lookup"><span data-stu-id="482de-103">SIGN Function</span></span>

<span data-ttu-id="482de-104">Возвращает значение, представляющее знак числа.</span><span class="sxs-lookup"><span data-stu-id="482de-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="482de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="482de-105">Syntax</span></span>

<span data-ttu-id="482de-106">ЗНАК (** *номер* **, ** *fuzz* **)</span><span class="sxs-lookup"><span data-stu-id="482de-106">SIGN(** *number* **, ** *fuzz* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="482de-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="482de-107">Parameters</span></span>

|<span data-ttu-id="482de-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="482de-108">**Name**</span></span>|<span data-ttu-id="482de-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="482de-109">**Required/Optional**</span></span>|<span data-ttu-id="482de-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="482de-110">**Data Type**</span></span>|<span data-ttu-id="482de-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="482de-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="482de-112">_number_</span><span class="sxs-lookup"><span data-stu-id="482de-112">_number_</span></span> <br/> |<span data-ttu-id="482de-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="482de-113">Required</span></span>  <br/> |<span data-ttu-id="482de-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="482de-114">**Numeric**</span></span> <br/> | <span data-ttu-id="482de-115">Номер, для которого требуется для определения знака.</span><span class="sxs-lookup"><span data-stu-id="482de-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="482de-116">_Fuzz_</span><span class="sxs-lookup"><span data-stu-id="482de-116">_fuzz_</span></span> <br/> |<span data-ttu-id="482de-117">Optional</span><span class="sxs-lookup"><span data-stu-id="482de-117">Optional</span></span>  <br/> |<span data-ttu-id="482de-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="482de-118">**Numeric**</span></span> <br/> |<span data-ttu-id="482de-119">Указывает, как закрытие нулевое значение должно быть чтобы считаться равно нулю.</span><span class="sxs-lookup"><span data-stu-id="482de-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="482de-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="482de-121">Числовой</span><span class="sxs-lookup"><span data-stu-id="482de-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="482de-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="482de-122">Remarks</span></span>

<span data-ttu-id="482de-123">Функция знак возвращает значение 1, если _число_ является положительным, если _число_ равняется нулю, или значение -1, если _число_ равняется 0 отрицательных результатах.</span><span class="sxs-lookup"><span data-stu-id="482de-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="482de-124">Specifyin значение _fuzz_ помогает избежать ошибок с плавающей запятой округление, когда вычисление равно нулю почти.</span><span class="sxs-lookup"><span data-stu-id="482de-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="482de-125">Если не указать значение _fuzz_ , Visio использует 1E-9 (0.000000001).</span><span class="sxs-lookup"><span data-stu-id="482de-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="482de-126">Можно указать другое значение при масштабировании документы или если вы хотите точного сравнения.</span><span class="sxs-lookup"><span data-stu-id="482de-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="482de-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="482de-127">Example 1</span></span>

<span data-ttu-id="482de-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="482de-128">SIGN(-5)</span></span>
  
<span data-ttu-id="482de-129">Возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="482de-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="482de-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="482de-130">Example 2</span></span>

<span data-ttu-id="482de-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="482de-131">SIGN(0)</span></span>
  
<span data-ttu-id="482de-132">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="482de-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="482de-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="482de-133">Example 3</span></span>

<span data-ttu-id="482de-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="482de-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="482de-135">Возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="482de-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="482de-136">Пример 4</span><span class="sxs-lookup"><span data-stu-id="482de-136">Example 4</span></span>

<span data-ttu-id="482de-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="482de-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="482de-138">Возвращает 1.</span><span class="sxs-lookup"><span data-stu-id="482de-138">Returns 1.</span></span>
  

