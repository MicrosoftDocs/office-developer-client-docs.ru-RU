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
description: Возвращает остаток (остатка от деления), который является результатом деления числа на делитель.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429273"
---
# <a name="modulus-function"></a><span data-ttu-id="dd77d-103">Функция MODULUS</span><span class="sxs-lookup"><span data-stu-id="dd77d-103">MODULUS Function</span></span>

<span data-ttu-id="dd77d-104">Возвращает остаток (остатка от деления), который является результатом деления числа на делитель.</span><span class="sxs-lookup"><span data-stu-id="dd77d-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dd77d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd77d-105">Syntax</span></span>

<span data-ttu-id="dd77d-106">МОДУЛЬ (\* \* *число* \* \*, \* \* *делитель* \* \*)</span><span class="sxs-lookup"><span data-stu-id="dd77d-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dd77d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd77d-107">Parameters</span></span>

|<span data-ttu-id="dd77d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="dd77d-108">**Name**</span></span>|<span data-ttu-id="dd77d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="dd77d-109">**Required/Optional**</span></span>|<span data-ttu-id="dd77d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="dd77d-110">**Data Type**</span></span>|<span data-ttu-id="dd77d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd77d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dd77d-112">_число_</span><span class="sxs-lookup"><span data-stu-id="dd77d-112">_number_</span></span> <br/> |<span data-ttu-id="dd77d-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="dd77d-113">Required</span></span>  <br/> |<span data-ttu-id="dd77d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="dd77d-114">**Number**</span></span> <br/> |<span data-ttu-id="dd77d-115">Делимое.</span><span class="sxs-lookup"><span data-stu-id="dd77d-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="dd77d-116">_делител_</span><span class="sxs-lookup"><span data-stu-id="dd77d-116">_divisor_</span></span> <br/> |<span data-ttu-id="dd77d-117">Обязательна</span><span class="sxs-lookup"><span data-stu-id="dd77d-117">Required</span></span>  <br/> |<span data-ttu-id="dd77d-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="dd77d-118">**Number**</span></span> <br/> |<span data-ttu-id="dd77d-119">Делитель.</span><span class="sxs-lookup"><span data-stu-id="dd77d-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dd77d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd77d-120">Return value</span></span>

<span data-ttu-id="dd77d-121">Номер</span><span class="sxs-lookup"><span data-stu-id="dd77d-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd77d-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="dd77d-122">Remarks</span></span>

<span data-ttu-id="dd77d-123">Результат имеет тот же знак, что и делитель.</span><span class="sxs-lookup"><span data-stu-id="dd77d-123">The result has the same sign as the divisor.</span></span> <span data-ttu-id="dd77d-124">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="dd77d-124">A #DIV/0!</span></span> <span data-ttu-id="dd77d-125">Если делитель равен 0, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd77d-125">error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="dd77d-126">Почти во всех ситуациях необходимо использовать функцию модуля, а не функцию остат.</span><span class="sxs-lookup"><span data-stu-id="dd77d-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dd77d-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd77d-127">Example 1</span></span>

<span data-ttu-id="dd77d-128">МОДУЛЬ (5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="dd77d-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="dd77d-129">Возвращает 0,8.</span><span class="sxs-lookup"><span data-stu-id="dd77d-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dd77d-130">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dd77d-130">Example 2</span></span>

<span data-ttu-id="dd77d-131">МОДУЛЬ (5,-1,4)</span><span class="sxs-lookup"><span data-stu-id="dd77d-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="dd77d-132">Возвращает значение – 0,6.</span><span class="sxs-lookup"><span data-stu-id="dd77d-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dd77d-133">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dd77d-133">Example 3</span></span>

<span data-ttu-id="dd77d-134">МОДУЛЬ (-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="dd77d-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="dd77d-135">Возвращает 0,6.</span><span class="sxs-lookup"><span data-stu-id="dd77d-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="dd77d-136">Пример 4</span><span class="sxs-lookup"><span data-stu-id="dd77d-136">Example 4</span></span>

<span data-ttu-id="dd77d-137">МОДУЛЬ (-5,-1,4)</span><span class="sxs-lookup"><span data-stu-id="dd77d-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="dd77d-138">Возвращает значение – 0,8.</span><span class="sxs-lookup"><span data-stu-id="dd77d-138">Returns -0.8.</span></span>
  

