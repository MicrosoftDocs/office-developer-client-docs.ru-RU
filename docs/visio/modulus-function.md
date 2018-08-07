---
title: Функция MODULUS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Возвращает остаток от деления, полученные при делении числа на делителя.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814284"
---
# <a name="modulus-function"></a><span data-ttu-id="0c683-103">Функция MODULUS</span><span class="sxs-lookup"><span data-stu-id="0c683-103">MODULUS Function</span></span>

<span data-ttu-id="0c683-104">Возвращает остаток от деления, полученные при делении числа на делителя.</span><span class="sxs-lookup"><span data-stu-id="0c683-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0c683-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c683-105">Syntax</span></span>

<span data-ttu-id="0c683-106">Операции с МОДУЛЯМИ (** *номер* **, ** *делителя* **)</span><span class="sxs-lookup"><span data-stu-id="0c683-106">MODULUS(** *number* **, ** *divisor* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0c683-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c683-107">Parameters</span></span>

|<span data-ttu-id="0c683-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0c683-108">**Name**</span></span>|<span data-ttu-id="0c683-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="0c683-109">**Required/Optional**</span></span>|<span data-ttu-id="0c683-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0c683-110">**Data Type**</span></span>|<span data-ttu-id="0c683-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c683-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0c683-112">_number_</span><span class="sxs-lookup"><span data-stu-id="0c683-112">_number_</span></span> <br/> |<span data-ttu-id="0c683-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c683-113">Required</span></span>  <br/> |<span data-ttu-id="0c683-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="0c683-114">**Number**</span></span> <br/> |<span data-ttu-id="0c683-115">Дивидендов.</span><span class="sxs-lookup"><span data-stu-id="0c683-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="0c683-116">_делителя_</span><span class="sxs-lookup"><span data-stu-id="0c683-116">_divisor_</span></span> <br/> |<span data-ttu-id="0c683-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0c683-117">Required</span></span>  <br/> |<span data-ttu-id="0c683-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="0c683-118">**Number**</span></span> <br/> |<span data-ttu-id="0c683-119">Делителя.</span><span class="sxs-lookup"><span data-stu-id="0c683-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0c683-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="0c683-121">Number</span><span class="sxs-lookup"><span data-stu-id="0c683-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c683-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="0c683-122">Remarks</span></span>

<span data-ttu-id="0c683-123">Результат имеет тот же знак в качестве делителя.</span><span class="sxs-lookup"><span data-stu-id="0c683-123">The result has the same sign as the divisor.</span></span> <span data-ttu-id="0c683-124">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="0c683-124">A #DIV/0!</span></span> <span data-ttu-id="0c683-125">Если делителя равно 0, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="0c683-125">error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="0c683-126">В большинстве случаев функции МОДУЛЯ можно использовать вместо функция МОД.</span><span class="sxs-lookup"><span data-stu-id="0c683-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0c683-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c683-127">Example 1</span></span>

<span data-ttu-id="0c683-128">ОПЕРАЦИИ С МОДУЛЯМИ (5, 1.4)</span><span class="sxs-lookup"><span data-stu-id="0c683-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="0c683-129">Возвращает 0,8.</span><span class="sxs-lookup"><span data-stu-id="0c683-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0c683-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0c683-130">Example 2</span></span>

<span data-ttu-id="0c683-131">ОПЕРАЦИИ С МОДУЛЯМИ (5,-1.4)</span><span class="sxs-lookup"><span data-stu-id="0c683-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="0c683-132">Возвращает-0.6.</span><span class="sxs-lookup"><span data-stu-id="0c683-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0c683-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0c683-133">Example 3</span></span>

<span data-ttu-id="0c683-134">ОПЕРАЦИИ С МОДУЛЯМИ (-5, 1.4)</span><span class="sxs-lookup"><span data-stu-id="0c683-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="0c683-135">Возвращает 0,6.</span><span class="sxs-lookup"><span data-stu-id="0c683-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="0c683-136">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0c683-136">Example 4</span></span>

<span data-ttu-id="0c683-137">ОПЕРАЦИИ С МОДУЛЯМИ (-5,-1.4)</span><span class="sxs-lookup"><span data-stu-id="0c683-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="0c683-138">Возвращает-0.8.</span><span class="sxs-lookup"><span data-stu-id="0c683-138">Returns -0.8.</span></span>
  

